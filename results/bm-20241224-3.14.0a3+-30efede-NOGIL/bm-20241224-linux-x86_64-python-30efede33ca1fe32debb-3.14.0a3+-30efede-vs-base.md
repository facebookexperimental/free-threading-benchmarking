# Results vs. base

- fork: python
- ref: 30efede33ca1fe32debb
- machine: linux-x86_64
- commit hash: 30efede
- commit date: 2024-12-24
- overall geometric mean: 1.209x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 447 ms                                                                                                            | 612 ms: 1.37x slower                                                                                                    |
| docutils       | 3.78 sec                                                                                                          | 4.40 sec: 1.16x slower                                                                                                  |
| html5lib       | 91.1 ms                                                                                                           | 131 ms: 1.44x slower                                                                                                    |
| sphinx         | 1.43 sec                                                                                                          | 1.76 sec: 1.23x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.29x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 905 ms                                                                                                            | 964 ms: 1.06x slower                                                                                                    |
| async_tree_none_tg         | 383 ms                                                                                                            | 421 ms: 1.10x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 697 ms                                                                                                            | 776 ms: 1.11x slower                                                                                                    |
| async_tree_io              | 927 ms                                                                                                            | 1.06 sec: 1.14x slower                                                                                                  |
| coroutines                 | 30.6 ms                                                                                                           | 35.0 ms: 1.14x slower                                                                                                   |
| async_generators           | 561 ms                                                                                                            | 658 ms: 1.17x slower                                                                                                    |
| async_tree_memoization_tg  | 473 ms                                                                                                            | 571 ms: 1.21x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 686 ms                                                                                                            | 857 ms: 1.25x slower                                                                                                    |
| async_tree_memoization     | 524 ms                                                                                                            | 671 ms: 1.28x slower                                                                                                    |
| async_tree_none            | 390 ms                                                                                                            | 504 ms: 1.29x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 115 ms                                                                                                            | 147 ms: 1.27x slower                                                                                                    |
| nbody          | 129 ms                                                                                                            | 177 ms: 1.37x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 4.26 ms                                                                                                           | 4.76 ms: 1.12x slower                                                                                                   |
| regex_dna      | 267 ms                                                                                                            | 300 ms: 1.13x slower                                                                                                    |
| regex_compile  | 176 ms                                                                                                            | 219 ms: 1.25x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| json_loads           | 35.9 us                                                                                                           | 37.6 us: 1.05x slower                                                                                                   |
| xml_etree_parse      | 207 ms                                                                                                            | 222 ms: 1.07x slower                                                                                                    |
| json_dumps           | 16.0 ms                                                                                                           | 17.6 ms: 1.10x slower                                                                                                   |
| xml_etree_process    | 85.3 ms                                                                                                           | 101 ms: 1.19x slower                                                                                                    |
| tomli_loads          | 2.61 sec                                                                                                          | 3.25 sec: 1.25x slower                                                                                                  |
| xml_etree_generate   | 116 ms                                                                                                            | 147 ms: 1.27x slower                                                                                                    |
| unpickle_pure_python | 292 us                                                                                                            | 418 us: 1.43x slower                                                                                                    |
| pickle_pure_python   | 441 us                                                                                                            | 654 us: 1.48x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 26.0 ms                                                                                                           | 31.0 ms: 1.19x slower                                                                                                   |
| python_startup_no_site | 14.8 ms                                                                                                           | 20.4 ms: 1.38x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.28x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 48.1 ms                                                                                                           | 59.3 ms: 1.23x slower                                                                                                   |
| genshi_xml      | 68.9 ms                                                                                                           | 87.7 ms: 1.27x slower                                                                                                   |
| genshi_text     | 31.0 ms                                                                                                           | 40.0 ms: 1.29x slower                                                                                                   |
| mako            | 16.9 ms                                                                                                           | 26.8 ms: 1.59x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.34x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 9.27 ms                                                                                                           | 6.85 ms: 1.35x faster                                                                                                   |
| create_gc_cycles           | 3.90 ms                                                                                                           | 3.38 ms: 1.15x faster                                                                                                   |
| json_loads                 | 35.9 us                                                                                                           | 37.6 us: 1.05x slower                                                                                                   |
| async_tree_io_tg           | 905 ms                                                                                                            | 964 ms: 1.06x slower                                                                                                    |
| json                       | 6.58 ms                                                                                                           | 7.04 ms: 1.07x slower                                                                                                   |
| xml_etree_parse            | 207 ms                                                                                                            | 222 ms: 1.07x slower                                                                                                    |
| k_core                     | 4.21 sec                                                                                                          | 4.53 sec: 1.08x slower                                                                                                  |
| pathlib                    | 28.5 ms                                                                                                           | 31.3 ms: 1.10x slower                                                                                                   |
| async_tree_none_tg         | 383 ms                                                                                                            | 421 ms: 1.10x slower                                                                                                    |
| json_dumps                 | 16.0 ms                                                                                                           | 17.6 ms: 1.10x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 697 ms                                                                                                            | 776 ms: 1.11x slower                                                                                                    |
| regex_effbot               | 4.26 ms                                                                                                           | 4.76 ms: 1.12x slower                                                                                                   |
| regex_dna                  | 267 ms                                                                                                            | 300 ms: 1.13x slower                                                                                                    |
| shortest_path              | 923 ms                                                                                                            | 1.05 sec: 1.13x slower                                                                                                  |
| async_tree_io              | 927 ms                                                                                                            | 1.06 sec: 1.14x slower                                                                                                  |
| coroutines                 | 30.6 ms                                                                                                           | 35.0 ms: 1.14x slower                                                                                                   |
| spectral_norm              | 144 ms                                                                                                            | 165 ms: 1.15x slower                                                                                                    |
| sqlglot_optimize           | 79.0 ms                                                                                                           | 91.1 ms: 1.15x slower                                                                                                   |
| connected_components       | 834 ms                                                                                                            | 967 ms: 1.16x slower                                                                                                    |
| docutils                   | 3.78 sec                                                                                                          | 4.40 sec: 1.16x slower                                                                                                  |
| pycparser                  | 1.61 sec                                                                                                          | 1.87 sec: 1.17x slower                                                                                                  |
| async_generators           | 561 ms                                                                                                            | 658 ms: 1.17x slower                                                                                                    |
| dulwich_log                | 98.0 ms                                                                                                           | 115 ms: 1.17x slower                                                                                                    |
| sympy_expand               | 609 ms                                                                                                            | 718 ms: 1.18x slower                                                                                                    |
| xml_etree_process          | 85.3 ms                                                                                                           | 101 ms: 1.19x slower                                                                                                    |
| deepcopy                   | 343 us                                                                                                            | 408 us: 1.19x slower                                                                                                    |
| python_startup             | 26.0 ms                                                                                                           | 31.0 ms: 1.19x slower                                                                                                   |
| nqueens                    | 109 ms                                                                                                            | 130 ms: 1.19x slower                                                                                                    |
| async_tree_memoization_tg  | 473 ms                                                                                                            | 571 ms: 1.21x slower                                                                                                    |
| mdp                        | 3.64 sec                                                                                                          | 4.39 sec: 1.21x slower                                                                                                  |
| meteor_contest             | 149 ms                                                                                                            | 181 ms: 1.22x slower                                                                                                    |
| many_optionals             | 1.20 ms                                                                                                           | 1.46 ms: 1.22x slower                                                                                                   |
| sphinx                     | 1.43 sec                                                                                                          | 1.76 sec: 1.23x slower                                                                                                  |
| sympy_str                  | 378 ms                                                                                                            | 464 ms: 1.23x slower                                                                                                    |
| scimark_fft                | 449 ms                                                                                                            | 551 ms: 1.23x slower                                                                                                    |
| django_template            | 48.1 ms                                                                                                           | 59.3 ms: 1.23x slower                                                                                                   |
| deepcopy_reduce            | 3.70 us                                                                                                           | 4.57 us: 1.23x slower                                                                                                   |
| coverage                   | 110 ms                                                                                                            | 136 ms: 1.24x slower                                                                                                    |
| tomli_loads                | 2.61 sec                                                                                                          | 3.25 sec: 1.25x slower                                                                                                  |
| regex_compile              | 176 ms                                                                                                            | 219 ms: 1.25x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 686 ms                                                                                                            | 857 ms: 1.25x slower                                                                                                    |
| telco                      | 10.3 ms                                                                                                           | 13.0 ms: 1.26x slower                                                                                                   |
| sympy_integrate            | 28.4 ms                                                                                                           | 35.8 ms: 1.26x slower                                                                                                   |
| typing_runtime_protocols   | 220 us                                                                                                            | 278 us: 1.27x slower                                                                                                    |
| xml_etree_generate         | 116 ms                                                                                                            | 147 ms: 1.27x slower                                                                                                    |
| pylint                     | 401 ms                                                                                                            | 509 ms: 1.27x slower                                                                                                    |
| float                      | 115 ms                                                                                                            | 147 ms: 1.27x slower                                                                                                    |
| genshi_xml                 | 68.9 ms                                                                                                           | 87.7 ms: 1.27x slower                                                                                                   |
| thrift                     | 1.01 ms                                                                                                           | 1.29 ms: 1.27x slower                                                                                                   |
| async_tree_memoization     | 524 ms                                                                                                            | 671 ms: 1.28x slower                                                                                                    |
| sympy_sum                  | 203 ms                                                                                                            | 260 ms: 1.28x slower                                                                                                    |
| genshi_text                | 31.0 ms                                                                                                           | 40.0 ms: 1.29x slower                                                                                                   |
| async_tree_none            | 390 ms                                                                                                            | 504 ms: 1.29x slower                                                                                                    |
| scimark_sparse_mat_mult    | 6.27 ms                                                                                                           | 8.18 ms: 1.30x slower                                                                                                   |
| deepcopy_memo              | 39.5 us                                                                                                           | 52.2 us: 1.32x slower                                                                                                   |
| generators                 | 39.6 ms                                                                                                           | 53.2 ms: 1.34x slower                                                                                                   |
| crypto_pyaes               | 94.0 ms                                                                                                           | 126 ms: 1.34x slower                                                                                                    |
| scimark_lu                 | 147 ms                                                                                                            | 198 ms: 1.34x slower                                                                                                    |
| sqlalchemy_declarative     | 179 ms                                                                                                            | 242 ms: 1.35x slower                                                                                                    |
| bpe_tokeniser              | 6.01 sec                                                                                                          | 8.12 sec: 1.35x slower                                                                                                  |
| fannkuch                   | 514 ms                                                                                                            | 697 ms: 1.36x slower                                                                                                    |
| pprint_pformat             | 1.92 sec                                                                                                          | 2.62 sec: 1.36x slower                                                                                                  |
| pyflate                    | 684 ms                                                                                                            | 930 ms: 1.36x slower                                                                                                    |
| 2to3                       | 447 ms                                                                                                            | 612 ms: 1.37x slower                                                                                                    |
| pprint_safe_repr           | 936 ms                                                                                                            | 1.28 sec: 1.37x slower                                                                                                  |
| nbody                      | 129 ms                                                                                                            | 177 ms: 1.37x slower                                                                                                    |
| python_startup_no_site     | 14.8 ms                                                                                                           | 20.4 ms: 1.38x slower                                                                                                   |
| sqlglot_normalize          | 130 ms                                                                                                            | 179 ms: 1.38x slower                                                                                                    |
| bench_thread_pool          | 3.13 ms                                                                                                           | 4.32 ms: 1.38x slower                                                                                                   |
| unpickle_pure_python       | 292 us                                                                                                            | 418 us: 1.43x slower                                                                                                    |
| html5lib                   | 91.1 ms                                                                                                           | 131 ms: 1.44x slower                                                                                                    |
| hexiom                     | 8.87 ms                                                                                                           | 13.0 ms: 1.46x slower                                                                                                   |
| logging_format             | 8.76 us                                                                                                           | 12.9 us: 1.47x slower                                                                                                   |
| pickle_pure_python         | 441 us                                                                                                            | 654 us: 1.48x slower                                                                                                    |
| richards                   | 59.0 ms                                                                                                           | 87.7 ms: 1.49x slower                                                                                                   |
| logging_simple             | 7.60 us                                                                                                           | 11.5 us: 1.51x slower                                                                                                   |
| richards_super             | 63.9 ms                                                                                                           | 96.8 ms: 1.51x slower                                                                                                   |
| chaos                      | 85.1 ms                                                                                                           | 129 ms: 1.52x slower                                                                                                    |
| subparsers                 | 29.6 ms                                                                                                           | 45.0 ms: 1.52x slower                                                                                                   |
| comprehensions             | 22.3 us                                                                                                           | 34.7 us: 1.56x slower                                                                                                   |
| mako                       | 16.9 ms                                                                                                           | 26.8 ms: 1.59x slower                                                                                                   |
| logging_silent             | 139 ns                                                                                                            | 222 ns: 1.60x slower                                                                                                    |
| scimark_monte_carlo        | 88.6 ms                                                                                                           | 142 ms: 1.61x slower                                                                                                    |
| sqlalchemy_imperative      | 22.7 ms                                                                                                           | 36.7 ms: 1.62x slower                                                                                                   |
| sqlglot_transpile          | 2.12 ms                                                                                                           | 3.60 ms: 1.70x slower                                                                                                   |
| go                         | 168 ms                                                                                                            | 289 ms: 1.72x slower                                                                                                    |
| sqlglot_parse              | 1.68 ms                                                                                                           | 2.94 ms: 1.75x slower                                                                                                   |
| raytrace                   | 345 ms                                                                                                            | 607 ms: 1.76x slower                                                                                                    |
| scimark_sor                | 153 ms                                                                                                            | 272 ms: 1.77x slower                                                                                                    |
| deltablue                  | 4.51 ms                                                                                                           | 11.0 ms: 2.43x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.27x slower                                                                                                            |

Benchmark hidden because not significant (6): sqlite_synth, xml_etree_iterparse, pidigits, bench_mp_pool, regex_v8, asyncio_websockets

- Geometric mean (including insignificant results): 1.209x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.18x