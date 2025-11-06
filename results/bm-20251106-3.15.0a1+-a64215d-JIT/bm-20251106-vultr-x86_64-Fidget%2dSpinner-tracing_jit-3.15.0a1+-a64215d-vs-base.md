# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: a64215d
- commit date: 2025-11-06
- overall geometric mean: 1.011x faster
- HPT reliability: 97.37%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 252 ms: 1.01x faster                                                    |
| docutils       | 2.63 sec                                                               | 2.76 sec: 1.05x slower                                                  |
| html5lib       | 61.4 ms                                                                | 68.9 ms: 1.12x slower                                                   |
| sphinx         | 993 ms                                                                 | 1.03 sec: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators          | 364 ms                                                                 | 361 ms: 1.01x faster                                                    |
| coroutines                | 24.3 ms                                                                | 24.2 ms: 1.01x faster                                                   |
| async_tree_memoization_tg | 306 ms                                                                 | 309 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed   | 484 ms                                                                 | 491 ms: 1.01x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (7): async_tree_none, asyncio_websockets, async_tree_io, async_tree_io_tg, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 70.6 ms                                                                | 60.7 ms: 1.16x faster                                                   |
| pidigits       | 209 ms                                                                 | 200 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 22.6 ms                                                                | 21.7 ms: 1.04x faster                                                   |
| regex_dna      | 175 ms                                                                 | 176 ms: 1.01x slower                                                    |
| regex_effbot   | 2.59 ms                                                                | 2.71 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|---------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python  | 307 us                                                                 | 299 us: 1.03x faster                                                    |
| xml_etree_iterparse | 85.4 ms                                                                | 83.6 ms: 1.02x faster                                                   |
| json_dumps          | 9.31 ms                                                                | 9.13 ms: 1.02x faster                                                   |
| xml_etree_parse     | 129 ms                                                                 | 128 ms: 1.01x faster                                                    |
| xml_etree_process   | 53.7 ms                                                                | 54.9 ms: 1.02x slower                                                   |
| xml_etree_generate  | 77.0 ms                                                                | 79.7 ms: 1.04x slower                                                   |
| tomli_loads         | 1.75 sec                                                               | 1.84 sec: 1.05x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (2): unpickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.24 ms                                                                | 7.25 ms: 1.00x slower                                                   |
| python_startup         | 12.4 ms                                                                | 12.4 ms: 1.00x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.7 ms                                                                | 10.5 ms: 1.02x faster                                                   |
| django_template | 34.6 ms                                                                | 35.3 ms: 1.02x slower                                                   |
| genshi_text     | 20.5 ms                                                                | 21.5 ms: 1.05x slower                                                   |
| genshi_xml      | 49.3 ms                                                                | 55.1 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                 | bm-20251101-vultr-x86_64-python-b1554146c29182803d1d-3.15.0a1+-b155414 | bm-20251106-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-a64215d |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                  | 42.2 ms                                                                | 21.5 ms: 1.97x faster                                                   |
| richards_super            | 48.4 ms                                                                | 25.8 ms: 1.87x faster                                                   |
| float                     | 70.6 ms                                                                | 60.7 ms: 1.16x faster                                                   |
| spectral_norm             | 96.7 ms                                                                | 83.6 ms: 1.16x faster                                                   |
| logging_silent            | 99.6 ns                                                                | 86.4 ns: 1.15x faster                                                   |
| scimark_monte_carlo       | 62.0 ms                                                                | 55.0 ms: 1.13x faster                                                   |
| scimark_sor               | 108 ms                                                                 | 95.8 ms: 1.13x faster                                                   |
| deltablue                 | 3.15 ms                                                                | 2.81 ms: 1.12x faster                                                   |
| pyflate                   | 401 ms                                                                 | 367 ms: 1.09x faster                                                    |
| scimark_lu                | 110 ms                                                                 | 102 ms: 1.07x faster                                                    |
| deepcopy_memo             | 26.6 us                                                                | 25.1 us: 1.06x faster                                                   |
| chaos                     | 57.1 ms                                                                | 54.1 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult   | 4.21 ms                                                                | 4.03 ms: 1.04x faster                                                   |
| pidigits                  | 209 ms                                                                 | 200 ms: 1.04x faster                                                    |
| regex_v8                  | 22.6 ms                                                                | 21.7 ms: 1.04x faster                                                   |
| go                        | 107 ms                                                                 | 103 ms: 1.03x faster                                                    |
| crypto_pyaes              | 67.8 ms                                                                | 65.6 ms: 1.03x faster                                                   |
| pickle_pure_python        | 307 us                                                                 | 299 us: 1.03x faster                                                    |
| mako                      | 10.7 ms                                                                | 10.5 ms: 1.02x faster                                                   |
| xml_etree_iterparse       | 85.4 ms                                                                | 83.6 ms: 1.02x faster                                                   |
| json_dumps                | 9.31 ms                                                                | 9.13 ms: 1.02x faster                                                   |
| logging_format            | 6.65 us                                                                | 6.53 us: 1.02x faster                                                   |
| coverage                  | 82.3 ms                                                                | 80.9 ms: 1.02x faster                                                   |
| 2to3                      | 255 ms                                                                 | 252 ms: 1.01x faster                                                    |
| scimark_fft               | 257 ms                                                                 | 253 ms: 1.01x faster                                                    |
| comprehensions            | 16.1 us                                                                | 16.0 us: 1.01x faster                                                   |
| xml_etree_parse           | 129 ms                                                                 | 128 ms: 1.01x faster                                                    |
| async_generators          | 364 ms                                                                 | 361 ms: 1.01x faster                                                    |
| json                      | 5.00 ms                                                                | 4.96 ms: 1.01x faster                                                   |
| coroutines                | 24.3 ms                                                                | 24.2 ms: 1.01x faster                                                   |
| python_startup_no_site    | 7.24 ms                                                                | 7.25 ms: 1.00x slower                                                   |
| k_core                    | 1.87 sec                                                               | 1.87 sec: 1.00x slower                                                  |
| python_startup            | 12.4 ms                                                                | 12.4 ms: 1.00x slower                                                   |
| bench_thread_pool         | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                   |
| async_tree_memoization_tg | 306 ms                                                                 | 309 ms: 1.01x slower                                                    |
| fannkuch                  | 363 ms                                                                 | 366 ms: 1.01x slower                                                    |
| pathlib                   | 17.5 ms                                                                | 17.7 ms: 1.01x slower                                                   |
| regex_dna                 | 175 ms                                                                 | 176 ms: 1.01x slower                                                    |
| logging_simple            | 5.77 us                                                                | 5.83 us: 1.01x slower                                                   |
| shortest_path             | 436 ms                                                                 | 442 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed   | 484 ms                                                                 | 491 ms: 1.01x slower                                                    |
| meteor_contest            | 99.8 ms                                                                | 101 ms: 1.01x slower                                                    |
| connected_components      | 390 ms                                                                 | 395 ms: 1.01x slower                                                    |
| subparsers                | 45.0 ms                                                                | 45.6 ms: 1.01x slower                                                   |
| telco                     | 159 ms                                                                 | 162 ms: 1.02x slower                                                    |
| hexiom                    | 5.97 ms                                                                | 6.09 ms: 1.02x slower                                                   |
| django_template           | 34.6 ms                                                                | 35.3 ms: 1.02x slower                                                   |
| deepcopy_reduce           | 2.59 us                                                                | 2.65 us: 1.02x slower                                                   |
| xml_etree_process         | 53.7 ms                                                                | 54.9 ms: 1.02x slower                                                   |
| deepcopy                  | 245 us                                                                 | 253 us: 1.03x slower                                                    |
| sphinx                    | 993 ms                                                                 | 1.03 sec: 1.03x slower                                                  |
| xml_etree_generate        | 77.0 ms                                                                | 79.7 ms: 1.04x slower                                                   |
| bpe_tokeniser             | 3.96 sec                                                               | 4.13 sec: 1.04x slower                                                  |
| nqueens                   | 81.5 ms                                                                | 85.0 ms: 1.04x slower                                                   |
| sympy_expand              | 487 ms                                                                 | 508 ms: 1.04x slower                                                    |
| many_optionals            | 1.23 ms                                                                | 1.29 ms: 1.04x slower                                                   |
| regex_effbot              | 2.59 ms                                                                | 2.71 ms: 1.05x slower                                                   |
| genshi_text               | 20.5 ms                                                                | 21.5 ms: 1.05x slower                                                   |
| sympy_integrate           | 19.4 ms                                                                | 20.3 ms: 1.05x slower                                                   |
| sqlglot_v2_optimize       | 51.4 ms                                                                | 53.9 ms: 1.05x slower                                                   |
| docutils                  | 2.63 sec                                                               | 2.76 sec: 1.05x slower                                                  |
| generators                | 27.5 ms                                                                | 28.9 ms: 1.05x slower                                                   |
| tomli_loads               | 1.75 sec                                                               | 1.84 sec: 1.05x slower                                                  |
| sqlglot_v2_normalize      | 103 ms                                                                 | 108 ms: 1.06x slower                                                    |
| sympy_sum                 | 158 ms                                                                 | 168 ms: 1.06x slower                                                    |
| pylint                    | 293 ms                                                                 | 312 ms: 1.07x slower                                                    |
| dulwich_log               | 69.7 ms                                                                | 75.0 ms: 1.08x slower                                                   |
| sympy_str                 | 282 ms                                                                 | 306 ms: 1.08x slower                                                    |
| gc_traversal              | 4.40 ms                                                                | 4.78 ms: 1.09x slower                                                   |
| raytrace                  | 251 ms                                                                 | 275 ms: 1.10x slower                                                    |
| genshi_xml                | 49.3 ms                                                                | 55.1 ms: 1.12x slower                                                   |
| html5lib                  | 61.4 ms                                                                | 68.9 ms: 1.12x slower                                                   |
| mdp                       | 1.16 sec                                                               | 1.33 sec: 1.15x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (21): pprint_pformat, nbody, async_tree_none, sqlglot_v2_parse, bench_mp_pool, sqlite_synth, unpickle_pure_python, asyncio_websockets, sqlglot_v2_transpile, regex_compile, async_tree_io, create_gc_cycles, thrift, async_tree_io_tg, async_tree_none_tg, json_loads, async_tree_memoization, typing_runtime_protocols, async_tree_cpu_io_mixed_tg, pycparser, pprint_safe_repr

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 97.37% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x