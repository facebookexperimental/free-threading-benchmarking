# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: f509a13
- commit date: 2025-01-09
- overall geometric mean: 1.253x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 466 ms                                                                 | 681 ms: 1.46x slower                                                    |
| docutils       | 3.92 sec                                                               | 4.92 sec: 1.25x slower                                                  |
| html5lib       | 77.5 ms                                                                | 129 ms: 1.67x slower                                                    |
| sphinx         | 1.48 sec                                                               | 1.73 sec: 1.17x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.38x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| asyncio_websockets         | 749 ms                                                                 | 830 ms: 1.11x slower                                                    |
| async_tree_cpu_io_mixed    | 719 ms                                                                 | 816 ms: 1.13x slower                                                    |
| async_generators           | 569 ms                                                                 | 665 ms: 1.17x slower                                                    |
| async_tree_io_tg           | 857 ms                                                                 | 1.04 sec: 1.21x slower                                                  |
| async_tree_memoization_tg  | 472 ms                                                                 | 577 ms: 1.22x slower                                                    |
| coroutines                 | 29.9 ms                                                                | 37.4 ms: 1.25x slower                                                   |
| async_tree_cpu_io_mixed_tg | 676 ms                                                                 | 860 ms: 1.27x slower                                                    |
| async_tree_none_tg         | 336 ms                                                                 | 436 ms: 1.30x slower                                                    |
| async_tree_io              | 863 ms                                                                 | 1.14 sec: 1.32x slower                                                  |
| async_tree_memoization     | 481 ms                                                                 | 652 ms: 1.35x slower                                                    |
| async_tree_none            | 399 ms                                                                 | 565 ms: 1.42x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.25x slower                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 247 ms                                                                 | 236 ms: 1.05x faster                                                    |
| float          | 110 ms                                                                 | 146 ms: 1.33x slower                                                    |
| nbody          | 124 ms                                                                 | 197 ms: 1.58x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.26x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 270 ms                                                                 | 278 ms: 1.03x slower                                                    |
| regex_compile  | 160 ms                                                                 | 234 ms: 1.46x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                            |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_generate   | 128 ms                                                                 | 145 ms: 1.13x slower                                                    |
| json_loads           | 35.5 us                                                                | 41.7 us: 1.18x slower                                                   |
| json_dumps           | 15.5 ms                                                                | 19.0 ms: 1.23x slower                                                   |
| xml_etree_process    | 86.8 ms                                                                | 108 ms: 1.25x slower                                                    |
| tomli_loads          | 2.58 sec                                                               | 3.23 sec: 1.26x slower                                                  |
| xml_etree_parse      | 199 ms                                                                 | 256 ms: 1.28x slower                                                    |
| unpickle_pure_python | 291 us                                                                 | 468 us: 1.60x slower                                                    |
| pickle_pure_python   | 418 us                                                                 | 813 us: 1.95x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.29x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 28.8 ms                                                                | 42.9 ms: 1.49x slower                                                   |
| python_startup_no_site | 17.0 ms                                                                | 27.2 ms: 1.60x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.54x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 46.5 ms                                                                | 61.3 ms: 1.32x slower                                                   |
| genshi_xml      | 73.6 ms                                                                | 97.3 ms: 1.32x slower                                                   |
| genshi_text     | 30.9 ms                                                                | 43.1 ms: 1.40x slower                                                   |
| mako            | 16.5 ms                                                                | 27.5 ms: 1.67x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.42x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits                   | 247 ms                                                                 | 236 ms: 1.05x faster                                                    |
| regex_dna                  | 270 ms                                                                 | 278 ms: 1.03x slower                                                    |
| bench_mp_pool              | 93.2 ms                                                                | 101 ms: 1.09x slower                                                    |
| spectral_norm              | 149 ms                                                                 | 162 ms: 1.09x slower                                                    |
| json                       | 7.27 ms                                                                | 7.98 ms: 1.10x slower                                                   |
| asyncio_websockets         | 749 ms                                                                 | 830 ms: 1.11x slower                                                    |
| gc_traversal               | 9.07 ms                                                                | 10.2 ms: 1.12x slower                                                   |
| xml_etree_generate         | 128 ms                                                                 | 145 ms: 1.13x slower                                                    |
| async_tree_cpu_io_mixed    | 719 ms                                                                 | 816 ms: 1.13x slower                                                    |
| async_generators           | 569 ms                                                                 | 665 ms: 1.17x slower                                                    |
| sphinx                     | 1.48 sec                                                               | 1.73 sec: 1.17x slower                                                  |
| json_loads                 | 35.5 us                                                                | 41.7 us: 1.18x slower                                                   |
| sqlite_synth               | 3.58 us                                                                | 4.22 us: 1.18x slower                                                   |
| pathlib                    | 28.3 ms                                                                | 33.7 ms: 1.19x slower                                                   |
| k_core                     | 4.08 sec                                                               | 4.93 sec: 1.21x slower                                                  |
| async_tree_io_tg           | 857 ms                                                                 | 1.04 sec: 1.21x slower                                                  |
| async_tree_memoization_tg  | 472 ms                                                                 | 577 ms: 1.22x slower                                                    |
| mdp                        | 3.96 sec                                                               | 4.86 sec: 1.23x slower                                                  |
| deepcopy_reduce            | 3.77 us                                                                | 4.63 us: 1.23x slower                                                   |
| json_dumps                 | 15.5 ms                                                                | 19.0 ms: 1.23x slower                                                   |
| sympy_integrate            | 31.0 ms                                                                | 38.5 ms: 1.24x slower                                                   |
| telco                      | 9.58 ms                                                                | 11.9 ms: 1.24x slower                                                   |
| xml_etree_process          | 86.8 ms                                                                | 108 ms: 1.25x slower                                                    |
| sqlglot_normalize          | 140 ms                                                                 | 175 ms: 1.25x slower                                                    |
| coroutines                 | 29.9 ms                                                                | 37.4 ms: 1.25x slower                                                   |
| scimark_lu                 | 160 ms                                                                 | 200 ms: 1.25x slower                                                    |
| docutils                   | 3.92 sec                                                               | 4.92 sec: 1.25x slower                                                  |
| tomli_loads                | 2.58 sec                                                               | 3.23 sec: 1.26x slower                                                  |
| shortest_path              | 929 ms                                                                 | 1.17 sec: 1.26x slower                                                  |
| scimark_fft                | 444 ms                                                                 | 563 ms: 1.27x slower                                                    |
| async_tree_cpu_io_mixed_tg | 676 ms                                                                 | 860 ms: 1.27x slower                                                    |
| many_optionals             | 1.08 ms                                                                | 1.38 ms: 1.27x slower                                                   |
| sqlglot_optimize           | 75.0 ms                                                                | 95.7 ms: 1.27x slower                                                   |
| fannkuch                   | 540 ms                                                                 | 691 ms: 1.28x slower                                                    |
| sympy_expand               | 585 ms                                                                 | 750 ms: 1.28x slower                                                    |
| pycparser                  | 1.54 sec                                                               | 1.98 sec: 1.28x slower                                                  |
| xml_etree_parse            | 199 ms                                                                 | 256 ms: 1.28x slower                                                    |
| logging_format             | 10.1 us                                                                | 13.2 us: 1.30x slower                                                   |
| async_tree_none_tg         | 336 ms                                                                 | 436 ms: 1.30x slower                                                    |
| deepcopy                   | 360 us                                                                 | 470 us: 1.31x slower                                                    |
| async_tree_io              | 863 ms                                                                 | 1.14 sec: 1.32x slower                                                  |
| connected_components       | 810 ms                                                                 | 1.07 sec: 1.32x slower                                                  |
| coverage                   | 108 ms                                                                 | 142 ms: 1.32x slower                                                    |
| django_template            | 46.5 ms                                                                | 61.3 ms: 1.32x slower                                                   |
| genshi_xml                 | 73.6 ms                                                                | 97.3 ms: 1.32x slower                                                   |
| nqueens                    | 110 ms                                                                 | 145 ms: 1.32x slower                                                    |
| pyflate                    | 692 ms                                                                 | 917 ms: 1.33x slower                                                    |
| float                      | 110 ms                                                                 | 146 ms: 1.33x slower                                                    |
| sympy_sum                  | 217 ms                                                                 | 292 ms: 1.35x slower                                                    |
| async_tree_memoization     | 481 ms                                                                 | 652 ms: 1.35x slower                                                    |
| meteor_contest             | 142 ms                                                                 | 196 ms: 1.38x slower                                                    |
| scimark_sparse_mat_mult    | 6.73 ms                                                                | 9.34 ms: 1.39x slower                                                   |
| deepcopy_memo              | 42.7 us                                                                | 59.6 us: 1.40x slower                                                   |
| genshi_text                | 30.9 ms                                                                | 43.1 ms: 1.40x slower                                                   |
| pprint_pformat             | 1.89 sec                                                               | 2.64 sec: 1.40x slower                                                  |
| pylint                     | 384 ms                                                                 | 540 ms: 1.41x slower                                                    |
| typing_runtime_protocols   | 206 us                                                                 | 290 us: 1.41x slower                                                    |
| async_tree_none            | 399 ms                                                                 | 565 ms: 1.42x slower                                                    |
| thrift                     | 974 us                                                                 | 1.39 ms: 1.43x slower                                                   |
| scimark_monte_carlo        | 92.8 ms                                                                | 133 ms: 1.43x slower                                                    |
| generators                 | 38.7 ms                                                                | 56.0 ms: 1.45x slower                                                   |
| regex_compile              | 160 ms                                                                 | 234 ms: 1.46x slower                                                    |
| 2to3                       | 466 ms                                                                 | 681 ms: 1.46x slower                                                    |
| pprint_safe_repr           | 930 ms                                                                 | 1.36 sec: 1.46x slower                                                  |
| dulwich_log                | 105 ms                                                                 | 155 ms: 1.48x slower                                                    |
| python_startup             | 28.8 ms                                                                | 42.9 ms: 1.49x slower                                                   |
| hexiom                     | 8.33 ms                                                                | 12.4 ms: 1.49x slower                                                   |
| scimark_sor                | 163 ms                                                                 | 247 ms: 1.51x slower                                                    |
| sympy_str                  | 341 ms                                                                 | 520 ms: 1.52x slower                                                    |
| richards                   | 57.2 ms                                                                | 88.2 ms: 1.54x slower                                                   |
| crypto_pyaes               | 86.4 ms                                                                | 134 ms: 1.55x slower                                                    |
| bpe_tokeniser              | 5.69 sec                                                               | 8.87 sec: 1.56x slower                                                  |
| richards_super             | 63.2 ms                                                                | 99.6 ms: 1.58x slower                                                   |
| nbody                      | 124 ms                                                                 | 197 ms: 1.58x slower                                                    |
| subparsers                 | 31.1 ms                                                                | 49.4 ms: 1.59x slower                                                   |
| logging_simple             | 8.26 us                                                                | 13.1 us: 1.59x slower                                                   |
| python_startup_no_site     | 17.0 ms                                                                | 27.2 ms: 1.60x slower                                                   |
| unpickle_pure_python       | 291 us                                                                 | 468 us: 1.60x slower                                                    |
| chaos                      | 83.9 ms                                                                | 138 ms: 1.64x slower                                                    |
| html5lib                   | 77.5 ms                                                                | 129 ms: 1.67x slower                                                    |
| mako                       | 16.5 ms                                                                | 27.5 ms: 1.67x slower                                                   |
| sqlalchemy_imperative      | 22.1 ms                                                                | 37.2 ms: 1.69x slower                                                   |
| logging_silent             | 137 ns                                                                 | 233 ns: 1.70x slower                                                    |
| comprehensions             | 21.2 us                                                                | 36.2 us: 1.71x slower                                                   |
| bench_thread_pool          | 3.39 ms                                                                | 5.81 ms: 1.72x slower                                                   |
| sqlalchemy_declarative     | 184 ms                                                                 | 325 ms: 1.77x slower                                                    |
| raytrace                   | 364 ms                                                                 | 644 ms: 1.77x slower                                                    |
| sqlglot_parse              | 1.62 ms                                                                | 3.12 ms: 1.92x slower                                                   |
| pickle_pure_python         | 418 us                                                                 | 813 us: 1.95x slower                                                    |
| go                         | 162 ms                                                                 | 314 ms: 1.95x slower                                                    |
| sqlglot_transpile          | 2.04 ms                                                                | 4.15 ms: 2.04x slower                                                   |
| deltablue                  | 4.21 ms                                                                | 10.3 ms: 2.46x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.36x slower                                                            |

Benchmark hidden because not significant (4): create_gc_cycles, xml_etree_iterparse, regex_v8, regex_effbot

- Geometric mean (including insignificant results): 1.253x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.19x