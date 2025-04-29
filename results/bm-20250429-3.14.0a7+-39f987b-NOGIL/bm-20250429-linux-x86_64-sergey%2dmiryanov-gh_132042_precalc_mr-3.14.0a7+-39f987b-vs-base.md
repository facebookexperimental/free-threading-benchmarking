# Results vs. base

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.004x slower
- HPT reliability: 90.14%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 420 ms                                                                 | 425 ms: 1.01x slower                                                              |
| docutils       | 3.97 sec                                                               | 3.92 sec: 1.01x faster                                                            |
| sphinx         | 1.55 sec                                                               | 1.60 sec: 1.03x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                      |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| coroutines                 | 30.7 ms                                                                | 29.7 ms: 1.03x faster                                                             |
| asyncio_websockets         | 701 ms                                                                 | 690 ms: 1.02x faster                                                              |
| async_tree_cpu_io_mixed_tg | 588 ms                                                                 | 595 ms: 1.01x slower                                                              |
| async_tree_memoization_tg  | 396 ms                                                                 | 403 ms: 1.02x slower                                                              |
| async_tree_io_tg           | 680 ms                                                                 | 708 ms: 1.04x slower                                                              |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                                      |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, async_generators, async_tree_none_tg, async_tree_io, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 91.8 ms                                                                | 90.6 ms: 1.01x faster                                                             |
| pidigits       | 222 ms                                                                 | 219 ms: 1.01x faster                                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                      |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_effbot   | 3.74 ms                                                                | 3.66 ms: 1.02x faster                                                             |
| regex_compile  | 185 ms                                                                 | 182 ms: 1.02x faster                                                              |
| regex_dna      | 245 ms                                                                 | 251 ms: 1.02x slower                                                              |
| regex_v8       | 26.2 ms                                                                | 29.1 ms: 1.11x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 144 ms                                                                 | 134 ms: 1.08x faster                                                              |
| unpickle_pure_python | 312 us                                                                 | 305 us: 1.02x faster                                                              |
| xml_etree_process    | 97.1 ms                                                                | 95.0 ms: 1.02x faster                                                             |
| json_loads           | 40.7 us                                                                | 42.1 us: 1.03x slower                                                             |
| tomli_loads          | 2.81 sec                                                               | 2.92 sec: 1.04x slower                                                            |
| xml_etree_generate   | 134 ms                                                                 | 139 ms: 1.04x slower                                                              |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                      |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 25.2 ms                                                                | 25.9 ms: 1.03x slower                                                             |
| python_startup_no_site | 15.0 ms                                                                | 15.5 ms: 1.03x slower                                                             |
| Geometric mean         | (ref)                                                                  | 1.03x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_text    | 34.2 ms                                                                | 34.6 ms: 1.01x slower                                                             |
| mako           | 21.6 ms                                                                | 21.9 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                      |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_iterparse        | 144 ms                                                                 | 134 ms: 1.08x faster                                                              |
| spectral_norm              | 143 ms                                                                 | 133 ms: 1.07x faster                                                              |
| scimark_sparse_mat_mult    | 7.04 ms                                                                | 6.63 ms: 1.06x faster                                                             |
| gc_traversal               | 4.31 ms                                                                | 4.08 ms: 1.06x faster                                                             |
| chaos                      | 82.9 ms                                                                | 79.6 ms: 1.04x faster                                                             |
| coroutines                 | 30.7 ms                                                                | 29.7 ms: 1.03x faster                                                             |
| create_gc_cycles           | 2.83 ms                                                                | 2.73 ms: 1.03x faster                                                             |
| scimark_fft                | 478 ms                                                                 | 464 ms: 1.03x faster                                                              |
| unpickle_pure_python       | 312 us                                                                 | 305 us: 1.02x faster                                                              |
| pathlib                    | 26.6 ms                                                                | 26.0 ms: 1.02x faster                                                             |
| xml_etree_process          | 97.1 ms                                                                | 95.0 ms: 1.02x faster                                                             |
| regex_effbot               | 3.74 ms                                                                | 3.66 ms: 1.02x faster                                                             |
| crypto_pyaes               | 112 ms                                                                 | 110 ms: 1.02x faster                                                              |
| nqueens                    | 114 ms                                                                 | 112 ms: 1.02x faster                                                              |
| scimark_lu                 | 170 ms                                                                 | 167 ms: 1.02x faster                                                              |
| fannkuch                   | 611 ms                                                                 | 599 ms: 1.02x faster                                                              |
| regex_compile              | 185 ms                                                                 | 182 ms: 1.02x faster                                                              |
| asyncio_websockets         | 701 ms                                                                 | 690 ms: 1.02x faster                                                              |
| k_core                     | 4.14 sec                                                               | 4.08 sec: 1.02x faster                                                            |
| bpe_tokeniser              | 7.52 sec                                                               | 7.42 sec: 1.01x faster                                                            |
| float                      | 91.8 ms                                                                | 90.6 ms: 1.01x faster                                                             |
| pidigits                   | 222 ms                                                                 | 219 ms: 1.01x faster                                                              |
| connected_components       | 887 ms                                                                 | 876 ms: 1.01x faster                                                              |
| scimark_monte_carlo        | 100 ms                                                                 | 98.8 ms: 1.01x faster                                                             |
| docutils                   | 3.97 sec                                                               | 3.92 sec: 1.01x faster                                                            |
| dulwich_log                | 80.8 ms                                                                | 79.9 ms: 1.01x faster                                                             |
| json                       | 7.15 ms                                                                | 7.10 ms: 1.01x faster                                                             |
| 2to3                       | 420 ms                                                                 | 425 ms: 1.01x slower                                                              |
| subparsers                 | 33.0 ms                                                                | 33.3 ms: 1.01x slower                                                             |
| genshi_text                | 34.2 ms                                                                | 34.6 ms: 1.01x slower                                                             |
| async_tree_cpu_io_mixed_tg | 588 ms                                                                 | 595 ms: 1.01x slower                                                              |
| richards_super             | 77.8 ms                                                                | 78.9 ms: 1.01x slower                                                             |
| mako                       | 21.6 ms                                                                | 21.9 ms: 1.01x slower                                                             |
| scimark_sor                | 156 ms                                                                 | 159 ms: 1.02x slower                                                              |
| sympy_expand               | 668 ms                                                                 | 680 ms: 1.02x slower                                                              |
| async_tree_memoization_tg  | 396 ms                                                                 | 403 ms: 1.02x slower                                                              |
| deepcopy_reduce            | 3.87 us                                                                | 3.96 us: 1.02x slower                                                             |
| deltablue                  | 4.75 ms                                                                | 4.86 ms: 1.02x slower                                                             |
| go                         | 163 ms                                                                 | 167 ms: 1.02x slower                                                              |
| regex_dna                  | 245 ms                                                                 | 251 ms: 1.02x slower                                                              |
| python_startup             | 25.2 ms                                                                | 25.9 ms: 1.03x slower                                                             |
| python_startup_no_site     | 15.0 ms                                                                | 15.5 ms: 1.03x slower                                                             |
| comprehensions             | 25.1 us                                                                | 25.8 us: 1.03x slower                                                             |
| deepcopy                   | 369 us                                                                 | 379 us: 1.03x slower                                                              |
| sphinx                     | 1.55 sec                                                               | 1.60 sec: 1.03x slower                                                            |
| logging_simple             | 8.67 us                                                                | 8.95 us: 1.03x slower                                                             |
| telco                      | 10.4 ms                                                                | 10.8 ms: 1.03x slower                                                             |
| json_loads                 | 40.7 us                                                                | 42.1 us: 1.03x slower                                                             |
| sqlglot_v2_normalize       | 145 ms                                                                 | 150 ms: 1.04x slower                                                              |
| tomli_loads                | 2.81 sec                                                               | 2.92 sec: 1.04x slower                                                            |
| xml_etree_generate         | 134 ms                                                                 | 139 ms: 1.04x slower                                                              |
| pprint_pformat             | 2.09 sec                                                               | 2.17 sec: 1.04x slower                                                            |
| async_tree_io_tg           | 680 ms                                                                 | 708 ms: 1.04x slower                                                              |
| pprint_safe_repr           | 1.01 sec                                                               | 1.05 sec: 1.04x slower                                                            |
| sqlglot_v2_parse           | 1.96 ms                                                                | 2.04 ms: 1.04x slower                                                             |
| richards                   | 66.0 ms                                                                | 69.5 ms: 1.05x slower                                                             |
| logging_format             | 9.79 us                                                                | 10.3 us: 1.05x slower                                                             |
| hexiom                     | 8.77 ms                                                                | 9.32 ms: 1.06x slower                                                             |
| thrift                     | 1.09 ms                                                                | 1.16 ms: 1.06x slower                                                             |
| sqlglot_v2_optimize        | 77.0 ms                                                                | 83.1 ms: 1.08x slower                                                             |
| logging_silent             | 128 ns                                                                 | 140 ns: 1.09x slower                                                              |
| regex_v8                   | 26.2 ms                                                                | 29.1 ms: 1.11x slower                                                             |
| generators                 | 42.4 ms                                                                | 47.3 ms: 1.12x slower                                                             |
| bench_thread_pool          | 2.64 ms                                                                | 3.00 ms: 1.14x slower                                                             |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                                      |

Benchmark hidden because not significant (30): sympy_integrate, xml_etree_parse, sympy_sum, deepcopy_memo, html5lib, sqlite_synth, django_template, many_optionals, async_tree_cpu_io_mixed, sqlglot_v2_transpile, pickle_pure_python, coverage, json_dumps, shortest_path, async_generators, pycparser, async_tree_none_tg, raytrace, async_tree_io, meteor_contest, nbody, async_tree_none, pylint, genshi_xml, pyflate, sympy_str, mdp, async_tree_memoization, typing_runtime_protocols, bench_mp_pool

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 90.14% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x