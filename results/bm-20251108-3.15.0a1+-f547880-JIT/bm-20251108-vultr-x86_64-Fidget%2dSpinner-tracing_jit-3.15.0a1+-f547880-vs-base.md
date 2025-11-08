# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: f547880
- commit date: 2025-11-08
- overall geometric mean: 1.012x faster
- HPT reliability: 92.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 251 ms: 1.02x faster                                                    |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                  |
| html5lib       | 61.4 ms                                                                | 68.0 ms: 1.11x slower                                                   |
| sphinx         | 993 ms                                                                 | 1.02 sec: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators          | 364 ms                                                                 | 358 ms: 1.02x faster                                                    |
| async_tree_io_tg          | 594 ms                                                                 | 598 ms: 1.01x slower                                                    |
| async_tree_memoization_tg | 306 ms                                                                 | 312 ms: 1.02x slower                                                    |
| async_tree_none_tg        | 243 ms                                                                 | 248 ms: 1.02x slower                                                    |
| coroutines                | 24.3 ms                                                                | 25.0 ms: 1.03x slower                                                   |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (6): async_tree_none, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 70.6 ms                                                                | 60.5 ms: 1.17x faster                                                   |
| pidigits       | 209 ms                                                                 | 207 ms: 1.01x faster                                                    |
| nbody          | 84.6 ms                                                                | 86.5 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 22.6 ms                                                                | 21.2 ms: 1.06x faster                                                   |
| regex_dna      | 175 ms                                                                 | 171 ms: 1.02x faster                                                    |
| regex_compile  | 126 ms                                                                 | 125 ms: 1.01x faster                                                    |
| regex_effbot   | 2.59 ms                                                                | 2.62 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|---------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps          | 9.31 ms                                                                | 9.03 ms: 1.03x faster                                                   |
| pickle_pure_python  | 307 us                                                                 | 300 us: 1.02x faster                                                    |
| xml_etree_iterparse | 85.4 ms                                                                | 83.4 ms: 1.02x faster                                                   |
| xml_etree_parse     | 129 ms                                                                 | 128 ms: 1.01x faster                                                    |
| xml_etree_generate  | 77.0 ms                                                                | 77.8 ms: 1.01x slower                                                   |
| xml_etree_process   | 53.7 ms                                                                | 54.3 ms: 1.01x slower                                                   |
| tomli_loads         | 1.75 sec                                                               | 1.83 sec: 1.05x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (2): unpickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.24 ms                                                                | 7.26 ms: 1.00x slower                                                   |
| python_startup         | 12.4 ms                                                                | 12.5 ms: 1.00x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.6 ms                                                                | 35.2 ms: 1.02x slower                                                   |
| genshi_text     | 20.5 ms                                                                | 21.4 ms: 1.05x slower                                                   |
| genshi_xml      | 49.3 ms                                                                | 55.5 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251108-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f547880 |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                  | 42.2 ms                                                                | 21.8 ms: 1.94x faster                                                   |
| richards_super            | 48.4 ms                                                                | 26.1 ms: 1.86x faster                                                   |
| spectral_norm             | 96.7 ms                                                                | 82.7 ms: 1.17x faster                                                   |
| float                     | 70.6 ms                                                                | 60.5 ms: 1.17x faster                                                   |
| logging_silent            | 99.6 ns                                                                | 87.8 ns: 1.14x faster                                                   |
| scimark_monte_carlo       | 62.0 ms                                                                | 54.9 ms: 1.13x faster                                                   |
| deltablue                 | 3.15 ms                                                                | 2.82 ms: 1.12x faster                                                   |
| scimark_sor               | 108 ms                                                                 | 96.6 ms: 1.12x faster                                                   |
| pyflate                   | 401 ms                                                                 | 369 ms: 1.09x faster                                                    |
| scimark_lu                | 110 ms                                                                 | 101 ms: 1.08x faster                                                    |
| regex_v8                  | 22.6 ms                                                                | 21.2 ms: 1.06x faster                                                   |
| deepcopy_memo             | 26.6 us                                                                | 25.2 us: 1.06x faster                                                   |
| chaos                     | 57.1 ms                                                                | 54.4 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult   | 4.21 ms                                                                | 4.04 ms: 1.04x faster                                                   |
| crypto_pyaes              | 67.8 ms                                                                | 65.7 ms: 1.03x faster                                                   |
| json_dumps                | 9.31 ms                                                                | 9.03 ms: 1.03x faster                                                   |
| meteor_contest            | 99.8 ms                                                                | 97.2 ms: 1.03x faster                                                   |
| go                        | 107 ms                                                                 | 104 ms: 1.03x faster                                                    |
| pickle_pure_python        | 307 us                                                                 | 300 us: 1.02x faster                                                    |
| xml_etree_iterparse       | 85.4 ms                                                                | 83.4 ms: 1.02x faster                                                   |
| create_gc_cycles          | 1.94 ms                                                                | 1.90 ms: 1.02x faster                                                   |
| regex_dna                 | 175 ms                                                                 | 171 ms: 1.02x faster                                                    |
| 2to3                      | 255 ms                                                                 | 251 ms: 1.02x faster                                                    |
| async_generators          | 364 ms                                                                 | 358 ms: 1.02x faster                                                    |
| scimark_fft               | 257 ms                                                                 | 253 ms: 1.01x faster                                                    |
| logging_format            | 6.65 us                                                                | 6.56 us: 1.01x faster                                                   |
| json                      | 5.00 ms                                                                | 4.94 ms: 1.01x faster                                                   |
| pidigits                  | 209 ms                                                                 | 207 ms: 1.01x faster                                                    |
| regex_compile             | 126 ms                                                                 | 125 ms: 1.01x faster                                                    |
| coverage                  | 82.3 ms                                                                | 81.5 ms: 1.01x faster                                                   |
| xml_etree_parse           | 129 ms                                                                 | 128 ms: 1.01x faster                                                    |
| comprehensions            | 16.1 us                                                                | 16.0 us: 1.01x faster                                                   |
| python_startup_no_site    | 7.24 ms                                                                | 7.26 ms: 1.00x slower                                                   |
| python_startup            | 12.4 ms                                                                | 12.5 ms: 1.00x slower                                                   |
| bench_thread_pool         | 1.01 ms                                                                | 1.01 ms: 1.01x slower                                                   |
| async_tree_io_tg          | 594 ms                                                                 | 598 ms: 1.01x slower                                                    |
| regex_effbot              | 2.59 ms                                                                | 2.62 ms: 1.01x slower                                                   |
| xml_etree_generate        | 77.0 ms                                                                | 77.8 ms: 1.01x slower                                                   |
| xml_etree_process         | 53.7 ms                                                                | 54.3 ms: 1.01x slower                                                   |
| deepcopy_reduce           | 2.59 us                                                                | 2.62 us: 1.01x slower                                                   |
| subparsers                | 45.0 ms                                                                | 45.6 ms: 1.01x slower                                                   |
| pathlib                   | 17.5 ms                                                                | 17.8 ms: 1.02x slower                                                   |
| sqlglot_v2_parse          | 1.21 ms                                                                | 1.23 ms: 1.02x slower                                                   |
| async_tree_memoization_tg | 306 ms                                                                 | 312 ms: 1.02x slower                                                    |
| sqlglot_v2_transpile      | 1.51 ms                                                                | 1.54 ms: 1.02x slower                                                   |
| django_template           | 34.6 ms                                                                | 35.2 ms: 1.02x slower                                                   |
| async_tree_none_tg        | 243 ms                                                                 | 248 ms: 1.02x slower                                                    |
| nbody                     | 84.6 ms                                                                | 86.5 ms: 1.02x slower                                                   |
| logging_simple            | 5.77 us                                                                | 5.90 us: 1.02x slower                                                   |
| hexiom                    | 5.97 ms                                                                | 6.12 ms: 1.02x slower                                                   |
| coroutines                | 24.3 ms                                                                | 25.0 ms: 1.03x slower                                                   |
| sympy_expand              | 487 ms                                                                 | 503 ms: 1.03x slower                                                    |
| sphinx                    | 993 ms                                                                 | 1.02 sec: 1.03x slower                                                  |
| sqlglot_v2_optimize       | 51.4 ms                                                                | 53.4 ms: 1.04x slower                                                   |
| deepcopy                  | 245 us                                                                 | 255 us: 1.04x slower                                                    |
| many_optionals            | 1.23 ms                                                                | 1.29 ms: 1.04x slower                                                   |
| sympy_integrate           | 19.4 ms                                                                | 20.3 ms: 1.04x slower                                                   |
| genshi_text               | 20.5 ms                                                                | 21.4 ms: 1.05x slower                                                   |
| tomli_loads               | 1.75 sec                                                               | 1.83 sec: 1.05x slower                                                  |
| nqueens                   | 81.5 ms                                                                | 85.4 ms: 1.05x slower                                                   |
| sqlglot_v2_normalize      | 103 ms                                                                 | 108 ms: 1.05x slower                                                    |
| docutils                  | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                  |
| pylint                    | 293 ms                                                                 | 313 ms: 1.07x slower                                                    |
| sympy_sum                 | 158 ms                                                                 | 170 ms: 1.07x slower                                                    |
| sympy_str                 | 282 ms                                                                 | 307 ms: 1.09x slower                                                    |
| generators                | 27.5 ms                                                                | 29.9 ms: 1.09x slower                                                   |
| dulwich_log               | 69.7 ms                                                                | 75.9 ms: 1.09x slower                                                   |
| raytrace                  | 251 ms                                                                 | 275 ms: 1.09x slower                                                    |
| html5lib                  | 61.4 ms                                                                | 68.0 ms: 1.11x slower                                                   |
| genshi_xml                | 49.3 ms                                                                | 55.5 ms: 1.13x slower                                                   |
| mdp                       | 1.16 sec                                                               | 1.35 sec: 1.16x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (23): pprint_pformat, async_tree_none, gc_traversal, thrift, typing_runtime_protocols, connected_components, bench_mp_pool, asyncio_websockets, fannkuch, unpickle_pure_python, shortest_path, bpe_tokeniser, k_core, sqlite_synth, json_loads, telco, async_tree_cpu_io_mixed, mako, pycparser, async_tree_io, async_tree_cpu_io_mixed_tg, pprint_safe_repr, async_tree_memoization

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 92.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x