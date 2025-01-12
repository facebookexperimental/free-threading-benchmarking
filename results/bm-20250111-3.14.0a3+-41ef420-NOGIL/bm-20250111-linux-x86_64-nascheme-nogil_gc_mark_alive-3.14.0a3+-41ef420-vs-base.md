# Results vs. base

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: 41ef420
- commit date: 2025-01-11
- overall geometric mean: 1.049x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 614 ms                                                                 | 660 ms: 1.07x slower                                                    |
| docutils       | 4.46 sec                                                               | 4.79 sec: 1.07x slower                                                  |
| sphinx         | 1.73 sec                                                               | 1.87 sec: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg        | 412 ms                                                                 | 445 ms: 1.08x slower                                                    |
| async_tree_memoization_tg | 593 ms                                                                 | 645 ms: 1.09x slower                                                    |
| async_generators          | 625 ms                                                                 | 681 ms: 1.09x slower                                                    |
| coroutines                | 34.7 ms                                                                | 38.7 ms: 1.11x slower                                                   |
| asyncio_websockets        | 714 ms                                                                 | 827 ms: 1.16x slower                                                    |
| async_tree_io             | 966 ms                                                                 | 1.12 sec: 1.16x slower                                                  |
| async_tree_memoization    | 604 ms                                                                 | 705 ms: 1.17x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.09x slower                                                            |

Benchmark hidden because not significant (4): async_tree_io_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 244 ms                                                                 | 236 ms: 1.04x faster                                                    |
| float          | 137 ms                                                                 | 151 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 210 ms                                                                 | 256 ms: 1.22x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmark hidden because not significant (3): regex_v8, regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 229 ms                                                                 | 206 ms: 1.11x faster                                                    |
| pickle_pure_python   | 643 us                                                                 | 615 us: 1.05x faster                                                    |
| unpickle_pure_python | 445 us                                                                 | 475 us: 1.07x slower                                                    |
| xml_etree_process    | 100 ms                                                                 | 108 ms: 1.08x slower                                                    |
| tomli_loads          | 2.93 sec                                                               | 3.20 sec: 1.09x slower                                                  |
| json_dumps           | 16.3 ms                                                                | 18.0 ms: 1.10x slower                                                   |
| json_loads           | 38.7 us                                                                | 43.1 us: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 30.6 ms                                                                | 36.2 ms: 1.18x slower                                                   |
| python_startup_no_site | 20.0 ms                                                                | 26.0 ms: 1.30x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.24x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 27.1 ms                                                                | 25.5 ms: 1.06x faster                                                   |
| django_template | 59.7 ms                                                                | 65.3 ms: 1.09x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| create_gc_cycles          | 4.47 ms                                                                | 3.45 ms: 1.29x faster                                                   |
| xml_etree_parse           | 229 ms                                                                 | 206 ms: 1.11x faster                                                    |
| sqlite_synth              | 4.21 us                                                                | 3.82 us: 1.10x faster                                                   |
| logging_silent            | 237 ns                                                                 | 222 ns: 1.07x faster                                                    |
| mako                      | 27.1 ms                                                                | 25.5 ms: 1.06x faster                                                   |
| pickle_pure_python        | 643 us                                                                 | 615 us: 1.05x faster                                                    |
| pidigits                  | 244 ms                                                                 | 236 ms: 1.04x faster                                                    |
| richards                  | 79.9 ms                                                                | 83.0 ms: 1.04x slower                                                   |
| hexiom                    | 13.0 ms                                                                | 13.8 ms: 1.06x slower                                                   |
| scimark_fft               | 518 ms                                                                 | 549 ms: 1.06x slower                                                    |
| scimark_monte_carlo       | 140 ms                                                                 | 148 ms: 1.06x slower                                                    |
| unpickle_pure_python      | 445 us                                                                 | 475 us: 1.07x slower                                                    |
| fannkuch                  | 639 ms                                                                 | 684 ms: 1.07x slower                                                    |
| crypto_pyaes              | 124 ms                                                                 | 133 ms: 1.07x slower                                                    |
| 2to3                      | 614 ms                                                                 | 660 ms: 1.07x slower                                                    |
| docutils                  | 4.46 sec                                                               | 4.79 sec: 1.07x slower                                                  |
| pycparser                 | 1.73 sec                                                               | 1.86 sec: 1.08x slower                                                  |
| dulwich_log               | 111 ms                                                                 | 119 ms: 1.08x slower                                                    |
| sympy_integrate           | 37.0 ms                                                                | 39.8 ms: 1.08x slower                                                   |
| sqlalchemy_imperative     | 36.3 ms                                                                | 39.1 ms: 1.08x slower                                                   |
| sphinx                    | 1.73 sec                                                               | 1.87 sec: 1.08x slower                                                  |
| xml_etree_process         | 100 ms                                                                 | 108 ms: 1.08x slower                                                    |
| sympy_sum                 | 272 ms                                                                 | 293 ms: 1.08x slower                                                    |
| async_tree_none_tg        | 412 ms                                                                 | 445 ms: 1.08x slower                                                    |
| deepcopy                  | 414 us                                                                 | 449 us: 1.08x slower                                                    |
| pprint_pformat            | 2.61 sec                                                               | 2.83 sec: 1.09x slower                                                  |
| async_tree_memoization_tg | 593 ms                                                                 | 645 ms: 1.09x slower                                                    |
| pathlib                   | 30.7 ms                                                                | 33.5 ms: 1.09x slower                                                   |
| async_generators          | 625 ms                                                                 | 681 ms: 1.09x slower                                                    |
| tomli_loads               | 2.93 sec                                                               | 3.20 sec: 1.09x slower                                                  |
| django_template           | 59.7 ms                                                                | 65.3 ms: 1.09x slower                                                   |
| deltablue                 | 9.66 ms                                                                | 10.6 ms: 1.09x slower                                                   |
| bench_mp_pool             | 88.0 ms                                                                | 96.3 ms: 1.09x slower                                                   |
| thrift                    | 1.46 ms                                                                | 1.60 ms: 1.09x slower                                                   |
| float                     | 137 ms                                                                 | 151 ms: 1.10x slower                                                    |
| chaos                     | 119 ms                                                                 | 131 ms: 1.10x slower                                                    |
| json_dumps                | 16.3 ms                                                                | 18.0 ms: 1.10x slower                                                   |
| deepcopy_memo             | 52.0 us                                                                | 57.4 us: 1.11x slower                                                   |
| sqlglot_normalize         | 163 ms                                                                 | 180 ms: 1.11x slower                                                    |
| json_loads                | 38.7 us                                                                | 43.1 us: 1.11x slower                                                   |
| coroutines                | 34.7 ms                                                                | 38.7 ms: 1.11x slower                                                   |
| generators                | 51.5 ms                                                                | 57.7 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult   | 8.37 ms                                                                | 9.40 ms: 1.12x slower                                                   |
| shortest_path             | 1.04 sec                                                               | 1.17 sec: 1.12x slower                                                  |
| comprehensions            | 35.3 us                                                                | 39.7 us: 1.13x slower                                                   |
| deepcopy_reduce           | 4.33 us                                                                | 4.89 us: 1.13x slower                                                   |
| bench_thread_pool         | 4.59 ms                                                                | 5.23 ms: 1.14x slower                                                   |
| mdp                       | 4.24 sec                                                               | 4.89 sec: 1.15x slower                                                  |
| raytrace                  | 570 ms                                                                 | 659 ms: 1.16x slower                                                    |
| sqlalchemy_declarative    | 249 ms                                                                 | 289 ms: 1.16x slower                                                    |
| asyncio_websockets        | 714 ms                                                                 | 827 ms: 1.16x slower                                                    |
| bpe_tokeniser             | 7.57 sec                                                               | 8.78 sec: 1.16x slower                                                  |
| async_tree_io             | 966 ms                                                                 | 1.12 sec: 1.16x slower                                                  |
| async_tree_memoization    | 604 ms                                                                 | 705 ms: 1.17x slower                                                    |
| logging_simple            | 10.5 us                                                                | 12.4 us: 1.17x slower                                                   |
| pprint_safe_repr          | 1.19 sec                                                               | 1.40 sec: 1.17x slower                                                  |
| sympy_str                 | 433 ms                                                                 | 513 ms: 1.18x slower                                                    |
| python_startup            | 30.6 ms                                                                | 36.2 ms: 1.18x slower                                                   |
| sqlglot_optimize          | 82.8 ms                                                                | 98.4 ms: 1.19x slower                                                   |
| richards_super            | 97.0 ms                                                                | 116 ms: 1.20x slower                                                    |
| many_optionals            | 1.44 ms                                                                | 1.74 ms: 1.20x slower                                                   |
| typing_runtime_protocols  | 271 us                                                                 | 326 us: 1.20x slower                                                    |
| regex_compile             | 210 ms                                                                 | 256 ms: 1.22x slower                                                    |
| subparsers                | 45.4 ms                                                                | 56.7 ms: 1.25x slower                                                   |
| python_startup_no_site    | 20.0 ms                                                                | 26.0 ms: 1.30x slower                                                   |
| Geometric mean            | (ref)                                                                  | 1.06x slower                                                            |

Benchmark hidden because not significant (31): gc_traversal, regex_v8, xml_etree_iterparse, genshi_xml, json, pylint, nqueens, telco, connected_components, go, logging_format, nbody, coverage, regex_effbot, pyflate, genshi_text, meteor_contest, sqlglot_transpile, k_core, async_tree_io_tg, sqlglot_parse, scimark_lu, sympy_expand, html5lib, regex_dna, async_tree_none, async_tree_cpu_io_mixed, scimark_sor, async_tree_cpu_io_mixed_tg, spectral_norm, xml_etree_generate

- Geometric mean (including insignificant results): 1.049x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.00x