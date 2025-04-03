# Results vs. base

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.002x slower
- HPT reliability: 95.62%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 255 ms: 1.00x faster                                                  |
| docutils       | 2.59 sec                                                               | 2.62 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators       | 340 ms                                                                 | 338 ms: 1.01x faster                                                  |
| async_tree_memoization | 324 ms                                                                 | 327 ms: 1.01x slower                                                  |
| async_tree_io          | 629 ms                                                                 | 636 ms: 1.01x slower                                                  |
| async_tree_none        | 283 ms                                                                 | 287 ms: 1.01x slower                                                  |
| coroutines             | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 71.6 ms                                                                | 72.4 ms: 1.01x slower                                                 |
| nbody          | 94.7 ms                                                                | 95.9 ms: 1.01x slower                                                 |
| pidigits       | 198 ms                                                                 | 206 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                | 21.6 ms: 1.02x faster                                                 |
| regex_compile  | 132 ms                                                                 | 132 ms: 1.00x faster                                                  |
| regex_dna      | 172 ms                                                                 | 173 ms: 1.01x slower                                                  |
| regex_effbot   | 2.68 ms                                                                | 2.77 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads        | 2.03 sec                                                               | 2.00 sec: 1.02x faster                                                |
| pickle_pure_python | 319 us                                                                 | 317 us: 1.01x faster                                                  |
| xml_etree_process  | 61.3 ms                                                                | 61.7 ms: 1.01x slower                                                 |
| xml_etree_parse    | 129 ms                                                                 | 131 ms: 1.01x slower                                                  |
| json_loads         | 27.1 us                                                                | 27.5 us: 1.02x slower                                                 |
| Geometric mean     | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (4): unpickle_pure_python, xml_etree_generate, xml_etree_iterparse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 8.71 ms                                                                | 8.65 ms: 1.01x faster                                                 |
| python_startup         | 15.1 ms                                                                | 15.1 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.3 ms                                                                | 21.8 ms: 1.02x faster                                                 |
| genshi_xml     | 51.3 ms                                                                | 50.3 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark               | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| generators              | 31.1 ms                                                                | 29.6 ms: 1.05x faster                                                 |
| scimark_lu              | 119 ms                                                                 | 116 ms: 1.03x faster                                                  |
| scimark_sparse_mat_mult | 4.61 ms                                                                | 4.51 ms: 1.02x faster                                                 |
| genshi_text             | 22.3 ms                                                                | 21.8 ms: 1.02x faster                                                 |
| genshi_xml              | 51.3 ms                                                                | 50.3 ms: 1.02x faster                                                 |
| pathlib                 | 19.8 ms                                                                | 19.4 ms: 1.02x faster                                                 |
| regex_v8                | 22.0 ms                                                                | 21.6 ms: 1.02x faster                                                 |
| tomli_loads             | 2.03 sec                                                               | 2.00 sec: 1.02x faster                                                |
| richards                | 44.6 ms                                                                | 44.0 ms: 1.01x faster                                                 |
| scimark_monte_carlo     | 63.5 ms                                                                | 62.6 ms: 1.01x faster                                                 |
| deepcopy_reduce         | 2.73 us                                                                | 2.71 us: 1.01x faster                                                 |
| logging_silent          | 102 ns                                                                 | 101 ns: 1.01x faster                                                  |
| crypto_pyaes            | 70.2 ms                                                                | 69.6 ms: 1.01x faster                                                 |
| async_generators        | 340 ms                                                                 | 338 ms: 1.01x faster                                                  |
| richards_super          | 50.7 ms                                                                | 50.3 ms: 1.01x faster                                                 |
| python_startup_no_site  | 8.71 ms                                                                | 8.65 ms: 1.01x faster                                                 |
| pickle_pure_python      | 319 us                                                                 | 317 us: 1.01x faster                                                  |
| sqlalchemy_imperative   | 20.5 ms                                                                | 20.4 ms: 1.01x faster                                                 |
| comprehensions          | 17.4 us                                                                | 17.3 us: 1.00x faster                                                 |
| python_startup          | 15.1 ms                                                                | 15.1 ms: 1.00x faster                                                 |
| sqlglot_v2_normalize    | 109 ms                                                                 | 109 ms: 1.00x faster                                                  |
| regex_compile           | 132 ms                                                                 | 132 ms: 1.00x faster                                                  |
| 2to3                    | 256 ms                                                                 | 255 ms: 1.00x faster                                                  |
| sqlglot_v2_optimize     | 54.3 ms                                                                | 54.2 ms: 1.00x faster                                                 |
| sqlalchemy_declarative  | 133 ms                                                                 | 133 ms: 1.00x slower                                                  |
| scimark_sor             | 116 ms                                                                 | 116 ms: 1.00x slower                                                  |
| many_optionals          | 1.05 ms                                                                | 1.05 ms: 1.01x slower                                                 |
| hexiom                  | 6.18 ms                                                                | 6.21 ms: 1.01x slower                                                 |
| go                      | 116 ms                                                                 | 117 ms: 1.01x slower                                                  |
| regex_dna               | 172 ms                                                                 | 173 ms: 1.01x slower                                                  |
| deepcopy_memo           | 30.0 us                                                                | 30.2 us: 1.01x slower                                                 |
| xml_etree_process       | 61.3 ms                                                                | 61.7 ms: 1.01x slower                                                 |
| pprint_safe_repr        | 738 ms                                                                 | 743 ms: 1.01x slower                                                  |
| subparsers              | 22.9 ms                                                                | 23.1 ms: 1.01x slower                                                 |
| async_tree_memoization  | 324 ms                                                                 | 327 ms: 1.01x slower                                                  |
| bench_thread_pool       | 1.06 ms                                                                | 1.07 ms: 1.01x slower                                                 |
| docutils                | 2.59 sec                                                               | 2.62 sec: 1.01x slower                                                |
| nqueens                 | 81.7 ms                                                                | 82.5 ms: 1.01x slower                                                 |
| async_tree_io           | 629 ms                                                                 | 636 ms: 1.01x slower                                                  |
| logging_simple          | 6.23 us                                                                | 6.30 us: 1.01x slower                                                 |
| async_tree_none         | 283 ms                                                                 | 287 ms: 1.01x slower                                                  |
| raytrace                | 260 ms                                                                 | 263 ms: 1.01x slower                                                  |
| float                   | 71.6 ms                                                                | 72.4 ms: 1.01x slower                                                 |
| fannkuch                | 393 ms                                                                 | 398 ms: 1.01x slower                                                  |
| xml_etree_parse         | 129 ms                                                                 | 131 ms: 1.01x slower                                                  |
| pprint_pformat          | 1.51 sec                                                               | 1.52 sec: 1.01x slower                                                |
| nbody                   | 94.7 ms                                                                | 95.9 ms: 1.01x slower                                                 |
| scimark_fft             | 326 ms                                                                 | 331 ms: 1.02x slower                                                  |
| json                    | 4.85 ms                                                                | 4.93 ms: 1.02x slower                                                 |
| chaos                   | 56.3 ms                                                                | 57.2 ms: 1.02x slower                                                 |
| json_loads              | 27.1 us                                                                | 27.5 us: 1.02x slower                                                 |
| logging_format          | 6.91 us                                                                | 7.04 us: 1.02x slower                                                 |
| spectral_norm           | 97.5 ms                                                                | 99.4 ms: 1.02x slower                                                 |
| deltablue               | 3.34 ms                                                                | 3.41 ms: 1.02x slower                                                 |
| coroutines              | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| regex_effbot            | 2.68 ms                                                                | 2.77 ms: 1.03x slower                                                 |
| pidigits                | 198 ms                                                                 | 206 ms: 1.04x slower                                                  |
| gc_traversal            | 4.21 ms                                                                | 4.49 ms: 1.06x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (36): connected_components, async_tree_memoization_tg, async_tree_cpu_io_mixed, unpickle_pure_python, async_tree_none_tg, create_gc_cycles, telco, k_core, sqlglot_v2_parse, sympy_integrate, shortest_path, pycparser, pylint, bpe_tokeniser, bench_mp_pool, async_tree_cpu_io_mixed_tg, dulwich_log, typing_runtime_protocols, asyncio_websockets, sympy_sum, deepcopy, sympy_str, sympy_expand, mdp, pyflate, mako, django_template, xml_etree_generate, sqlite_synth, xml_etree_iterparse, json_dumps, meteor_contest, sqlglot_v2_transpile, coverage, sphinx, async_tree_io_tg

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 95.62% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x