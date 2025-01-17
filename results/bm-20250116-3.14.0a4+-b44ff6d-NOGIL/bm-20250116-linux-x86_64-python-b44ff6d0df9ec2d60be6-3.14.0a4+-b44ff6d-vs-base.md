# Results vs. base

- fork: python
- ref: b44ff6d0df9ec2d60be6
- machine: linux-x86_64
- commit hash: b44ff6d
- commit date: 2025-01-16
- overall geometric mean: 1.132x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 479 ms                                                                                                            | 603 ms: 1.26x slower                                                                                                    |
| docutils       | 3.60 sec                                                                                                          | 4.11 sec: 1.14x slower                                                                                                  |
| html5lib       | 87.3 ms                                                                                                           | 107 ms: 1.22x slower                                                                                                    |
| sphinx         | 1.43 sec                                                                                                          | 1.71 sec: 1.19x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 939 ms                                                                                                            | 775 ms: 1.21x faster                                                                                                    |
| async_tree_none_tg         | 392 ms                                                                                                            | 347 ms: 1.13x faster                                                                                                    |
| async_tree_io              | 921 ms                                                                                                            | 835 ms: 1.10x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 727 ms                                                                                                            | 673 ms: 1.08x faster                                                                                                    |
| async_tree_cpu_io_mixed    | 731 ms                                                                                                            | 776 ms: 1.06x slower                                                                                                    |
| coroutines                 | 31.8 ms                                                                                                           | 34.0 ms: 1.07x slower                                                                                                   |
| async_tree_memoization     | 492 ms                                                                                                            | 534 ms: 1.09x slower                                                                                                    |
| async_generators           | 544 ms                                                                                                            | 603 ms: 1.11x slower                                                                                                    |
| async_tree_none            | 375 ms                                                                                                            | 456 ms: 1.21x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.00x faster                                                                                                            |

Benchmark hidden because not significant (2): async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 129 ms                                                                                                            | 176 ms: 1.37x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 4.23 ms                                                                                                           | 4.65 ms: 1.10x slower                                                                                                   |
| regex_compile  | 178 ms                                                                                                            | 196 ms: 1.10x slower                                                                                                    |
| regex_dna      | 270 ms                                                                                                            | 304 ms: 1.13x slower                                                                                                    |
| regex_v8       | 30.6 ms                                                                                                           | 35.3 ms: 1.15x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 162 ms                                                                                                            | 144 ms: 1.12x faster                                                                                                    |
| json_dumps           | 16.3 ms                                                                                                           | 17.2 ms: 1.05x slower                                                                                                   |
| xml_etree_parse      | 206 ms                                                                                                            | 225 ms: 1.09x slower                                                                                                    |
| unpickle_pure_python | 308 us                                                                                                            | 341 us: 1.11x slower                                                                                                    |
| tomli_loads          | 2.64 sec                                                                                                          | 2.99 sec: 1.13x slower                                                                                                  |
| xml_etree_generate   | 119 ms                                                                                                            | 140 ms: 1.17x slower                                                                                                    |
| pickle_pure_python   | 434 us                                                                                                            | 527 us: 1.22x slower                                                                                                    |
| json_loads           | 36.6 us                                                                                                           | 44.7 us: 1.22x slower                                                                                                   |
| xml_etree_process    | 88.6 ms                                                                                                           | 110 ms: 1.24x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 28.2 ms                                                                                                           | 37.0 ms: 1.31x slower                                                                                                   |
| python_startup_no_site | 16.7 ms                                                                                                           | 24.2 ms: 1.45x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.38x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 49.3 ms                                                                                                           | 58.6 ms: 1.19x slower                                                                                                   |
| genshi_text     | 30.9 ms                                                                                                           | 38.5 ms: 1.25x slower                                                                                                   |
| mako            | 17.7 ms                                                                                                           | 24.8 ms: 1.40x slower                                                                                                   |
| genshi_xml      | 67.8 ms                                                                                                           | 96.8 ms: 1.43x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.31x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250116-3.14.0a4+-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json | results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles           | 4.11 ms                                                                                                           | 2.98 ms: 1.38x faster                                                                                                   |
| async_tree_io_tg           | 939 ms                                                                                                            | 775 ms: 1.21x faster                                                                                                    |
| gc_traversal               | 9.29 ms                                                                                                           | 7.85 ms: 1.18x faster                                                                                                   |
| sqlite_synth               | 4.06 us                                                                                                           | 3.48 us: 1.17x faster                                                                                                   |
| async_tree_none_tg         | 392 ms                                                                                                            | 347 ms: 1.13x faster                                                                                                    |
| xml_etree_iterparse        | 162 ms                                                                                                            | 144 ms: 1.12x faster                                                                                                    |
| async_tree_io              | 921 ms                                                                                                            | 835 ms: 1.10x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 727 ms                                                                                                            | 673 ms: 1.08x faster                                                                                                    |
| json_dumps                 | 16.3 ms                                                                                                           | 17.2 ms: 1.05x slower                                                                                                   |
| scimark_sor                | 175 ms                                                                                                            | 185 ms: 1.06x slower                                                                                                    |
| k_core                     | 4.20 sec                                                                                                          | 4.46 sec: 1.06x slower                                                                                                  |
| json                       | 7.84 ms                                                                                                           | 8.31 ms: 1.06x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 731 ms                                                                                                            | 776 ms: 1.06x slower                                                                                                    |
| coroutines                 | 31.8 ms                                                                                                           | 34.0 ms: 1.07x slower                                                                                                   |
| nqueens                    | 113 ms                                                                                                            | 122 ms: 1.09x slower                                                                                                    |
| async_tree_memoization     | 492 ms                                                                                                            | 534 ms: 1.09x slower                                                                                                    |
| xml_etree_parse            | 206 ms                                                                                                            | 225 ms: 1.09x slower                                                                                                    |
| spectral_norm              | 142 ms                                                                                                            | 155 ms: 1.09x slower                                                                                                    |
| regex_effbot               | 4.23 ms                                                                                                           | 4.65 ms: 1.10x slower                                                                                                   |
| pathlib                    | 27.8 ms                                                                                                           | 30.7 ms: 1.10x slower                                                                                                   |
| telco                      | 10.8 ms                                                                                                           | 11.9 ms: 1.10x slower                                                                                                   |
| regex_compile              | 178 ms                                                                                                            | 196 ms: 1.10x slower                                                                                                    |
| unpickle_pure_python       | 308 us                                                                                                            | 341 us: 1.11x slower                                                                                                    |
| async_generators           | 544 ms                                                                                                            | 603 ms: 1.11x slower                                                                                                    |
| sympy_sum                  | 219 ms                                                                                                            | 244 ms: 1.11x slower                                                                                                    |
| pyflate                    | 662 ms                                                                                                            | 739 ms: 1.12x slower                                                                                                    |
| logging_silent             | 139 ns                                                                                                            | 156 ns: 1.12x slower                                                                                                    |
| regex_dna                  | 270 ms                                                                                                            | 304 ms: 1.13x slower                                                                                                    |
| raytrace                   | 386 ms                                                                                                            | 435 ms: 1.13x slower                                                                                                    |
| tomli_loads                | 2.64 sec                                                                                                          | 2.99 sec: 1.13x slower                                                                                                  |
| sqlglot_optimize           | 74.7 ms                                                                                                           | 84.7 ms: 1.13x slower                                                                                                   |
| go                         | 164 ms                                                                                                            | 186 ms: 1.14x slower                                                                                                    |
| sympy_integrate            | 29.9 ms                                                                                                           | 34.1 ms: 1.14x slower                                                                                                   |
| docutils                   | 3.60 sec                                                                                                          | 4.11 sec: 1.14x slower                                                                                                  |
| connected_components       | 825 ms                                                                                                            | 943 ms: 1.14x slower                                                                                                    |
| comprehensions             | 24.0 us                                                                                                           | 27.5 us: 1.15x slower                                                                                                   |
| sqlglot_transpile          | 2.16 ms                                                                                                           | 2.49 ms: 1.15x slower                                                                                                   |
| logging_simple             | 8.03 us                                                                                                           | 9.26 us: 1.15x slower                                                                                                   |
| regex_v8                   | 30.6 ms                                                                                                           | 35.3 ms: 1.15x slower                                                                                                   |
| shortest_path              | 941 ms                                                                                                            | 1.09 sec: 1.16x slower                                                                                                  |
| coverage                   | 113 ms                                                                                                            | 132 ms: 1.16x slower                                                                                                    |
| meteor_contest             | 150 ms                                                                                                            | 175 ms: 1.17x slower                                                                                                    |
| pylint                     | 408 ms                                                                                                            | 477 ms: 1.17x slower                                                                                                    |
| xml_etree_generate         | 119 ms                                                                                                            | 140 ms: 1.17x slower                                                                                                    |
| generators                 | 39.1 ms                                                                                                           | 46.0 ms: 1.18x slower                                                                                                   |
| dulwich_log                | 101 ms                                                                                                            | 118 ms: 1.18x slower                                                                                                    |
| scimark_lu                 | 150 ms                                                                                                            | 177 ms: 1.18x slower                                                                                                    |
| django_template            | 49.3 ms                                                                                                           | 58.6 ms: 1.19x slower                                                                                                   |
| sphinx                     | 1.43 sec                                                                                                          | 1.71 sec: 1.19x slower                                                                                                  |
| pprint_safe_repr           | 945 ms                                                                                                            | 1.14 sec: 1.20x slower                                                                                                  |
| mdp                        | 3.54 sec                                                                                                          | 4.29 sec: 1.21x slower                                                                                                  |
| async_tree_none            | 375 ms                                                                                                            | 456 ms: 1.21x slower                                                                                                    |
| pickle_pure_python         | 434 us                                                                                                            | 527 us: 1.22x slower                                                                                                    |
| json_loads                 | 36.6 us                                                                                                           | 44.7 us: 1.22x slower                                                                                                   |
| html5lib                   | 87.3 ms                                                                                                           | 107 ms: 1.22x slower                                                                                                    |
| chaos                      | 83.6 ms                                                                                                           | 103 ms: 1.23x slower                                                                                                    |
| sympy_expand               | 618 ms                                                                                                            | 763 ms: 1.23x slower                                                                                                    |
| xml_etree_process          | 88.6 ms                                                                                                           | 110 ms: 1.24x slower                                                                                                    |
| genshi_text                | 30.9 ms                                                                                                           | 38.5 ms: 1.25x slower                                                                                                   |
| fannkuch                   | 499 ms                                                                                                            | 622 ms: 1.25x slower                                                                                                    |
| pprint_pformat             | 1.89 sec                                                                                                          | 2.35 sec: 1.25x slower                                                                                                  |
| logging_format             | 10.4 us                                                                                                           | 13.0 us: 1.25x slower                                                                                                   |
| crypto_pyaes               | 96.8 ms                                                                                                           | 121 ms: 1.25x slower                                                                                                    |
| deepcopy                   | 353 us                                                                                                            | 443 us: 1.25x slower                                                                                                    |
| 2to3                       | 479 ms                                                                                                            | 603 ms: 1.26x slower                                                                                                    |
| bpe_tokeniser              | 6.26 sec                                                                                                          | 7.91 sec: 1.26x slower                                                                                                  |
| sqlglot_normalize          | 139 ms                                                                                                            | 175 ms: 1.26x slower                                                                                                    |
| thrift                     | 1.06 ms                                                                                                           | 1.34 ms: 1.26x slower                                                                                                   |
| richards_super             | 75.6 ms                                                                                                           | 95.5 ms: 1.26x slower                                                                                                   |
| scimark_fft                | 434 ms                                                                                                            | 556 ms: 1.28x slower                                                                                                    |
| richards                   | 61.4 ms                                                                                                           | 78.9 ms: 1.29x slower                                                                                                   |
| sqlglot_parse              | 1.71 ms                                                                                                           | 2.21 ms: 1.29x slower                                                                                                   |
| deepcopy_reduce            | 3.39 us                                                                                                           | 4.37 us: 1.29x slower                                                                                                   |
| python_startup             | 28.2 ms                                                                                                           | 37.0 ms: 1.31x slower                                                                                                   |
| sqlalchemy_declarative     | 175 ms                                                                                                            | 233 ms: 1.33x slower                                                                                                    |
| scimark_sparse_mat_mult    | 6.28 ms                                                                                                           | 8.38 ms: 1.33x slower                                                                                                   |
| subparsers                 | 31.6 ms                                                                                                           | 42.2 ms: 1.34x slower                                                                                                   |
| nbody                      | 129 ms                                                                                                            | 176 ms: 1.37x slower                                                                                                    |
| hexiom                     | 7.73 ms                                                                                                           | 10.7 ms: 1.39x slower                                                                                                   |
| typing_runtime_protocols   | 215 us                                                                                                            | 298 us: 1.39x slower                                                                                                    |
| bench_thread_pool          | 3.92 ms                                                                                                           | 5.49 ms: 1.40x slower                                                                                                   |
| mako                       | 17.7 ms                                                                                                           | 24.8 ms: 1.40x slower                                                                                                   |
| deepcopy_memo              | 41.9 us                                                                                                           | 59.2 us: 1.41x slower                                                                                                   |
| genshi_xml                 | 67.8 ms                                                                                                           | 96.8 ms: 1.43x slower                                                                                                   |
| python_startup_no_site     | 16.7 ms                                                                                                           | 24.2 ms: 1.45x slower                                                                                                   |
| scimark_monte_carlo        | 85.6 ms                                                                                                           | 125 ms: 1.46x slower                                                                                                    |
| sqlalchemy_imperative      | 22.1 ms                                                                                                           | 33.1 ms: 1.50x slower                                                                                                   |
| deltablue                  | 4.28 ms                                                                                                           | 6.72 ms: 1.57x slower                                                                                                   |
| many_optionals             | 1.00 ms                                                                                                           | 1.64 ms: 1.63x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (7): bench_mp_pool, async_tree_memoization_tg, asyncio_websockets, pidigits, pycparser, sympy_str, float

- Geometric mean (including insignificant results): 1.132x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.19x