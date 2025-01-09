# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: a111bff
- commit date: 2025-01-08
- overall geometric mean: 1.192x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 466 ms                                                                 | 600 ms: 1.29x slower                                                    |
| docutils       | 3.92 sec                                                               | 4.23 sec: 1.08x slower                                                  |
| html5lib       | 77.5 ms                                                                | 108 ms: 1.39x slower                                                    |
| sphinx         | 1.48 sec                                                               | 1.60 sec: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.20x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| coroutines                 | 29.9 ms                                                                | 31.4 ms: 1.05x slower                                                   |
| async_generators           | 569 ms                                                                 | 602 ms: 1.06x slower                                                    |
| async_tree_cpu_io_mixed_tg | 676 ms                                                                 | 748 ms: 1.11x slower                                                    |
| async_tree_io_tg           | 857 ms                                                                 | 960 ms: 1.12x slower                                                    |
| async_tree_memoization_tg  | 472 ms                                                                 | 542 ms: 1.15x slower                                                    |
| async_tree_cpu_io_mixed    | 719 ms                                                                 | 867 ms: 1.21x slower                                                    |
| async_tree_io              | 863 ms                                                                 | 1.07 sec: 1.24x slower                                                  |
| async_tree_none            | 399 ms                                                                 | 495 ms: 1.24x slower                                                    |
| async_tree_none_tg         | 336 ms                                                                 | 439 ms: 1.31x slower                                                    |
| async_tree_memoization     | 481 ms                                                                 | 634 ms: 1.32x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.16x slower                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 110 ms                                                                 | 131 ms: 1.19x slower                                                    |
| nbody          | 124 ms                                                                 | 173 ms: 1.39x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 4.72 ms                                                                | 4.27 ms: 1.10x faster                                                   |
| regex_dna      | 270 ms                                                                 | 321 ms: 1.19x slower                                                    |
| regex_compile  | 160 ms                                                                 | 221 ms: 1.38x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 154 ms                                                                 | 135 ms: 1.14x faster                                                    |
| json_loads           | 35.5 us                                                                | 36.8 us: 1.04x slower                                                   |
| xml_etree_generate   | 128 ms                                                                 | 137 ms: 1.07x slower                                                    |
| xml_etree_parse      | 199 ms                                                                 | 222 ms: 1.11x slower                                                    |
| json_dumps           | 15.5 ms                                                                | 18.1 ms: 1.17x slower                                                   |
| tomli_loads          | 2.58 sec                                                               | 3.03 sec: 1.18x slower                                                  |
| xml_etree_process    | 86.8 ms                                                                | 113 ms: 1.30x slower                                                    |
| unpickle_pure_python | 291 us                                                                 | 389 us: 1.34x slower                                                    |
| pickle_pure_python   | 418 us                                                                 | 702 us: 1.68x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.18x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 28.8 ms                                                                | 32.7 ms: 1.14x slower                                                   |
| python_startup_no_site | 17.0 ms                                                                | 20.2 ms: 1.19x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                                | 91.2 ms: 1.24x slower                                                   |
| genshi_text     | 30.9 ms                                                                | 41.2 ms: 1.33x slower                                                   |
| django_template | 46.5 ms                                                                | 70.3 ms: 1.51x slower                                                   |
| mako            | 16.5 ms                                                                | 25.7 ms: 1.55x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.40x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| create_gc_cycles           | 4.32 ms                                                                | 2.89 ms: 1.49x faster                                                   |
| xml_etree_iterparse        | 154 ms                                                                 | 135 ms: 1.14x faster                                                    |
| regex_effbot               | 4.72 ms                                                                | 4.27 ms: 1.10x faster                                                   |
| gc_traversal               | 9.07 ms                                                                | 8.36 ms: 1.08x faster                                                   |
| json_loads                 | 35.5 us                                                                | 36.8 us: 1.04x slower                                                   |
| coroutines                 | 29.9 ms                                                                | 31.4 ms: 1.05x slower                                                   |
| async_generators           | 569 ms                                                                 | 602 ms: 1.06x slower                                                    |
| xml_etree_generate         | 128 ms                                                                 | 137 ms: 1.07x slower                                                    |
| docutils                   | 3.92 sec                                                               | 4.23 sec: 1.08x slower                                                  |
| pycparser                  | 1.54 sec                                                               | 1.67 sec: 1.08x slower                                                  |
| k_core                     | 4.08 sec                                                               | 4.44 sec: 1.09x slower                                                  |
| sphinx                     | 1.48 sec                                                               | 1.60 sec: 1.09x slower                                                  |
| dulwich_log                | 105 ms                                                                 | 114 ms: 1.09x slower                                                    |
| pathlib                    | 28.3 ms                                                                | 31.0 ms: 1.10x slower                                                   |
| async_tree_cpu_io_mixed_tg | 676 ms                                                                 | 748 ms: 1.11x slower                                                    |
| mdp                        | 3.96 sec                                                               | 4.40 sec: 1.11x slower                                                  |
| xml_etree_parse            | 199 ms                                                                 | 222 ms: 1.11x slower                                                    |
| async_tree_io_tg           | 857 ms                                                                 | 960 ms: 1.12x slower                                                    |
| python_startup             | 28.8 ms                                                                | 32.7 ms: 1.14x slower                                                   |
| async_tree_memoization_tg  | 472 ms                                                                 | 542 ms: 1.15x slower                                                    |
| sympy_expand               | 585 ms                                                                 | 682 ms: 1.17x slower                                                    |
| shortest_path              | 929 ms                                                                 | 1.08 sec: 1.17x slower                                                  |
| json_dumps                 | 15.5 ms                                                                | 18.1 ms: 1.17x slower                                                   |
| sympy_integrate            | 31.0 ms                                                                | 36.4 ms: 1.17x slower                                                   |
| sympy_sum                  | 217 ms                                                                 | 255 ms: 1.17x slower                                                    |
| tomli_loads                | 2.58 sec                                                               | 3.03 sec: 1.18x slower                                                  |
| deepcopy_memo              | 42.7 us                                                                | 50.3 us: 1.18x slower                                                   |
| connected_components       | 810 ms                                                                 | 956 ms: 1.18x slower                                                    |
| deepcopy                   | 360 us                                                                 | 426 us: 1.18x slower                                                    |
| float                      | 110 ms                                                                 | 131 ms: 1.19x slower                                                    |
| python_startup_no_site     | 17.0 ms                                                                | 20.2 ms: 1.19x slower                                                   |
| regex_dna                  | 270 ms                                                                 | 321 ms: 1.19x slower                                                    |
| async_tree_cpu_io_mixed    | 719 ms                                                                 | 867 ms: 1.21x slower                                                    |
| deepcopy_reduce            | 3.77 us                                                                | 4.56 us: 1.21x slower                                                   |
| telco                      | 9.58 ms                                                                | 11.6 ms: 1.21x slower                                                   |
| coverage                   | 108 ms                                                                 | 131 ms: 1.21x slower                                                    |
| many_optionals             | 1.08 ms                                                                | 1.31 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult    | 6.73 ms                                                                | 8.17 ms: 1.21x slower                                                   |
| genshi_xml                 | 73.6 ms                                                                | 91.2 ms: 1.24x slower                                                   |
| async_tree_io              | 863 ms                                                                 | 1.07 sec: 1.24x slower                                                  |
| async_tree_none            | 399 ms                                                                 | 495 ms: 1.24x slower                                                    |
| logging_simple             | 8.26 us                                                                | 10.3 us: 1.25x slower                                                   |
| fannkuch                   | 540 ms                                                                 | 674 ms: 1.25x slower                                                    |
| sqlglot_optimize           | 75.0 ms                                                                | 94.0 ms: 1.25x slower                                                   |
| pyflate                    | 692 ms                                                                 | 868 ms: 1.26x slower                                                    |
| logging_format             | 10.1 us                                                                | 12.7 us: 1.26x slower                                                   |
| scimark_fft                | 444 ms                                                                 | 558 ms: 1.26x slower                                                    |
| nqueens                    | 110 ms                                                                 | 138 ms: 1.26x slower                                                    |
| scimark_lu                 | 160 ms                                                                 | 202 ms: 1.27x slower                                                    |
| 2to3                       | 466 ms                                                                 | 600 ms: 1.29x slower                                                    |
| meteor_contest             | 142 ms                                                                 | 184 ms: 1.30x slower                                                    |
| pprint_safe_repr           | 930 ms                                                                 | 1.21 sec: 1.30x slower                                                  |
| xml_etree_process          | 86.8 ms                                                                | 113 ms: 1.30x slower                                                    |
| subparsers                 | 31.1 ms                                                                | 40.6 ms: 1.30x slower                                                   |
| async_tree_none_tg         | 336 ms                                                                 | 439 ms: 1.31x slower                                                    |
| async_tree_memoization     | 481 ms                                                                 | 634 ms: 1.32x slower                                                    |
| genshi_text                | 30.9 ms                                                                | 41.2 ms: 1.33x slower                                                   |
| unpickle_pure_python       | 291 us                                                                 | 389 us: 1.34x slower                                                    |
| bpe_tokeniser              | 5.69 sec                                                               | 7.64 sec: 1.34x slower                                                  |
| thrift                     | 974 us                                                                 | 1.31 ms: 1.34x slower                                                   |
| chaos                      | 83.9 ms                                                                | 113 ms: 1.35x slower                                                    |
| typing_runtime_protocols   | 206 us                                                                 | 279 us: 1.35x slower                                                    |
| sqlglot_normalize          | 140 ms                                                                 | 191 ms: 1.36x slower                                                    |
| scimark_sor                | 163 ms                                                                 | 222 ms: 1.36x slower                                                    |
| hexiom                     | 8.33 ms                                                                | 11.4 ms: 1.37x slower                                                   |
| pylint                     | 384 ms                                                                 | 526 ms: 1.37x slower                                                    |
| richards                   | 57.2 ms                                                                | 78.5 ms: 1.37x slower                                                   |
| regex_compile              | 160 ms                                                                 | 221 ms: 1.38x slower                                                    |
| scimark_monte_carlo        | 92.8 ms                                                                | 129 ms: 1.39x slower                                                    |
| html5lib                   | 77.5 ms                                                                | 108 ms: 1.39x slower                                                    |
| nbody                      | 124 ms                                                                 | 173 ms: 1.39x slower                                                    |
| sqlalchemy_declarative     | 184 ms                                                                 | 256 ms: 1.39x slower                                                    |
| sympy_str                  | 341 ms                                                                 | 478 ms: 1.40x slower                                                    |
| pprint_pformat             | 1.89 sec                                                               | 2.66 sec: 1.41x slower                                                  |
| generators                 | 38.7 ms                                                                | 54.8 ms: 1.42x slower                                                   |
| crypto_pyaes               | 86.4 ms                                                                | 124 ms: 1.44x slower                                                    |
| richards_super             | 63.2 ms                                                                | 91.6 ms: 1.45x slower                                                   |
| comprehensions             | 21.2 us                                                                | 31.8 us: 1.50x slower                                                   |
| django_template            | 46.5 ms                                                                | 70.3 ms: 1.51x slower                                                   |
| raytrace                   | 364 ms                                                                 | 563 ms: 1.55x slower                                                    |
| mako                       | 16.5 ms                                                                | 25.7 ms: 1.55x slower                                                   |
| logging_silent             | 137 ns                                                                 | 224 ns: 1.64x slower                                                    |
| pickle_pure_python         | 418 us                                                                 | 702 us: 1.68x slower                                                    |
| go                         | 162 ms                                                                 | 272 ms: 1.68x slower                                                    |
| sqlglot_transpile          | 2.04 ms                                                                | 3.44 ms: 1.69x slower                                                   |
| sqlalchemy_imperative      | 22.1 ms                                                                | 39.8 ms: 1.81x slower                                                   |
| sqlglot_parse              | 1.62 ms                                                                | 3.07 ms: 1.89x slower                                                   |
| deltablue                  | 4.21 ms                                                                | 9.71 ms: 2.31x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.24x slower                                                            |

Benchmark hidden because not significant (8): pidigits, bench_mp_pool, sqlite_synth, asyncio_websockets, regex_v8, json, spectral_norm, bench_thread_pool

- Geometric mean (including insignificant results): 1.192x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.19x