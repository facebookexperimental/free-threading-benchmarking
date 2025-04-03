# Results vs. base

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.031x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 491 ms                                                                 | 516 ms: 1.05x slower                                                  |
| docutils       | 4.10 sec                                                               | 4.30 sec: 1.05x slower                                                |
| html5lib       | 93.7 ms                                                                | 103 ms: 1.09x slower                                                  |
| sphinx         | 1.56 sec                                                               | 1.61 sec: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets | 788 ms                                                                 | 720 ms: 1.09x faster                                                  |
| coroutines         | 30.2 ms                                                                | 32.5 ms: 1.07x slower                                                 |
| async_tree_none    | 373 ms                                                                 | 404 ms: 1.08x slower                                                  |
| Geometric mean     | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (8): async_tree_io, async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed, async_generators, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 94.1 ms                                                                | 89.0 ms: 1.06x faster                                                 |
| pidigits       | 237 ms                                                                 | 273 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.49 ms                                                                | 4.19 ms: 1.07x faster                                                 |
| regex_v8       | 31.6 ms                                                                | 29.6 ms: 1.07x faster                                                 |
| regex_compile  | 185 ms                                                                 | 222 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_generate   | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| unpickle_pure_python | 308 us                                                                 | 322 us: 1.05x slower                                                  |
| xml_etree_process    | 90.0 ms                                                                | 94.4 ms: 1.05x slower                                                 |
| json_loads           | 39.4 us                                                                | 45.4 us: 1.15x slower                                                 |
| json_dumps           | 15.7 ms                                                                | 18.1 ms: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (4): xml_etree_parse, pickle_pure_python, tomli_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 31.3 ms                                                                | 33.4 ms: 1.07x slower                                                 |
| python_startup_no_site | 22.3 ms                                                                | 24.8 ms: 1.11x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 21.8 ms                                                                | 23.4 ms: 1.07x slower                                                 |
| genshi_xml      | 74.2 ms                                                                | 84.5 ms: 1.14x slower                                                 |
| django_template | 51.0 ms                                                                | 59.6 ms: 1.17x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark              | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| sqlglot_v2_parse       | 2.18 ms                                                                | 1.97 ms: 1.11x faster                                                 |
| asyncio_websockets     | 788 ms                                                                 | 720 ms: 1.09x faster                                                  |
| subparsers             | 37.9 ms                                                                | 35.2 ms: 1.08x faster                                                 |
| regex_effbot           | 4.49 ms                                                                | 4.19 ms: 1.07x faster                                                 |
| regex_v8               | 31.6 ms                                                                | 29.6 ms: 1.07x faster                                                 |
| xml_etree_generate     | 136 ms                                                                 | 127 ms: 1.07x faster                                                  |
| sqlglot_v2_optimize    | 85.6 ms                                                                | 80.4 ms: 1.06x faster                                                 |
| float                  | 94.1 ms                                                                | 89.0 ms: 1.06x faster                                                 |
| mdp                    | 2.25 sec                                                               | 2.31 sec: 1.03x slower                                                |
| fannkuch               | 613 ms                                                                 | 634 ms: 1.03x slower                                                  |
| sphinx                 | 1.56 sec                                                               | 1.61 sec: 1.03x slower                                                |
| pyflate                | 676 ms                                                                 | 706 ms: 1.05x slower                                                  |
| unpickle_pure_python   | 308 us                                                                 | 322 us: 1.05x slower                                                  |
| nqueens                | 116 ms                                                                 | 122 ms: 1.05x slower                                                  |
| generators             | 45.6 ms                                                                | 47.7 ms: 1.05x slower                                                 |
| logging_simple         | 9.38 us                                                                | 9.83 us: 1.05x slower                                                 |
| raytrace               | 406 ms                                                                 | 425 ms: 1.05x slower                                                  |
| xml_etree_process      | 90.0 ms                                                                | 94.4 ms: 1.05x slower                                                 |
| docutils               | 4.10 sec                                                               | 4.30 sec: 1.05x slower                                                |
| 2to3                   | 491 ms                                                                 | 516 ms: 1.05x slower                                                  |
| scimark_monte_carlo    | 102 ms                                                                 | 108 ms: 1.05x slower                                                  |
| telco                  | 11.1 ms                                                                | 11.8 ms: 1.06x slower                                                 |
| sympy_str              | 410 ms                                                                 | 433 ms: 1.06x slower                                                  |
| pprint_pformat         | 2.09 sec                                                               | 2.21 sec: 1.06x slower                                                |
| scimark_sor            | 162 ms                                                                 | 172 ms: 1.06x slower                                                  |
| k_core                 | 4.19 sec                                                               | 4.47 sec: 1.07x slower                                                |
| json                   | 7.61 ms                                                                | 8.12 ms: 1.07x slower                                                 |
| python_startup         | 31.3 ms                                                                | 33.4 ms: 1.07x slower                                                 |
| mako                   | 21.8 ms                                                                | 23.4 ms: 1.07x slower                                                 |
| shortest_path          | 981 ms                                                                 | 1.05 sec: 1.07x slower                                                |
| coroutines             | 30.2 ms                                                                | 32.5 ms: 1.07x slower                                                 |
| pycparser              | 1.51 sec                                                               | 1.63 sec: 1.08x slower                                                |
| scimark_fft            | 468 ms                                                                 | 504 ms: 1.08x slower                                                  |
| spectral_norm          | 140 ms                                                                 | 151 ms: 1.08x slower                                                  |
| connected_components   | 889 ms                                                                 | 959 ms: 1.08x slower                                                  |
| create_gc_cycles       | 2.50 ms                                                                | 2.70 ms: 1.08x slower                                                 |
| async_tree_none        | 373 ms                                                                 | 404 ms: 1.08x slower                                                  |
| comprehensions         | 25.6 us                                                                | 27.7 us: 1.08x slower                                                 |
| html5lib               | 93.7 ms                                                                | 103 ms: 1.09x slower                                                  |
| sqlalchemy_imperative  | 28.2 ms                                                                | 30.9 ms: 1.09x slower                                                 |
| deepcopy_reduce        | 4.01 us                                                                | 4.43 us: 1.10x slower                                                 |
| chaos                  | 91.3 ms                                                                | 101 ms: 1.11x slower                                                  |
| pylint                 | 421 ms                                                                 | 467 ms: 1.11x slower                                                  |
| sqlalchemy_declarative | 210 ms                                                                 | 233 ms: 1.11x slower                                                  |
| python_startup_no_site | 22.3 ms                                                                | 24.8 ms: 1.11x slower                                                 |
| scimark_lu             | 164 ms                                                                 | 183 ms: 1.11x slower                                                  |
| genshi_xml             | 74.2 ms                                                                | 84.5 ms: 1.14x slower                                                 |
| sympy_integrate        | 30.2 ms                                                                | 34.5 ms: 1.14x slower                                                 |
| deltablue              | 5.08 ms                                                                | 5.81 ms: 1.14x slower                                                 |
| bench_mp_pool          | 85.9 ms                                                                | 98.5 ms: 1.15x slower                                                 |
| pidigits               | 237 ms                                                                 | 273 ms: 1.15x slower                                                  |
| json_loads             | 39.4 us                                                                | 45.4 us: 1.15x slower                                                 |
| json_dumps             | 15.7 ms                                                                | 18.1 ms: 1.15x slower                                                 |
| go                     | 163 ms                                                                 | 190 ms: 1.17x slower                                                  |
| django_template        | 51.0 ms                                                                | 59.6 ms: 1.17x slower                                                 |
| dulwich_log            | 84.2 ms                                                                | 98.7 ms: 1.17x slower                                                 |
| gc_traversal           | 3.45 ms                                                                | 4.07 ms: 1.18x slower                                                 |
| regex_compile          | 185 ms                                                                 | 222 ms: 1.20x slower                                                  |
| bench_thread_pool      | 3.75 ms                                                                | 5.16 ms: 1.38x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (36): crypto_pyaes, sqlglot_v2_transpile, xml_etree_parse, richards, sqlite_synth, nbody, hexiom, regex_dna, async_tree_io, genshi_text, typing_runtime_protocols, async_tree_memoization, pprint_safe_repr, logging_silent, deepcopy_memo, async_tree_io_tg, pickle_pure_python, async_tree_cpu_io_mixed, bpe_tokeniser, async_generators, meteor_contest, scimark_sparse_mat_mult, async_tree_memoization_tg, logging_format, tomli_loads, deepcopy, async_tree_none_tg, xml_etree_iterparse, pathlib, richards_super, sympy_sum, sqlglot_v2_normalize, coverage, async_tree_cpu_io_mixed_tg, sympy_expand, many_optionals

- Geometric mean (including insignificant results): 1.031x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.01x