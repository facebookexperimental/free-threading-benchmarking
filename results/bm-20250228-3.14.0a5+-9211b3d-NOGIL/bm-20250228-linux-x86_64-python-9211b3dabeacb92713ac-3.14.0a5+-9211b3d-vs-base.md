# Results vs. base

- fork: python
- ref: 9211b3dabeacb92713ac
- machine: linux-x86_64
- commit hash: 9211b3d
- commit date: 2025-02-28
- overall geometric mean: 1.117x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 439 ms                                                                                                            | 504 ms: 1.15x slower                                                                                                    |
| docutils       | 3.61 sec                                                                                                          | 4.01 sec: 1.11x slower                                                                                                  |
| html5lib       | 84.6 ms                                                                                                           | 97.3 ms: 1.15x slower                                                                                                   |
| sphinx         | 1.42 sec                                                                                                          | 1.60 sec: 1.13x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 882 ms                                                                                                            | 738 ms: 1.19x faster                                                                                                    |
| async_tree_memoization_tg  | 469 ms                                                                                                            | 427 ms: 1.10x faster                                                                                                    |
| async_tree_none_tg         | 361 ms                                                                                                            | 330 ms: 1.09x faster                                                                                                    |
| async_tree_io              | 869 ms                                                                                                            | 797 ms: 1.09x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 686 ms                                                                                                            | 654 ms: 1.05x faster                                                                                                    |
| async_tree_cpu_io_mixed    | 660 ms                                                                                                            | 704 ms: 1.07x slower                                                                                                    |
| async_tree_memoization     | 475 ms                                                                                                            | 513 ms: 1.08x slower                                                                                                    |
| async_generators           | 495 ms                                                                                                            | 560 ms: 1.13x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.02x faster                                                                                                            |

Benchmark hidden because not significant (3): coroutines, asyncio_websockets, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 106 ms                                                                                                            | 99.4 ms: 1.07x faster                                                                                                   |
| nbody          | 122 ms                                                                                                            | 182 ms: 1.50x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 33.8 ms                                                                                                           | 32.4 ms: 1.04x faster                                                                                                   |
| regex_dna      | 287 ms                                                                                                            | 303 ms: 1.06x slower                                                                                                    |
| regex_compile  | 174 ms                                                                                                            | 186 ms: 1.07x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 144 ms                                                                                                            | 133 ms: 1.09x faster                                                                                                    |
| xml_etree_process    | 83.1 ms                                                                                                           | 88.5 ms: 1.07x slower                                                                                                   |
| json_loads           | 38.0 us                                                                                                           | 40.8 us: 1.07x slower                                                                                                   |
| json_dumps           | 14.6 ms                                                                                                           | 17.0 ms: 1.17x slower                                                                                                   |
| xml_etree_generate   | 115 ms                                                                                                            | 135 ms: 1.17x slower                                                                                                    |
| unpickle_pure_python | 281 us                                                                                                            | 333 us: 1.19x slower                                                                                                    |
| pickle_pure_python   | 409 us                                                                                                            | 492 us: 1.20x slower                                                                                                    |
| tomli_loads          | 2.53 sec                                                                                                          | 3.05 sec: 1.21x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 26.0 ms                                                                                                           | 30.2 ms: 1.16x slower                                                                                                   |
| python_startup_no_site | 15.2 ms                                                                                                           | 20.3 ms: 1.34x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.25x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 43.4 ms                                                                                                           | 52.4 ms: 1.21x slower                                                                                                   |
| genshi_xml      | 68.2 ms                                                                                                           | 84.8 ms: 1.24x slower                                                                                                   |
| genshi_text     | 29.2 ms                                                                                                           | 37.0 ms: 1.27x slower                                                                                                   |
| mako            | 15.9 ms                                                                                                           | 22.7 ms: 1.43x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.28x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json | results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 7.85 ms                                                                                                           | 3.86 ms: 2.04x faster                                                                                                   |
| create_gc_cycles           | 3.69 ms                                                                                                           | 2.54 ms: 1.45x faster                                                                                                   |
| async_tree_io_tg           | 882 ms                                                                                                            | 738 ms: 1.19x faster                                                                                                    |
| async_tree_memoization_tg  | 469 ms                                                                                                            | 427 ms: 1.10x faster                                                                                                    |
| async_tree_none_tg         | 361 ms                                                                                                            | 330 ms: 1.09x faster                                                                                                    |
| async_tree_io              | 869 ms                                                                                                            | 797 ms: 1.09x faster                                                                                                    |
| xml_etree_iterparse        | 144 ms                                                                                                            | 133 ms: 1.09x faster                                                                                                    |
| bench_mp_pool              | 94.8 ms                                                                                                           | 88.2 ms: 1.07x faster                                                                                                   |
| float                      | 106 ms                                                                                                            | 99.4 ms: 1.07x faster                                                                                                   |
| sqlite_synth               | 3.65 us                                                                                                           | 3.44 us: 1.06x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 686 ms                                                                                                            | 654 ms: 1.05x faster                                                                                                    |
| regex_v8                   | 33.8 ms                                                                                                           | 32.4 ms: 1.04x faster                                                                                                   |
| generators                 | 42.1 ms                                                                                                           | 43.9 ms: 1.04x slower                                                                                                   |
| regex_dna                  | 287 ms                                                                                                            | 303 ms: 1.06x slower                                                                                                    |
| sqlglot_normalize          | 142 ms                                                                                                            | 150 ms: 1.06x slower                                                                                                    |
| xml_etree_process          | 83.1 ms                                                                                                           | 88.5 ms: 1.07x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 660 ms                                                                                                            | 704 ms: 1.07x slower                                                                                                    |
| regex_compile              | 174 ms                                                                                                            | 186 ms: 1.07x slower                                                                                                    |
| json_loads                 | 38.0 us                                                                                                           | 40.8 us: 1.07x slower                                                                                                   |
| logging_silent             | 135 ns                                                                                                            | 145 ns: 1.07x slower                                                                                                    |
| async_tree_memoization     | 475 ms                                                                                                            | 513 ms: 1.08x slower                                                                                                    |
| k_core                     | 4.05 sec                                                                                                          | 4.39 sec: 1.08x slower                                                                                                  |
| spectral_norm              | 129 ms                                                                                                            | 142 ms: 1.10x slower                                                                                                    |
| pathlib                    | 29.0 ms                                                                                                           | 31.9 ms: 1.10x slower                                                                                                   |
| docutils                   | 3.61 sec                                                                                                          | 4.01 sec: 1.11x slower                                                                                                  |
| richards_super             | 71.5 ms                                                                                                           | 79.6 ms: 1.11x slower                                                                                                   |
| comprehensions             | 21.5 us                                                                                                           | 24.3 us: 1.13x slower                                                                                                   |
| dulwich_log                | 92.1 ms                                                                                                           | 104 ms: 1.13x slower                                                                                                    |
| async_generators           | 495 ms                                                                                                            | 560 ms: 1.13x slower                                                                                                    |
| sphinx                     | 1.42 sec                                                                                                          | 1.60 sec: 1.13x slower                                                                                                  |
| sqlglot_optimize           | 74.0 ms                                                                                                           | 84.0 ms: 1.13x slower                                                                                                   |
| deepcopy                   | 361 us                                                                                                            | 411 us: 1.14x slower                                                                                                    |
| 2to3                       | 439 ms                                                                                                            | 504 ms: 1.15x slower                                                                                                    |
| html5lib                   | 84.6 ms                                                                                                           | 97.3 ms: 1.15x slower                                                                                                   |
| nqueens                    | 109 ms                                                                                                            | 126 ms: 1.15x slower                                                                                                    |
| sympy_integrate            | 28.9 ms                                                                                                           | 33.4 ms: 1.15x slower                                                                                                   |
| sympy_expand               | 589 ms                                                                                                            | 681 ms: 1.16x slower                                                                                                    |
| raytrace                   | 369 ms                                                                                                            | 428 ms: 1.16x slower                                                                                                    |
| python_startup             | 26.0 ms                                                                                                           | 30.2 ms: 1.16x slower                                                                                                   |
| pprint_safe_repr           | 916 ms                                                                                                            | 1.07 sec: 1.17x slower                                                                                                  |
| json_dumps                 | 14.6 ms                                                                                                           | 17.0 ms: 1.17x slower                                                                                                   |
| chaos                      | 76.8 ms                                                                                                           | 89.8 ms: 1.17x slower                                                                                                   |
| xml_etree_generate         | 115 ms                                                                                                            | 135 ms: 1.17x slower                                                                                                    |
| pylint                     | 384 ms                                                                                                            | 452 ms: 1.18x slower                                                                                                    |
| sqlglot_transpile          | 2.21 ms                                                                                                           | 2.61 ms: 1.18x slower                                                                                                   |
| mdp                        | 3.61 sec                                                                                                          | 4.28 sec: 1.18x slower                                                                                                  |
| unpickle_pure_python       | 281 us                                                                                                            | 333 us: 1.19x slower                                                                                                    |
| go                         | 147 ms                                                                                                            | 175 ms: 1.19x slower                                                                                                    |
| sympy_str                  | 357 ms                                                                                                            | 427 ms: 1.20x slower                                                                                                    |
| pprint_pformat             | 1.84 sec                                                                                                          | 2.20 sec: 1.20x slower                                                                                                  |
| pickle_pure_python         | 409 us                                                                                                            | 492 us: 1.20x slower                                                                                                    |
| tomli_loads                | 2.53 sec                                                                                                          | 3.05 sec: 1.21x slower                                                                                                  |
| sqlalchemy_imperative      | 22.6 ms                                                                                                           | 27.3 ms: 1.21x slower                                                                                                   |
| crypto_pyaes               | 98.7 ms                                                                                                           | 119 ms: 1.21x slower                                                                                                    |
| django_template            | 43.4 ms                                                                                                           | 52.4 ms: 1.21x slower                                                                                                   |
| scimark_sor                | 156 ms                                                                                                            | 190 ms: 1.21x slower                                                                                                    |
| meteor_contest             | 144 ms                                                                                                            | 174 ms: 1.22x slower                                                                                                    |
| telco                      | 9.58 ms                                                                                                           | 11.7 ms: 1.22x slower                                                                                                   |
| connected_components       | 794 ms                                                                                                            | 968 ms: 1.22x slower                                                                                                    |
| logging_format             | 9.08 us                                                                                                           | 11.3 us: 1.24x slower                                                                                                   |
| genshi_xml                 | 68.2 ms                                                                                                           | 84.8 ms: 1.24x slower                                                                                                   |
| pyflate                    | 606 ms                                                                                                            | 756 ms: 1.25x slower                                                                                                    |
| sqlalchemy_declarative     | 169 ms                                                                                                            | 212 ms: 1.25x slower                                                                                                    |
| sqlglot_parse              | 1.76 ms                                                                                                           | 2.20 ms: 1.25x slower                                                                                                   |
| coverage                   | 111 ms                                                                                                            | 139 ms: 1.26x slower                                                                                                    |
| typing_runtime_protocols   | 212 us                                                                                                            | 266 us: 1.26x slower                                                                                                    |
| deepcopy_memo              | 39.1 us                                                                                                           | 49.3 us: 1.26x slower                                                                                                   |
| genshi_text                | 29.2 ms                                                                                                           | 37.0 ms: 1.27x slower                                                                                                   |
| fannkuch                   | 510 ms                                                                                                            | 648 ms: 1.27x slower                                                                                                    |
| scimark_lu                 | 158 ms                                                                                                            | 201 ms: 1.27x slower                                                                                                    |
| deltablue                  | 4.06 ms                                                                                                           | 5.17 ms: 1.28x slower                                                                                                   |
| thrift                     | 927 us                                                                                                            | 1.19 ms: 1.28x slower                                                                                                   |
| shortest_path              | 852 ms                                                                                                            | 1.09 sec: 1.28x slower                                                                                                  |
| richards                   | 54.1 ms                                                                                                           | 69.5 ms: 1.28x slower                                                                                                   |
| logging_simple             | 7.64 us                                                                                                           | 9.83 us: 1.29x slower                                                                                                   |
| sympy_sum                  | 198 ms                                                                                                            | 254 ms: 1.29x slower                                                                                                    |
| bpe_tokeniser              | 5.74 sec                                                                                                          | 7.41 sec: 1.29x slower                                                                                                  |
| many_optionals             | 1.23 ms                                                                                                           | 1.59 ms: 1.29x slower                                                                                                   |
| hexiom                     | 7.65 ms                                                                                                           | 9.90 ms: 1.29x slower                                                                                                   |
| deepcopy_reduce            | 3.38 us                                                                                                           | 4.46 us: 1.32x slower                                                                                                   |
| subparsers                 | 30.5 ms                                                                                                           | 40.3 ms: 1.32x slower                                                                                                   |
| python_startup_no_site     | 15.2 ms                                                                                                           | 20.3 ms: 1.34x slower                                                                                                   |
| bench_thread_pool          | 3.07 ms                                                                                                           | 4.38 ms: 1.43x slower                                                                                                   |
| scimark_fft                | 457 ms                                                                                                            | 653 ms: 1.43x slower                                                                                                    |
| mako                       | 15.9 ms                                                                                                           | 22.7 ms: 1.43x slower                                                                                                   |
| scimark_monte_carlo        | 87.4 ms                                                                                                           | 130 ms: 1.49x slower                                                                                                    |
| nbody                      | 122 ms                                                                                                            | 182 ms: 1.50x slower                                                                                                    |
| scimark_sparse_mat_mult    | 6.39 ms                                                                                                           | 10.5 ms: 1.64x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (8): regex_effbot, xml_etree_parse, pidigits, coroutines, pycparser, json, asyncio_websockets, async_tree_none

- Geometric mean (including insignificant results): 1.117x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x