# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: 41ef420
- commit date: 2025-01-11
- overall geometric mean: 1.245x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 466 ms                                                                 | 660 ms: 1.42x slower                                                    |
| docutils       | 3.92 sec                                                               | 4.79 sec: 1.22x slower                                                  |
| html5lib       | 77.5 ms                                                                | 133 ms: 1.71x slower                                                    |
| sphinx         | 1.48 sec                                                               | 1.87 sec: 1.27x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.39x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| asyncio_websockets         | 749 ms                                                                 | 827 ms: 1.10x slower                                                    |
| async_tree_io_tg           | 857 ms                                                                 | 996 ms: 1.16x slower                                                    |
| async_tree_cpu_io_mixed    | 719 ms                                                                 | 849 ms: 1.18x slower                                                    |
| async_tree_cpu_io_mixed_tg | 676 ms                                                                 | 806 ms: 1.19x slower                                                    |
| async_generators           | 569 ms                                                                 | 681 ms: 1.20x slower                                                    |
| coroutines                 | 29.9 ms                                                                | 38.7 ms: 1.29x slower                                                   |
| async_tree_io              | 863 ms                                                                 | 1.12 sec: 1.30x slower                                                  |
| async_tree_none_tg         | 336 ms                                                                 | 445 ms: 1.32x slower                                                    |
| async_tree_none            | 399 ms                                                                 | 535 ms: 1.34x slower                                                    |
| async_tree_memoization_tg  | 472 ms                                                                 | 645 ms: 1.37x slower                                                    |
| async_tree_memoization     | 481 ms                                                                 | 705 ms: 1.46x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.26x slower                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 247 ms                                                                 | 236 ms: 1.05x faster                                                    |
| float          | 110 ms                                                                 | 151 ms: 1.37x slower                                                    |
| nbody          | 124 ms                                                                 | 177 ms: 1.42x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.23x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 4.72 ms                                                                | 4.49 ms: 1.05x faster                                                   |
| regex_dna      | 270 ms                                                                 | 325 ms: 1.20x slower                                                    |
| regex_compile  | 160 ms                                                                 | 256 ms: 1.59x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 154 ms                                                                 | 143 ms: 1.08x faster                                                    |
| json_dumps           | 15.5 ms                                                                | 18.0 ms: 1.16x slower                                                   |
| xml_etree_generate   | 128 ms                                                                 | 150 ms: 1.17x slower                                                    |
| json_loads           | 35.5 us                                                                | 43.1 us: 1.22x slower                                                   |
| tomli_loads          | 2.58 sec                                                               | 3.20 sec: 1.24x slower                                                  |
| xml_etree_process    | 86.8 ms                                                                | 108 ms: 1.24x slower                                                    |
| pickle_pure_python   | 418 us                                                                 | 615 us: 1.47x slower                                                    |
| unpickle_pure_python | 291 us                                                                 | 475 us: 1.63x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.22x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 28.8 ms                                                                | 36.2 ms: 1.26x slower                                                   |
| python_startup_no_site | 17.0 ms                                                                | 26.0 ms: 1.53x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.39x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                                | 89.7 ms: 1.22x slower                                                   |
| genshi_text     | 30.9 ms                                                                | 41.6 ms: 1.35x slower                                                   |
| django_template | 46.5 ms                                                                | 65.3 ms: 1.41x slower                                                   |
| mako            | 16.5 ms                                                                | 25.5 ms: 1.54x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.37x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| create_gc_cycles           | 4.32 ms                                                                | 3.45 ms: 1.25x faster                                                   |
| gc_traversal               | 9.07 ms                                                                | 8.15 ms: 1.11x faster                                                   |
| xml_etree_iterparse        | 154 ms                                                                 | 143 ms: 1.08x faster                                                    |
| json                       | 7.27 ms                                                                | 6.76 ms: 1.08x faster                                                   |
| regex_effbot               | 4.72 ms                                                                | 4.49 ms: 1.05x faster                                                   |
| pidigits                   | 247 ms                                                                 | 236 ms: 1.05x faster                                                    |
| sqlite_synth               | 3.58 us                                                                | 3.82 us: 1.07x slower                                                   |
| k_core                     | 4.08 sec                                                               | 4.45 sec: 1.09x slower                                                  |
| asyncio_websockets         | 749 ms                                                                 | 827 ms: 1.10x slower                                                    |
| dulwich_log                | 105 ms                                                                 | 119 ms: 1.14x slower                                                    |
| async_tree_io_tg           | 857 ms                                                                 | 996 ms: 1.16x slower                                                    |
| json_dumps                 | 15.5 ms                                                                | 18.0 ms: 1.16x slower                                                   |
| connected_components       | 810 ms                                                                 | 946 ms: 1.17x slower                                                    |
| xml_etree_generate         | 128 ms                                                                 | 150 ms: 1.17x slower                                                    |
| spectral_norm              | 149 ms                                                                 | 175 ms: 1.17x slower                                                    |
| async_tree_cpu_io_mixed    | 719 ms                                                                 | 849 ms: 1.18x slower                                                    |
| pathlib                    | 28.3 ms                                                                | 33.5 ms: 1.18x slower                                                   |
| async_tree_cpu_io_mixed_tg | 676 ms                                                                 | 806 ms: 1.19x slower                                                    |
| async_generators           | 569 ms                                                                 | 681 ms: 1.20x slower                                                    |
| regex_dna                  | 270 ms                                                                 | 325 ms: 1.20x slower                                                    |
| logging_format             | 10.1 us                                                                | 12.2 us: 1.21x slower                                                   |
| pycparser                  | 1.54 sec                                                               | 1.86 sec: 1.21x slower                                                  |
| telco                      | 9.58 ms                                                                | 11.6 ms: 1.21x slower                                                   |
| json_loads                 | 35.5 us                                                                | 43.1 us: 1.22x slower                                                   |
| genshi_xml                 | 73.6 ms                                                                | 89.7 ms: 1.22x slower                                                   |
| docutils                   | 3.92 sec                                                               | 4.79 sec: 1.22x slower                                                  |
| nqueens                    | 110 ms                                                                 | 134 ms: 1.22x slower                                                    |
| mdp                        | 3.96 sec                                                               | 4.89 sec: 1.23x slower                                                  |
| coverage                   | 108 ms                                                                 | 133 ms: 1.24x slower                                                    |
| scimark_fft                | 444 ms                                                                 | 549 ms: 1.24x slower                                                    |
| tomli_loads                | 2.58 sec                                                               | 3.20 sec: 1.24x slower                                                  |
| xml_etree_process          | 86.8 ms                                                                | 108 ms: 1.24x slower                                                    |
| deepcopy                   | 360 us                                                                 | 449 us: 1.25x slower                                                    |
| meteor_contest             | 142 ms                                                                 | 178 ms: 1.26x slower                                                    |
| python_startup             | 28.8 ms                                                                | 36.2 ms: 1.26x slower                                                   |
| shortest_path              | 929 ms                                                                 | 1.17 sec: 1.26x slower                                                  |
| scimark_lu                 | 160 ms                                                                 | 201 ms: 1.26x slower                                                    |
| sphinx                     | 1.48 sec                                                               | 1.87 sec: 1.27x slower                                                  |
| fannkuch                   | 540 ms                                                                 | 684 ms: 1.27x slower                                                    |
| sympy_integrate            | 31.0 ms                                                                | 39.8 ms: 1.28x slower                                                   |
| sqlglot_normalize          | 140 ms                                                                 | 180 ms: 1.29x slower                                                    |
| coroutines                 | 29.9 ms                                                                | 38.7 ms: 1.29x slower                                                   |
| pylint                     | 384 ms                                                                 | 498 ms: 1.29x slower                                                    |
| deepcopy_reduce            | 3.77 us                                                                | 4.89 us: 1.30x slower                                                   |
| async_tree_io              | 863 ms                                                                 | 1.12 sec: 1.30x slower                                                  |
| sympy_expand               | 585 ms                                                                 | 762 ms: 1.30x slower                                                    |
| sqlglot_optimize           | 75.0 ms                                                                | 98.4 ms: 1.31x slower                                                   |
| async_tree_none_tg         | 336 ms                                                                 | 445 ms: 1.32x slower                                                    |
| async_tree_none            | 399 ms                                                                 | 535 ms: 1.34x slower                                                    |
| pyflate                    | 692 ms                                                                 | 928 ms: 1.34x slower                                                    |
| deepcopy_memo              | 42.7 us                                                                | 57.4 us: 1.34x slower                                                   |
| genshi_text                | 30.9 ms                                                                | 41.6 ms: 1.35x slower                                                   |
| sympy_sum                  | 217 ms                                                                 | 293 ms: 1.35x slower                                                    |
| async_tree_memoization_tg  | 472 ms                                                                 | 645 ms: 1.37x slower                                                    |
| float                      | 110 ms                                                                 | 151 ms: 1.37x slower                                                    |
| scimark_sparse_mat_mult    | 6.73 ms                                                                | 9.40 ms: 1.40x slower                                                   |
| django_template            | 46.5 ms                                                                | 65.3 ms: 1.41x slower                                                   |
| 2to3                       | 466 ms                                                                 | 660 ms: 1.42x slower                                                    |
| nbody                      | 124 ms                                                                 | 177 ms: 1.42x slower                                                    |
| richards                   | 57.2 ms                                                                | 83.0 ms: 1.45x slower                                                   |
| async_tree_memoization     | 481 ms                                                                 | 705 ms: 1.46x slower                                                    |
| pickle_pure_python         | 418 us                                                                 | 615 us: 1.47x slower                                                    |
| generators                 | 38.7 ms                                                                | 57.7 ms: 1.49x slower                                                   |
| logging_simple             | 8.26 us                                                                | 12.4 us: 1.50x slower                                                   |
| pprint_pformat             | 1.89 sec                                                               | 2.83 sec: 1.50x slower                                                  |
| sympy_str                  | 341 ms                                                                 | 513 ms: 1.50x slower                                                    |
| pprint_safe_repr           | 930 ms                                                                 | 1.40 sec: 1.51x slower                                                  |
| scimark_sor                | 163 ms                                                                 | 249 ms: 1.52x slower                                                    |
| python_startup_no_site     | 17.0 ms                                                                | 26.0 ms: 1.53x slower                                                   |
| crypto_pyaes               | 86.4 ms                                                                | 133 ms: 1.54x slower                                                    |
| bench_thread_pool          | 3.39 ms                                                                | 5.23 ms: 1.54x slower                                                   |
| mako                       | 16.5 ms                                                                | 25.5 ms: 1.54x slower                                                   |
| bpe_tokeniser              | 5.69 sec                                                               | 8.78 sec: 1.54x slower                                                  |
| chaos                      | 83.9 ms                                                                | 131 ms: 1.57x slower                                                    |
| sqlalchemy_declarative     | 184 ms                                                                 | 289 ms: 1.57x slower                                                    |
| typing_runtime_protocols   | 206 us                                                                 | 326 us: 1.58x slower                                                    |
| regex_compile              | 160 ms                                                                 | 256 ms: 1.59x slower                                                    |
| scimark_monte_carlo        | 92.8 ms                                                                | 148 ms: 1.60x slower                                                    |
| many_optionals             | 1.08 ms                                                                | 1.74 ms: 1.61x slower                                                   |
| logging_silent             | 137 ns                                                                 | 222 ns: 1.62x slower                                                    |
| unpickle_pure_python       | 291 us                                                                 | 475 us: 1.63x slower                                                    |
| thrift                     | 974 us                                                                 | 1.60 ms: 1.64x slower                                                   |
| hexiom                     | 8.33 ms                                                                | 13.8 ms: 1.65x slower                                                   |
| go                         | 162 ms                                                                 | 269 ms: 1.66x slower                                                    |
| html5lib                   | 77.5 ms                                                                | 133 ms: 1.71x slower                                                    |
| sqlalchemy_imperative      | 22.1 ms                                                                | 39.1 ms: 1.77x slower                                                   |
| raytrace                   | 364 ms                                                                 | 659 ms: 1.81x slower                                                    |
| subparsers                 | 31.1 ms                                                                | 56.7 ms: 1.82x slower                                                   |
| richards_super             | 63.2 ms                                                                | 116 ms: 1.84x slower                                                    |
| sqlglot_transpile          | 2.04 ms                                                                | 3.80 ms: 1.86x slower                                                   |
| comprehensions             | 21.2 us                                                                | 39.7 us: 1.87x slower                                                   |
| sqlglot_parse              | 1.62 ms                                                                | 3.37 ms: 2.07x slower                                                   |
| deltablue                  | 4.21 ms                                                                | 10.6 ms: 2.51x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.34x slower                                                            |

Benchmark hidden because not significant (3): regex_v8, bench_mp_pool, xml_etree_parse

- Geometric mean (including insignificant results): 1.245x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.19x