# Results vs. base

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.013x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 443 ms                                                                 | 474 ms: 1.07x slower                                                  |
| docutils       | 3.57 sec                                                               | 3.68 sec: 1.03x slower                                                |
| sphinx         | 1.42 sec                                                               | 1.53 sec: 1.08x slower                                                |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 880 ms                                                                 | 909 ms: 1.03x slower                                                  |
| async_tree_memoization     | 449 ms                                                                 | 465 ms: 1.04x slower                                                  |
| async_tree_none            | 365 ms                                                                 | 379 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed_tg | 664 ms                                                                 | 691 ms: 1.04x slower                                                  |
| async_tree_none_tg         | 351 ms                                                                 | 366 ms: 1.04x slower                                                  |
| async_tree_memoization_tg  | 478 ms                                                                 | 508 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (5): coroutines, async_generators, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 92.9 ms                                                                | 96.4 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 162 ms                                                                 | 171 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): regex_effbot, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 238 ms                                                                 | 205 ms: 1.16x faster                                                  |
| tomli_loads          | 2.49 sec                                                               | 2.58 sec: 1.04x slower                                                |
| unpickle_pure_python | 272 us                                                                 | 295 us: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (6): xml_etree_generate, xml_etree_iterparse, json_loads, xml_etree_process, pickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.7 ms                                                                | 17.9 ms: 1.07x slower                                                 |
| python_startup         | 29.4 ms                                                                | 32.6 ms: 1.11x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 17.3 ms                                                                | 15.6 ms: 1.11x faster                                                 |
| genshi_xml     | 61.9 ms                                                                | 64.4 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 249 us                                                                 | 209 us: 1.19x faster                                                  |
| xml_etree_parse            | 238 ms                                                                 | 205 ms: 1.16x faster                                                  |
| mako                       | 17.3 ms                                                                | 15.6 ms: 1.11x faster                                                 |
| sqlglot_v2_normalize       | 152 ms                                                                 | 138 ms: 1.10x faster                                                  |
| telco                      | 11.2 ms                                                                | 10.4 ms: 1.08x faster                                                 |
| many_optionals             | 1.27 ms                                                                | 1.18 ms: 1.07x faster                                                 |
| pathlib                    | 30.9 ms                                                                | 29.1 ms: 1.06x faster                                                 |
| sympy_sum                  | 217 ms                                                                 | 205 ms: 1.06x faster                                                  |
| sympy_str                  | 378 ms                                                                 | 361 ms: 1.05x faster                                                  |
| scimark_monte_carlo        | 88.9 ms                                                                | 85.0 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 5.78 sec                                                               | 5.96 sec: 1.03x slower                                                |
| docutils                   | 3.57 sec                                                               | 3.68 sec: 1.03x slower                                                |
| sympy_expand               | 601 ms                                                                 | 620 ms: 1.03x slower                                                  |
| async_tree_io_tg           | 880 ms                                                                 | 909 ms: 1.03x slower                                                  |
| tomli_loads                | 2.49 sec                                                               | 2.58 sec: 1.04x slower                                                |
| async_tree_memoization     | 449 ms                                                                 | 465 ms: 1.04x slower                                                  |
| float                      | 92.9 ms                                                                | 96.4 ms: 1.04x slower                                                 |
| gc_traversal               | 7.84 ms                                                                | 8.14 ms: 1.04x slower                                                 |
| json                       | 6.71 ms                                                                | 6.97 ms: 1.04x slower                                                 |
| async_tree_none            | 365 ms                                                                 | 379 ms: 1.04x slower                                                  |
| genshi_xml                 | 61.9 ms                                                                | 64.4 ms: 1.04x slower                                                 |
| async_tree_cpu_io_mixed_tg | 664 ms                                                                 | 691 ms: 1.04x slower                                                  |
| async_tree_none_tg         | 351 ms                                                                 | 366 ms: 1.04x slower                                                  |
| mdp                        | 1.79 sec                                                               | 1.87 sec: 1.05x slower                                                |
| deepcopy_reduce            | 3.27 us                                                                | 3.43 us: 1.05x slower                                                 |
| pprint_safe_repr           | 924 ms                                                                 | 970 ms: 1.05x slower                                                  |
| chaos                      | 74.1 ms                                                                | 77.9 ms: 1.05x slower                                                 |
| coverage                   | 105 ms                                                                 | 111 ms: 1.05x slower                                                  |
| regex_compile              | 162 ms                                                                 | 171 ms: 1.06x slower                                                  |
| async_tree_memoization_tg  | 478 ms                                                                 | 508 ms: 1.06x slower                                                  |
| pycparser                  | 1.52 sec                                                               | 1.62 sec: 1.07x slower                                                |
| deepcopy                   | 315 us                                                                 | 337 us: 1.07x slower                                                  |
| 2to3                       | 443 ms                                                                 | 474 ms: 1.07x slower                                                  |
| python_startup_no_site     | 16.7 ms                                                                | 17.9 ms: 1.07x slower                                                 |
| scimark_sparse_mat_mult    | 5.88 ms                                                                | 6.30 ms: 1.07x slower                                                 |
| deltablue                  | 4.34 ms                                                                | 4.65 ms: 1.07x slower                                                 |
| sphinx                     | 1.42 sec                                                               | 1.53 sec: 1.08x slower                                                |
| richards_super             | 65.7 ms                                                                | 71.4 ms: 1.09x slower                                                 |
| unpickle_pure_python       | 272 us                                                                 | 295 us: 1.09x slower                                                  |
| pprint_pformat             | 1.84 sec                                                               | 2.00 sec: 1.09x slower                                                |
| shortest_path              | 861 ms                                                                 | 936 ms: 1.09x slower                                                  |
| bench_mp_pool              | 88.1 ms                                                                | 95.9 ms: 1.09x slower                                                 |
| logging_format             | 8.76 us                                                                | 9.56 us: 1.09x slower                                                 |
| subparsers                 | 28.6 ms                                                                | 31.2 ms: 1.09x slower                                                 |
| connected_components       | 769 ms                                                                 | 843 ms: 1.10x slower                                                  |
| sqlalchemy_declarative     | 169 ms                                                                 | 186 ms: 1.10x slower                                                  |
| create_gc_cycles           | 3.34 ms                                                                | 3.69 ms: 1.11x slower                                                 |
| python_startup             | 29.4 ms                                                                | 32.6 ms: 1.11x slower                                                 |
| meteor_contest             | 131 ms                                                                 | 146 ms: 1.11x slower                                                  |
| k_core                     | 3.95 sec                                                               | 4.43 sec: 1.12x slower                                                |
| bench_thread_pool          | 2.96 ms                                                                | 3.62 ms: 1.22x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (43): xml_etree_generate, raytrace, regex_effbot, nqueens, xml_etree_iterparse, sqlalchemy_imperative, richards, regex_dna, scimark_fft, scimark_lu, coroutines, async_generators, json_loads, dulwich_log, genshi_text, comprehensions, asyncio_websockets, nbody, logging_silent, async_tree_cpu_io_mixed, sqlite_synth, sympy_integrate, scimark_sor, go, sqlglot_v2_optimize, xml_etree_process, fannkuch, deepcopy_memo, sqlglot_v2_parse, hexiom, django_template, crypto_pyaes, pyflate, generators, pidigits, regex_v8, spectral_norm, async_tree_io, sqlglot_v2_transpile, pickle_pure_python, json_dumps, logging_simple, pylint

- Geometric mean (including insignificant results): 1.013x slower

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.00x