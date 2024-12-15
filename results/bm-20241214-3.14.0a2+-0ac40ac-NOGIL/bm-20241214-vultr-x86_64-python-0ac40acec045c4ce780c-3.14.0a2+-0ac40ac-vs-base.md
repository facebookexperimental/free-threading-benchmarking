# Results vs. base

- fork: python
- ref: 0ac40acec045c4ce780c
- machine: linux-x86_64
- commit hash: 0ac40ac
- commit date: 2024-12-14
- overall geometric mean: 1.265x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                                                            | 363 ms: 1.42x slower                                                                                                    |
| docutils       | 2.54 sec                                                                                                          | 3.06 sec: 1.20x slower                                                                                                  |
| sphinx         | 992 ms                                                                                                            | 1.17 sec: 1.18x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.26x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| coroutines                 | 22.1 ms                                                                                                           | 24.4 ms: 1.10x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 480 ms                                                                                                            | 604 ms: 1.26x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 496 ms                                                                                                            | 625 ms: 1.26x slower                                                                                                    |
| async_generators           | 358 ms                                                                                                            | 455 ms: 1.27x slower                                                                                                    |
| async_tree_io              | 623 ms                                                                                                            | 807 ms: 1.30x slower                                                                                                    |
| async_tree_io_tg           | 606 ms                                                                                                            | 791 ms: 1.31x slower                                                                                                    |
| async_tree_none_tg         | 257 ms                                                                                                            | 345 ms: 1.34x slower                                                                                                    |
| async_tree_none            | 276 ms                                                                                                            | 374 ms: 1.35x slower                                                                                                    |
| async_tree_memoization     | 335 ms                                                                                                            | 457 ms: 1.36x slower                                                                                                    |
| async_tree_memoization_tg  | 307 ms                                                                                                            | 431 ms: 1.40x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.26x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                                                            | 181 ms: 1.03x faster                                                                                                    |
| nbody          | 90.7 ms                                                                                                           | 131 ms: 1.45x slower                                                                                                    |
| float          | 76.8 ms                                                                                                           | 134 ms: 1.75x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.35x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 2.72 ms                                                                                                           | 2.86 ms: 1.05x slower                                                                                                   |
| regex_v8       | 23.2 ms                                                                                                           | 25.2 ms: 1.09x slower                                                                                                   |
| regex_dna      | 167 ms                                                                                                            | 187 ms: 1.12x slower                                                                                                    |
| regex_compile  | 127 ms                                                                                                            | 175 ms: 1.38x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.8 ms                                                                                                           | 89.6 ms: 1.01x faster                                                                                                   |
| xml_etree_parse      | 129 ms                                                                                                            | 131 ms: 1.01x slower                                                                                                    |
| json_loads           | 26.4 us                                                                                                           | 28.5 us: 1.08x slower                                                                                                   |
| xml_etree_generate   | 83.8 ms                                                                                                           | 97.0 ms: 1.16x slower                                                                                                   |
| json_dumps           | 11.4 ms                                                                                                           | 14.0 ms: 1.23x slower                                                                                                   |
| tomli_loads          | 1.99 sec                                                                                                          | 2.60 sec: 1.31x slower                                                                                                  |
| xml_etree_process    | 58.6 ms                                                                                                           | 78.8 ms: 1.34x slower                                                                                                   |
| pickle_pure_python   | 319 us                                                                                                            | 501 us: 1.57x slower                                                                                                    |
| unpickle_pure_python | 212 us                                                                                                            | 335 us: 1.58x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.24x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                                                           | 17.1 ms: 1.17x slower                                                                                                   |
| python_startup_no_site | 7.46 ms                                                                                                           | 10.2 ms: 1.37x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.27x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 50.6 ms                                                                                                           | 63.1 ms: 1.25x slower                                                                                                   |
| django_template | 35.5 ms                                                                                                           | 49.3 ms: 1.39x slower                                                                                                   |
| genshi_text     | 21.5 ms                                                                                                           | 31.0 ms: 1.44x slower                                                                                                   |
| mako            | 11.5 ms                                                                                                           | 16.9 ms: 1.47x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.38x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.16 ms                                                                                                           | 3.15 ms: 1.32x faster                                                                                                   |
| pidigits                   | 186 ms                                                                                                            | 181 ms: 1.03x faster                                                                                                    |
| xml_etree_iterparse        | 90.8 ms                                                                                                           | 89.6 ms: 1.01x faster                                                                                                   |
| create_gc_cycles           | 1.82 ms                                                                                                           | 1.80 ms: 1.01x faster                                                                                                   |
| xml_etree_parse            | 129 ms                                                                                                            | 131 ms: 1.01x slower                                                                                                    |
| json                       | 4.82 ms                                                                                                           | 5.03 ms: 1.04x slower                                                                                                   |
| regex_effbot               | 2.72 ms                                                                                                           | 2.86 ms: 1.05x slower                                                                                                   |
| json_loads                 | 26.4 us                                                                                                           | 28.5 us: 1.08x slower                                                                                                   |
| regex_v8                   | 23.2 ms                                                                                                           | 25.2 ms: 1.09x slower                                                                                                   |
| pathlib                    | 18.1 ms                                                                                                           | 19.8 ms: 1.09x slower                                                                                                   |
| coroutines                 | 22.1 ms                                                                                                           | 24.4 ms: 1.10x slower                                                                                                   |
| regex_dna                  | 167 ms                                                                                                            | 187 ms: 1.12x slower                                                                                                    |
| k_core                     | 2.06 sec                                                                                                          | 2.35 sec: 1.14x slower                                                                                                  |
| mdp                        | 2.46 sec                                                                                                          | 2.83 sec: 1.15x slower                                                                                                  |
| spectral_norm              | 98.7 ms                                                                                                           | 114 ms: 1.15x slower                                                                                                    |
| xml_etree_generate         | 83.8 ms                                                                                                           | 97.0 ms: 1.16x slower                                                                                                   |
| bpe_tokeniser              | 4.27 sec                                                                                                          | 5.00 sec: 1.17x slower                                                                                                  |
| python_startup             | 14.6 ms                                                                                                           | 17.1 ms: 1.17x slower                                                                                                   |
| sphinx                     | 992 ms                                                                                                            | 1.17 sec: 1.18x slower                                                                                                  |
| scimark_fft                | 320 ms                                                                                                            | 378 ms: 1.18x slower                                                                                                    |
| telco                      | 7.15 ms                                                                                                           | 8.58 ms: 1.20x slower                                                                                                   |
| docutils                   | 2.54 sec                                                                                                          | 3.06 sec: 1.20x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.54 ms                                                                                                           | 5.51 ms: 1.21x slower                                                                                                   |
| bench_mp_pool              | 88.3 ms                                                                                                           | 108 ms: 1.22x slower                                                                                                    |
| json_dumps                 | 11.4 ms                                                                                                           | 14.0 ms: 1.23x slower                                                                                                   |
| many_optionals             | 1.02 ms                                                                                                           | 1.25 ms: 1.23x slower                                                                                                   |
| dulwich_log                | 76.3 ms                                                                                                           | 94.0 ms: 1.23x slower                                                                                                   |
| connected_components       | 402 ms                                                                                                            | 500 ms: 1.24x slower                                                                                                    |
| shortest_path              | 442 ms                                                                                                            | 551 ms: 1.24x slower                                                                                                    |
| deepcopy                   | 255 us                                                                                                            | 318 us: 1.25x slower                                                                                                    |
| genshi_xml                 | 50.6 ms                                                                                                           | 63.1 ms: 1.25x slower                                                                                                   |
| nqueens                    | 79.9 ms                                                                                                           | 99.9 ms: 1.25x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 480 ms                                                                                                            | 604 ms: 1.26x slower                                                                                                    |
| sqlglot_optimize           | 52.3 ms                                                                                                           | 65.9 ms: 1.26x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 496 ms                                                                                                            | 625 ms: 1.26x slower                                                                                                    |
| async_generators           | 358 ms                                                                                                            | 455 ms: 1.27x slower                                                                                                    |
| sqlglot_normalize          | 104 ms                                                                                                            | 132 ms: 1.27x slower                                                                                                    |
| coverage                   | 78.8 ms                                                                                                           | 101 ms: 1.28x slower                                                                                                    |
| typing_runtime_protocols   | 156 us                                                                                                            | 202 us: 1.29x slower                                                                                                    |
| async_tree_io              | 623 ms                                                                                                            | 807 ms: 1.30x slower                                                                                                    |
| meteor_contest             | 99.3 ms                                                                                                           | 129 ms: 1.30x slower                                                                                                    |
| deepcopy_memo              | 30.2 us                                                                                                           | 39.4 us: 1.30x slower                                                                                                   |
| tomli_loads                | 1.99 sec                                                                                                          | 2.60 sec: 1.31x slower                                                                                                  |
| async_tree_io_tg           | 606 ms                                                                                                            | 791 ms: 1.31x slower                                                                                                    |
| pylint                     | 280 ms                                                                                                            | 369 ms: 1.32x slower                                                                                                    |
| fannkuch                   | 373 ms                                                                                                            | 493 ms: 1.32x slower                                                                                                    |
| async_tree_none_tg         | 257 ms                                                                                                            | 345 ms: 1.34x slower                                                                                                    |
| xml_etree_process          | 58.6 ms                                                                                                           | 78.8 ms: 1.34x slower                                                                                                   |
| deepcopy_reduce            | 2.57 us                                                                                                           | 3.46 us: 1.35x slower                                                                                                   |
| crypto_pyaes               | 66.4 ms                                                                                                           | 89.8 ms: 1.35x slower                                                                                                   |
| async_tree_none            | 276 ms                                                                                                            | 374 ms: 1.35x slower                                                                                                    |
| subparsers                 | 22.2 ms                                                                                                           | 30.2 ms: 1.36x slower                                                                                                   |
| pycparser                  | 1.12 sec                                                                                                          | 1.52 sec: 1.36x slower                                                                                                  |
| async_tree_memoization     | 335 ms                                                                                                            | 457 ms: 1.36x slower                                                                                                    |
| pprint_safe_repr           | 711 ms                                                                                                            | 973 ms: 1.37x slower                                                                                                    |
| python_startup_no_site     | 7.46 ms                                                                                                           | 10.2 ms: 1.37x slower                                                                                                   |
| regex_compile              | 127 ms                                                                                                            | 175 ms: 1.38x slower                                                                                                    |
| pprint_pformat             | 1.46 sec                                                                                                          | 2.02 sec: 1.39x slower                                                                                                  |
| django_template            | 35.5 ms                                                                                                           | 49.3 ms: 1.39x slower                                                                                                   |
| generators                 | 27.4 ms                                                                                                           | 38.2 ms: 1.40x slower                                                                                                   |
| async_tree_memoization_tg  | 307 ms                                                                                                            | 431 ms: 1.40x slower                                                                                                    |
| 2to3                       | 255 ms                                                                                                            | 363 ms: 1.42x slower                                                                                                    |
| genshi_text                | 21.5 ms                                                                                                           | 31.0 ms: 1.44x slower                                                                                                   |
| nbody                      | 90.7 ms                                                                                                           | 131 ms: 1.45x slower                                                                                                    |
| mako                       | 11.5 ms                                                                                                           | 16.9 ms: 1.47x slower                                                                                                   |
| sympy_integrate            | 19.8 ms                                                                                                           | 29.4 ms: 1.48x slower                                                                                                   |
| sqlalchemy_imperative      | 19.1 ms                                                                                                           | 28.9 ms: 1.51x slower                                                                                                   |
| thrift                     | 732 us                                                                                                            | 1.11 ms: 1.51x slower                                                                                                   |
| pickle_pure_python         | 319 us                                                                                                            | 501 us: 1.57x slower                                                                                                    |
| comprehensions             | 17.5 us                                                                                                           | 27.6 us: 1.57x slower                                                                                                   |
| unpickle_pure_python       | 212 us                                                                                                            | 335 us: 1.58x slower                                                                                                    |
| pyflate                    | 422 ms                                                                                                            | 668 ms: 1.58x slower                                                                                                    |
| sqlalchemy_declarative     | 126 ms                                                                                                            | 200 ms: 1.59x slower                                                                                                    |
| logging_format             | 6.88 us                                                                                                           | 11.1 us: 1.61x slower                                                                                                   |
| logging_simple             | 6.10 us                                                                                                           | 9.93 us: 1.63x slower                                                                                                   |
| hexiom                     | 5.94 ms                                                                                                           | 9.82 ms: 1.65x slower                                                                                                   |
| scimark_lu                 | 110 ms                                                                                                            | 183 ms: 1.66x slower                                                                                                    |
| richards_super             | 50.7 ms                                                                                                           | 85.4 ms: 1.68x slower                                                                                                   |
| logging_silent             | 107 ns                                                                                                            | 183 ns: 1.72x slower                                                                                                    |
| richards                   | 44.7 ms                                                                                                           | 77.3 ms: 1.73x slower                                                                                                   |
| float                      | 76.8 ms                                                                                                           | 134 ms: 1.75x slower                                                                                                    |
| sympy_str                  | 272 ms                                                                                                            | 475 ms: 1.75x slower                                                                                                    |
| chaos                      | 58.2 ms                                                                                                           | 104 ms: 1.78x slower                                                                                                    |
| sqlglot_transpile          | 1.59 ms                                                                                                           | 2.91 ms: 1.83x slower                                                                                                   |
| scimark_monte_carlo        | 64.3 ms                                                                                                           | 118 ms: 1.84x slower                                                                                                    |
| scimark_sor                | 125 ms                                                                                                            | 234 ms: 1.88x slower                                                                                                    |
| sqlglot_parse              | 1.28 ms                                                                                                           | 2.56 ms: 2.00x slower                                                                                                   |
| sympy_expand               | 459 ms                                                                                                            | 951 ms: 2.07x slower                                                                                                    |
| raytrace                   | 261 ms                                                                                                            | 552 ms: 2.12x slower                                                                                                    |
| sympy_sum                  | 152 ms                                                                                                            | 348 ms: 2.29x slower                                                                                                    |
| go                         | 117 ms                                                                                                            | 268 ms: 2.30x slower                                                                                                    |
| deltablue                  | 3.14 ms                                                                                                           | 8.25 ms: 2.62x slower                                                                                                   |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.40 ms: 3.28x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.38x slower                                                                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, sqlite_synth
Ignored benchmarks (1) of results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json: html5lib

- Geometric mean (including insignificant results): 1.265x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.19x