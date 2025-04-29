# Results vs. default_base_vs_NOGIL

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.092x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 385 ms                                                                 | 425 ms: 1.10x slower                                                              |
| docutils       | 3.67 sec                                                               | 3.92 sec: 1.07x slower                                                            |
| html5lib       | 78.6 ms                                                                | 83.2 ms: 1.06x slower                                                             |
| sphinx         | 1.43 sec                                                               | 1.60 sec: 1.12x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 851 ms                                                                 | 708 ms: 1.20x faster                                                              |
| async_tree_none_tg         | 355 ms                                                                 | 298 ms: 1.19x faster                                                              |
| async_tree_io              | 859 ms                                                                 | 740 ms: 1.16x faster                                                              |
| async_tree_memoization_tg  | 460 ms                                                                 | 403 ms: 1.14x faster                                                              |
| async_tree_cpu_io_mixed_tg | 668 ms                                                                 | 595 ms: 1.12x faster                                                              |
| async_tree_cpu_io_mixed    | 695 ms                                                                 | 638 ms: 1.09x faster                                                              |
| async_tree_none            | 373 ms                                                                 | 348 ms: 1.07x faster                                                              |
| async_tree_memoization     | 462 ms                                                                 | 452 ms: 1.02x faster                                                              |
| async_generators           | 519 ms                                                                 | 542 ms: 1.05x slower                                                              |
| Geometric mean             | (ref)                                                                  | 1.09x faster                                                                      |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pidigits       | 233 ms                                                                 | 219 ms: 1.06x faster                                                              |
| float          | 94.1 ms                                                                | 90.6 ms: 1.04x faster                                                             |
| nbody          | 116 ms                                                                 | 148 ms: 1.28x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_effbot   | 3.79 ms                                                                | 3.66 ms: 1.04x faster                                                             |
| regex_dna      | 247 ms                                                                 | 251 ms: 1.01x slower                                                              |
| regex_compile  | 153 ms                                                                 | 182 ms: 1.19x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                                      |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 148 ms                                                                 | 134 ms: 1.10x faster                                                              |
| xml_etree_parse      | 191 ms                                                                 | 200 ms: 1.04x slower                                                              |
| pickle_pure_python   | 393 us                                                                 | 432 us: 1.10x slower                                                              |
| unpickle_pure_python | 276 us                                                                 | 305 us: 1.10x slower                                                              |
| json_loads           | 37.4 us                                                                | 42.1 us: 1.12x slower                                                             |
| tomli_loads          | 2.48 sec                                                               | 2.92 sec: 1.18x slower                                                            |
| json_dumps           | 14.5 ms                                                                | 17.1 ms: 1.18x slower                                                             |
| xml_etree_process    | 79.1 ms                                                                | 95.0 ms: 1.20x slower                                                             |
| xml_etree_generate   | 115 ms                                                                 | 139 ms: 1.21x slower                                                              |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup_no_site | 11.6 ms                                                                | 15.5 ms: 1.33x slower                                                             |
| python_startup         | 19.0 ms                                                                | 25.9 ms: 1.36x slower                                                             |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| django_template | 44.5 ms                                                                | 49.9 ms: 1.12x slower                                                             |
| genshi_xml      | 62.9 ms                                                                | 75.8 ms: 1.20x slower                                                             |
| mako            | 17.3 ms                                                                | 21.9 ms: 1.26x slower                                                             |
| genshi_text     | 26.7 ms                                                                | 34.6 ms: 1.29x slower                                                             |
| Geometric mean  | (ref)                                                                  | 1.22x slower                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250429-linux-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| gc_traversal               | 8.12 ms                                                                | 4.08 ms: 1.99x faster                                                             |
| create_gc_cycles           | 3.97 ms                                                                | 2.73 ms: 1.45x faster                                                             |
| async_tree_io_tg           | 851 ms                                                                 | 708 ms: 1.20x faster                                                              |
| async_tree_none_tg         | 355 ms                                                                 | 298 ms: 1.19x faster                                                              |
| async_tree_io              | 859 ms                                                                 | 740 ms: 1.16x faster                                                              |
| async_tree_memoization_tg  | 460 ms                                                                 | 403 ms: 1.14x faster                                                              |
| async_tree_cpu_io_mixed_tg | 668 ms                                                                 | 595 ms: 1.12x faster                                                              |
| xml_etree_iterparse        | 148 ms                                                                 | 134 ms: 1.10x faster                                                              |
| sqlite_synth               | 3.30 us                                                                | 3.01 us: 1.10x faster                                                             |
| async_tree_cpu_io_mixed    | 695 ms                                                                 | 638 ms: 1.09x faster                                                              |
| async_tree_none            | 373 ms                                                                 | 348 ms: 1.07x faster                                                              |
| pidigits                   | 233 ms                                                                 | 219 ms: 1.06x faster                                                              |
| pycparser                  | 1.54 sec                                                               | 1.47 sec: 1.05x faster                                                            |
| float                      | 94.1 ms                                                                | 90.6 ms: 1.04x faster                                                             |
| regex_effbot               | 3.79 ms                                                                | 3.66 ms: 1.04x faster                                                             |
| async_tree_memoization     | 462 ms                                                                 | 452 ms: 1.02x faster                                                              |
| regex_dna                  | 247 ms                                                                 | 251 ms: 1.01x slower                                                              |
| xml_etree_parse            | 191 ms                                                                 | 200 ms: 1.04x slower                                                              |
| async_generators           | 519 ms                                                                 | 542 ms: 1.05x slower                                                              |
| k_core                     | 3.90 sec                                                               | 4.08 sec: 1.05x slower                                                            |
| pathlib                    | 24.8 ms                                                                | 26.0 ms: 1.05x slower                                                             |
| html5lib                   | 78.6 ms                                                                | 83.2 ms: 1.06x slower                                                             |
| spectral_norm              | 126 ms                                                                 | 133 ms: 1.06x slower                                                              |
| dulwich_log                | 74.9 ms                                                                | 79.9 ms: 1.07x slower                                                             |
| docutils                   | 3.67 sec                                                               | 3.92 sec: 1.07x slower                                                            |
| scimark_sor                | 145 ms                                                                 | 159 ms: 1.10x slower                                                              |
| pickle_pure_python         | 393 us                                                                 | 432 us: 1.10x slower                                                              |
| unpickle_pure_python       | 276 us                                                                 | 305 us: 1.10x slower                                                              |
| 2to3                       | 385 ms                                                                 | 425 ms: 1.10x slower                                                              |
| sqlglot_v2_normalize       | 136 ms                                                                 | 150 ms: 1.11x slower                                                              |
| logging_silent             | 125 ns                                                                 | 140 ns: 1.12x slower                                                              |
| chaos                      | 71.2 ms                                                                | 79.6 ms: 1.12x slower                                                             |
| sphinx                     | 1.43 sec                                                               | 1.60 sec: 1.12x slower                                                            |
| django_template            | 44.5 ms                                                                | 49.9 ms: 1.12x slower                                                             |
| deltablue                  | 4.33 ms                                                                | 4.86 ms: 1.12x slower                                                             |
| json_loads                 | 37.4 us                                                                | 42.1 us: 1.12x slower                                                             |
| scimark_fft                | 412 ms                                                                 | 464 ms: 1.13x slower                                                              |
| nqueens                    | 98.5 ms                                                                | 112 ms: 1.13x slower                                                              |
| scimark_lu                 | 147 ms                                                                 | 167 ms: 1.14x slower                                                              |
| pylint                     | 386 ms                                                                 | 441 ms: 1.14x slower                                                              |
| generators                 | 41.3 ms                                                                | 47.3 ms: 1.15x slower                                                             |
| subparsers                 | 29.1 ms                                                                | 33.3 ms: 1.15x slower                                                             |
| many_optionals             | 1.17 ms                                                                | 1.35 ms: 1.15x slower                                                             |
| connected_components       | 753 ms                                                                 | 876 ms: 1.16x slower                                                              |
| telco                      | 9.24 ms                                                                | 10.8 ms: 1.17x slower                                                             |
| scimark_sparse_mat_mult    | 5.68 ms                                                                | 6.63 ms: 1.17x slower                                                             |
| raytrace                   | 329 ms                                                                 | 384 ms: 1.17x slower                                                              |
| deepcopy_reduce            | 3.38 us                                                                | 3.96 us: 1.17x slower                                                             |
| tomli_loads                | 2.48 sec                                                               | 2.92 sec: 1.18x slower                                                            |
| pyflate                    | 566 ms                                                                 | 666 ms: 1.18x slower                                                              |
| json_dumps                 | 14.5 ms                                                                | 17.1 ms: 1.18x slower                                                             |
| logging_simple             | 7.58 us                                                                | 8.95 us: 1.18x slower                                                             |
| sqlglot_v2_transpile       | 2.10 ms                                                                | 2.48 ms: 1.18x slower                                                             |
| go                         | 141 ms                                                                 | 167 ms: 1.18x slower                                                              |
| comprehensions             | 21.8 us                                                                | 25.8 us: 1.18x slower                                                             |
| pprint_safe_repr           | 885 ms                                                                 | 1.05 sec: 1.18x slower                                                            |
| shortest_path              | 827 ms                                                                 | 983 ms: 1.19x slower                                                              |
| deepcopy                   | 319 us                                                                 | 379 us: 1.19x slower                                                              |
| regex_compile              | 153 ms                                                                 | 182 ms: 1.19x slower                                                              |
| fannkuch                   | 503 ms                                                                 | 599 ms: 1.19x slower                                                              |
| pprint_pformat             | 1.81 sec                                                               | 2.17 sec: 1.20x slower                                                            |
| sympy_expand               | 568 ms                                                                 | 680 ms: 1.20x slower                                                              |
| sqlglot_v2_optimize        | 69.2 ms                                                                | 83.1 ms: 1.20x slower                                                             |
| xml_etree_process          | 79.1 ms                                                                | 95.0 ms: 1.20x slower                                                             |
| sympy_integrate            | 25.6 ms                                                                | 30.8 ms: 1.20x slower                                                             |
| genshi_xml                 | 62.9 ms                                                                | 75.8 ms: 1.20x slower                                                             |
| thrift                     | 958 us                                                                 | 1.16 ms: 1.21x slower                                                             |
| sympy_sum                  | 189 ms                                                                 | 229 ms: 1.21x slower                                                              |
| xml_etree_generate         | 115 ms                                                                 | 139 ms: 1.21x slower                                                              |
| deepcopy_memo              | 37.4 us                                                                | 45.7 us: 1.22x slower                                                             |
| crypto_pyaes               | 89.6 ms                                                                | 110 ms: 1.22x slower                                                              |
| sympy_str                  | 331 ms                                                                 | 408 ms: 1.23x slower                                                              |
| hexiom                     | 7.55 ms                                                                | 9.32 ms: 1.23x slower                                                             |
| mdp                        | 1.87 sec                                                               | 2.31 sec: 1.24x slower                                                            |
| scimark_monte_carlo        | 80.0 ms                                                                | 98.8 ms: 1.24x slower                                                             |
| logging_format             | 8.28 us                                                                | 10.3 us: 1.25x slower                                                             |
| richards_super             | 62.9 ms                                                                | 78.9 ms: 1.25x slower                                                             |
| mako                       | 17.3 ms                                                                | 21.9 ms: 1.26x slower                                                             |
| meteor_contest             | 128 ms                                                                 | 163 ms: 1.27x slower                                                              |
| richards                   | 54.6 ms                                                                | 69.5 ms: 1.27x slower                                                             |
| sqlglot_v2_parse           | 1.60 ms                                                                | 2.04 ms: 1.28x slower                                                             |
| nbody                      | 116 ms                                                                 | 148 ms: 1.28x slower                                                              |
| bpe_tokeniser              | 5.76 sec                                                               | 7.42 sec: 1.29x slower                                                            |
| genshi_text                | 26.7 ms                                                                | 34.6 ms: 1.29x slower                                                             |
| typing_runtime_protocols   | 199 us                                                                 | 261 us: 1.32x slower                                                              |
| python_startup_no_site     | 11.6 ms                                                                | 15.5 ms: 1.33x slower                                                             |
| coverage                   | 107 ms                                                                 | 143 ms: 1.34x slower                                                              |
| python_startup             | 19.0 ms                                                                | 25.9 ms: 1.36x slower                                                             |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                                      |

Benchmark hidden because not significant (6): bench_mp_pool, asyncio_websockets, bench_thread_pool, coroutines, regex_v8, json

- Geometric mean (including insignificant results): 1.092x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x