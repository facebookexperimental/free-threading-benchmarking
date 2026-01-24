# Results vs. base

- fork: Fidget-Spinner
- ref: loop_2000
- machine: linux-x86_64
- commit hash: cec96a9
- commit date: 2026-01-24
- overall geometric mean: 1.003x slower
- HPT reliability: 98.89%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                 | 254 ms: 1.02x slower                                                  |
| html5lib       | 62.0 ms                                                                | 62.9 ms: 1.02x slower                                                 |
| sphinx         | 984 ms                                                                 | 998 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators          | 359 ms                                                                 | 355 ms: 1.01x faster                                                  |
| asyncio_websockets        | 544 ms                                                                 | 545 ms: 1.00x slower                                                  |
| async_tree_cpu_io_mixed   | 471 ms                                                                 | 479 ms: 1.02x slower                                                  |
| async_tree_memoization_tg | 286 ms                                                                 | 292 ms: 1.02x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (7): coroutines, async_tree_memoization, async_tree_io_tg, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 74.3 ms                                                                | 72.8 ms: 1.02x faster                                                 |
| pidigits       | 192 ms                                                                 | 197 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 177 ms                                                                 | 168 ms: 1.05x faster                                                  |
| regex_effbot   | 2.76 ms                                                                | 2.65 ms: 1.04x faster                                                 |
| regex_v8       | 21.0 ms                                                                | 20.8 ms: 1.01x faster                                                 |
| regex_compile  | 121 ms                                                                 | 122 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 9.20 ms                                                                | 9.01 ms: 1.02x faster                                                 |
| xml_etree_parse      | 131 ms                                                                 | 129 ms: 1.02x faster                                                  |
| xml_etree_iterparse  | 84.5 ms                                                                | 83.4 ms: 1.01x faster                                                 |
| xml_etree_process    | 54.2 ms                                                                | 53.6 ms: 1.01x faster                                                 |
| json_loads           | 28.3 us                                                                | 28.1 us: 1.01x faster                                                 |
| pickle_pure_python   | 276 us                                                                 | 278 us: 1.01x slower                                                  |
| tomli_loads          | 1.64 sec                                                               | 1.67 sec: 1.01x slower                                                |
| unpickle_pure_python | 175 us                                                                 | 178 us: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                | 12.6 ms: 1.00x faster                                                 |
| python_startup_no_site | 7.38 ms                                                                | 7.37 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 10.6 ms                                                                | 10.3 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (3): genshi_xml, django_template, genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20260124-vultr-x86_64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 | bm-20260124-vultr-x86_64-Fidget%2dSpinner-loop_2000-3.15.0a5+-cec96a9 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| bench_mp_pool             | 226 ms                                                                 | 183 ms: 1.23x faster                                                  |
| create_gc_cycles          | 1.95 ms                                                                | 1.85 ms: 1.06x faster                                                 |
| regex_dna                 | 177 ms                                                                 | 168 ms: 1.05x faster                                                  |
| generators                | 29.5 ms                                                                | 28.2 ms: 1.05x faster                                                 |
| regex_effbot              | 2.76 ms                                                                | 2.65 ms: 1.04x faster                                                 |
| typing_runtime_protocols  | 162 us                                                                 | 156 us: 1.04x faster                                                  |
| pprint_pformat            | 1.30 sec                                                               | 1.25 sec: 1.04x faster                                                |
| crypto_pyaes              | 67.2 ms                                                                | 65.1 ms: 1.03x faster                                                 |
| mako                      | 10.6 ms                                                                | 10.3 ms: 1.03x faster                                                 |
| scimark_sor               | 86.9 ms                                                                | 84.8 ms: 1.03x faster                                                 |
| logging_silent            | 83.2 ns                                                                | 81.2 ns: 1.02x faster                                                 |
| pprint_safe_repr          | 636 ms                                                                 | 621 ms: 1.02x faster                                                  |
| richards_super            | 21.5 ms                                                                | 21.0 ms: 1.02x faster                                                 |
| richards                  | 17.8 ms                                                                | 17.4 ms: 1.02x faster                                                 |
| json_dumps                | 9.20 ms                                                                | 9.01 ms: 1.02x faster                                                 |
| nbody                     | 74.3 ms                                                                | 72.8 ms: 1.02x faster                                                 |
| bpe_tokeniser             | 4.02 sec                                                               | 3.94 sec: 1.02x faster                                                |
| xml_etree_parse           | 131 ms                                                                 | 129 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult   | 4.15 ms                                                                | 4.09 ms: 1.01x faster                                                 |
| xml_etree_iterparse       | 84.5 ms                                                                | 83.4 ms: 1.01x faster                                                 |
| nqueens                   | 79.9 ms                                                                | 78.9 ms: 1.01x faster                                                 |
| xml_etree_process         | 54.2 ms                                                                | 53.6 ms: 1.01x faster                                                 |
| async_generators          | 359 ms                                                                 | 355 ms: 1.01x faster                                                  |
| regex_v8                  | 21.0 ms                                                                | 20.8 ms: 1.01x faster                                                 |
| k_core                    | 1.85 sec                                                               | 1.84 sec: 1.01x faster                                                |
| spectral_norm             | 81.4 ms                                                                | 80.9 ms: 1.01x faster                                                 |
| json_loads                | 28.3 us                                                                | 28.1 us: 1.01x faster                                                 |
| python_startup            | 12.6 ms                                                                | 12.6 ms: 1.00x faster                                                 |
| python_startup_no_site    | 7.38 ms                                                                | 7.37 ms: 1.00x faster                                                 |
| asyncio_websockets        | 544 ms                                                                 | 545 ms: 1.00x slower                                                  |
| deltablue                 | 2.73 ms                                                                | 2.74 ms: 1.00x slower                                                 |
| mdp                       | 1.35 sec                                                               | 1.36 sec: 1.01x slower                                                |
| dulwich_log               | 71.8 ms                                                                | 72.3 ms: 1.01x slower                                                 |
| coverage                  | 81.3 ms                                                                | 81.9 ms: 1.01x slower                                                 |
| pickle_pure_python        | 276 us                                                                 | 278 us: 1.01x slower                                                  |
| scimark_monte_carlo       | 51.7 ms                                                                | 52.1 ms: 1.01x slower                                                 |
| deepcopy_memo             | 22.4 us                                                                | 22.6 us: 1.01x slower                                                 |
| regex_compile             | 121 ms                                                                 | 122 ms: 1.01x slower                                                  |
| pyflate                   | 368 ms                                                                 | 372 ms: 1.01x slower                                                  |
| shortest_path             | 423 ms                                                                 | 428 ms: 1.01x slower                                                  |
| sphinx                    | 984 ms                                                                 | 998 ms: 1.01x slower                                                  |
| gc_traversal              | 4.28 ms                                                                | 4.35 ms: 1.01x slower                                                 |
| tomli_loads               | 1.64 sec                                                               | 1.67 sec: 1.01x slower                                                |
| comprehensions            | 15.8 us                                                                | 16.1 us: 1.02x slower                                                 |
| html5lib                  | 62.0 ms                                                                | 62.9 ms: 1.02x slower                                                 |
| pycparser                 | 1.11 sec                                                               | 1.13 sec: 1.02x slower                                                |
| connected_components      | 372 ms                                                                 | 378 ms: 1.02x slower                                                  |
| unpickle_pure_python      | 175 us                                                                 | 178 us: 1.02x slower                                                  |
| async_tree_cpu_io_mixed   | 471 ms                                                                 | 479 ms: 1.02x slower                                                  |
| sqlglot_v2_normalize      | 106 ms                                                                 | 108 ms: 1.02x slower                                                  |
| pathlib                   | 17.0 ms                                                                | 17.3 ms: 1.02x slower                                                 |
| many_optionals            | 974 us                                                                 | 991 us: 1.02x slower                                                  |
| 2to3                      | 250 ms                                                                 | 254 ms: 1.02x slower                                                  |
| raytrace                  | 260 ms                                                                 | 265 ms: 1.02x slower                                                  |
| sqlglot_v2_transpile      | 1.48 ms                                                                | 1.51 ms: 1.02x slower                                                 |
| async_tree_memoization_tg | 286 ms                                                                 | 292 ms: 1.02x slower                                                  |
| go                        | 101 ms                                                                 | 103 ms: 1.02x slower                                                  |
| hexiom                    | 6.06 ms                                                                | 6.20 ms: 1.02x slower                                                 |
| chaos                     | 53.0 ms                                                                | 54.2 ms: 1.02x slower                                                 |
| sqlglot_v2_parse          | 1.18 ms                                                                | 1.21 ms: 1.02x slower                                                 |
| sympy_str                 | 303 ms                                                                 | 310 ms: 1.02x slower                                                  |
| subparsers                | 9.09 ms                                                                | 9.34 ms: 1.03x slower                                                 |
| pidigits                  | 192 ms                                                                 | 197 ms: 1.03x slower                                                  |
| sympy_expand              | 502 ms                                                                 | 517 ms: 1.03x slower                                                  |
| meteor_contest            | 97.4 ms                                                                | 100 ms: 1.03x slower                                                  |
| sqlglot_v2_optimize       | 53.4 ms                                                                | 55.2 ms: 1.03x slower                                                 |
| pylint                    | 307 ms                                                                 | 319 ms: 1.04x slower                                                  |
| sympy_integrate           | 20.1 ms                                                                | 20.9 ms: 1.04x slower                                                 |
| sympy_sum                 | 168 ms                                                                 | 176 ms: 1.05x slower                                                  |
| logging_simple            | 5.80 us                                                                | 6.17 us: 1.06x slower                                                 |
| logging_format            | 6.57 us                                                                | 7.00 us: 1.07x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (23): scimark_fft, thrift, json, sqlite_synth, deepcopy_reduce, scimark_lu, genshi_xml, django_template, xml_etree_generate, telco, coroutines, fannkuch, float, deepcopy, docutils, async_tree_memoization, async_tree_io_tg, bench_thread_pool, genshi_text, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 98.89% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x