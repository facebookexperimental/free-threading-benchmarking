# Results vs. base

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.007x faster
- HPT reliability: 98.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 385 ms                                                                 | 362 ms: 1.06x faster                                                              |
| docutils       | 3.67 sec                                                               | 3.62 sec: 1.01x faster                                                            |
| sphinx         | 1.43 sec                                                               | 1.37 sec: 1.04x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                                      |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_memoization     | 462 ms                                                                 | 432 ms: 1.07x faster                                                              |
| async_tree_cpu_io_mixed    | 695 ms                                                                 | 654 ms: 1.06x faster                                                              |
| async_generators           | 519 ms                                                                 | 488 ms: 1.06x faster                                                              |
| asyncio_websockets         | 697 ms                                                                 | 667 ms: 1.04x faster                                                              |
| async_tree_io              | 859 ms                                                                 | 823 ms: 1.04x faster                                                              |
| async_tree_cpu_io_mixed_tg | 668 ms                                                                 | 644 ms: 1.04x faster                                                              |
| async_tree_none            | 373 ms                                                                 | 360 ms: 1.04x faster                                                              |
| async_tree_none_tg         | 355 ms                                                                 | 344 ms: 1.03x faster                                                              |
| async_tree_memoization_tg  | 460 ms                                                                 | 449 ms: 1.02x faster                                                              |
| coroutines                 | 29.8 ms                                                                | 30.2 ms: 1.01x slower                                                             |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                                      |

Benchmark hidden because not significant (1): async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| nbody          | 116 ms                                                                 | 114 ms: 1.02x faster                                                              |
| pidigits       | 233 ms                                                                 | 236 ms: 1.01x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                      |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_v8       | 29.0 ms                                                                | 27.1 ms: 1.07x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                      |

Benchmark hidden because not significant (3): regex_compile, regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_iterparse | 148 ms                                                                 | 143 ms: 1.04x faster                                                              |
| tomli_loads         | 2.48 sec                                                               | 2.42 sec: 1.02x faster                                                            |
| pickle_pure_python  | 393 us                                                                 | 397 us: 1.01x slower                                                              |
| json_dumps          | 14.5 ms                                                                | 14.9 ms: 1.03x slower                                                             |
| json_loads          | 37.4 us                                                                | 39.3 us: 1.05x slower                                                             |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                                      |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_generate, unpickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| django_template | 44.5 ms                                                                | 43.2 ms: 1.03x faster                                                             |
| genshi_xml      | 62.9 ms                                                                | 61.9 ms: 1.02x faster                                                             |
| mako            | 17.3 ms                                                                | 17.7 ms: 1.03x slower                                                             |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                                      |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| bench_thread_pool          | 3.02 ms                                                                | 2.55 ms: 1.18x faster                                                             |
| async_tree_memoization     | 462 ms                                                                 | 432 ms: 1.07x faster                                                              |
| regex_v8                   | 29.0 ms                                                                | 27.1 ms: 1.07x faster                                                             |
| async_tree_cpu_io_mixed    | 695 ms                                                                 | 654 ms: 1.06x faster                                                              |
| 2to3                       | 385 ms                                                                 | 362 ms: 1.06x faster                                                              |
| async_generators           | 519 ms                                                                 | 488 ms: 1.06x faster                                                              |
| sqlglot_v2_transpile       | 2.10 ms                                                                | 1.99 ms: 1.06x faster                                                             |
| sqlglot_v2_optimize        | 69.2 ms                                                                | 66.1 ms: 1.05x faster                                                             |
| asyncio_websockets         | 697 ms                                                                 | 667 ms: 1.04x faster                                                              |
| sphinx                     | 1.43 sec                                                               | 1.37 sec: 1.04x faster                                                            |
| async_tree_io              | 859 ms                                                                 | 823 ms: 1.04x faster                                                              |
| sqlglot_v2_normalize       | 136 ms                                                                 | 131 ms: 1.04x faster                                                              |
| sympy_expand               | 568 ms                                                                 | 547 ms: 1.04x faster                                                              |
| async_tree_cpu_io_mixed_tg | 668 ms                                                                 | 644 ms: 1.04x faster                                                              |
| xml_etree_iterparse        | 148 ms                                                                 | 143 ms: 1.04x faster                                                              |
| async_tree_none            | 373 ms                                                                 | 360 ms: 1.04x faster                                                              |
| comprehensions             | 21.8 us                                                                | 21.1 us: 1.03x faster                                                             |
| async_tree_none_tg         | 355 ms                                                                 | 344 ms: 1.03x faster                                                              |
| pycparser                  | 1.54 sec                                                               | 1.50 sec: 1.03x faster                                                            |
| subparsers                 | 29.1 ms                                                                | 28.2 ms: 1.03x faster                                                             |
| django_template            | 44.5 ms                                                                | 43.2 ms: 1.03x faster                                                             |
| json                       | 7.04 ms                                                                | 6.86 ms: 1.03x faster                                                             |
| tomli_loads                | 2.48 sec                                                               | 2.42 sec: 1.02x faster                                                            |
| async_tree_memoization_tg  | 460 ms                                                                 | 449 ms: 1.02x faster                                                              |
| thrift                     | 958 us                                                                 | 936 us: 1.02x faster                                                              |
| bpe_tokeniser              | 5.76 sec                                                               | 5.63 sec: 1.02x faster                                                            |
| generators                 | 41.3 ms                                                                | 40.4 ms: 1.02x faster                                                             |
| sympy_integrate            | 25.6 ms                                                                | 25.1 ms: 1.02x faster                                                             |
| nbody                      | 116 ms                                                                 | 114 ms: 1.02x faster                                                              |
| many_optionals             | 1.17 ms                                                                | 1.15 ms: 1.02x faster                                                             |
| genshi_xml                 | 62.9 ms                                                                | 61.9 ms: 1.02x faster                                                             |
| docutils                   | 3.67 sec                                                               | 3.62 sec: 1.01x faster                                                            |
| sqlglot_v2_parse           | 1.60 ms                                                                | 1.58 ms: 1.01x faster                                                             |
| dulwich_log                | 74.9 ms                                                                | 74.1 ms: 1.01x faster                                                             |
| chaos                      | 71.2 ms                                                                | 70.5 ms: 1.01x faster                                                             |
| sympy_sum                  | 189 ms                                                                 | 187 ms: 1.01x faster                                                              |
| sympy_str                  | 331 ms                                                                 | 328 ms: 1.01x faster                                                              |
| deepcopy_memo              | 37.4 us                                                                | 37.1 us: 1.01x faster                                                             |
| pickle_pure_python         | 393 us                                                                 | 397 us: 1.01x slower                                                              |
| go                         | 141 ms                                                                 | 143 ms: 1.01x slower                                                              |
| pidigits                   | 233 ms                                                                 | 236 ms: 1.01x slower                                                              |
| pathlib                    | 24.8 ms                                                                | 25.1 ms: 1.01x slower                                                             |
| pprint_safe_repr           | 885 ms                                                                 | 897 ms: 1.01x slower                                                              |
| coroutines                 | 29.8 ms                                                                | 30.2 ms: 1.01x slower                                                             |
| mdp                        | 1.87 sec                                                               | 1.90 sec: 1.01x slower                                                            |
| richards_super             | 62.9 ms                                                                | 63.7 ms: 1.01x slower                                                             |
| richards                   | 54.6 ms                                                                | 55.4 ms: 1.01x slower                                                             |
| spectral_norm              | 126 ms                                                                 | 127 ms: 1.01x slower                                                              |
| scimark_monte_carlo        | 80.0 ms                                                                | 81.2 ms: 1.02x slower                                                             |
| scimark_fft                | 412 ms                                                                 | 419 ms: 1.02x slower                                                              |
| connected_components       | 753 ms                                                                 | 766 ms: 1.02x slower                                                              |
| fannkuch                   | 503 ms                                                                 | 512 ms: 1.02x slower                                                              |
| shortest_path              | 827 ms                                                                 | 845 ms: 1.02x slower                                                              |
| mako                       | 17.3 ms                                                                | 17.7 ms: 1.03x slower                                                             |
| json_dumps                 | 14.5 ms                                                                | 14.9 ms: 1.03x slower                                                             |
| create_gc_cycles           | 3.97 ms                                                                | 4.09 ms: 1.03x slower                                                             |
| gc_traversal               | 8.12 ms                                                                | 8.40 ms: 1.03x slower                                                             |
| pyflate                    | 566 ms                                                                 | 587 ms: 1.04x slower                                                              |
| logging_silent             | 125 ns                                                                 | 131 ns: 1.04x slower                                                              |
| logging_format             | 8.28 us                                                                | 8.62 us: 1.04x slower                                                             |
| json_loads                 | 37.4 us                                                                | 39.3 us: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                                      |

Benchmark hidden because not significant (33): deepcopy_reduce, async_tree_io_tg, bench_mp_pool, pylint, sqlite_synth, deepcopy, telco, xml_etree_parse, regex_compile, float, python_startup_no_site, k_core, scimark_lu, python_startup, crypto_pyaes, xml_etree_generate, unpickle_pure_python, pprint_pformat, xml_etree_process, deltablue, meteor_contest, logging_simple, typing_runtime_protocols, regex_dna, coverage, hexiom, raytrace, html5lib, scimark_sor, genshi_text, scimark_sparse_mat_mult, regex_effbot, nqueens

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 98.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x