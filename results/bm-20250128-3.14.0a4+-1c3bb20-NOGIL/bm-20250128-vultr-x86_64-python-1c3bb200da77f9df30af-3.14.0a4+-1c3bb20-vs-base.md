# Results vs. base

- fork: python
- ref: 1c3bb200da77f9df30af
- machine: linux-x86_64
- commit hash: 1c3bb20
- commit date: 2025-01-28
- overall geometric mean: 1.153x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                                                            | 313 ms: 1.23x slower                                                                                                    |
| docutils       | 2.56 sec                                                                                                          | 2.88 sec: 1.13x slower                                                                                                  |
| sphinx         | 983 ms                                                                                                            | 1.14 sec: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 619 ms                                                                                                            | 587 ms: 1.05x faster                                                                                                    |
| async_tree_none_tg         | 264 ms                                                                                                            | 255 ms: 1.04x faster                                                                                                    |
| async_tree_io              | 626 ms                                                                                                            | 616 ms: 1.02x faster                                                                                                    |
| async_tree_memoization_tg  | 316 ms                                                                                                            | 325 ms: 1.03x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                                                            | 512 ms: 1.06x slower                                                                                                    |
| async_tree_none            | 272 ms                                                                                                            | 294 ms: 1.08x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 494 ms                                                                                                            | 543 ms: 1.10x slower                                                                                                    |
| async_tree_memoization     | 325 ms                                                                                                            | 359 ms: 1.10x slower                                                                                                    |
| coroutines                 | 21.8 ms                                                                                                           | 24.6 ms: 1.13x slower                                                                                                   |
| async_generators           | 320 ms                                                                                                            | 375 ms: 1.17x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                                                                            | 193 ms: 1.01x faster                                                                                                    |
| float          | 72.0 ms                                                                                                           | 77.9 ms: 1.08x slower                                                                                                   |
| nbody          | 89.3 ms                                                                                                           | 140 ms: 1.56x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 2.88 ms                                                                                                           | 2.88 ms: 1.00x faster                                                                                                   |
| regex_dna      | 172 ms                                                                                                            | 182 ms: 1.06x slower                                                                                                    |
| regex_compile  | 126 ms                                                                                                            | 157 ms: 1.25x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.5 ms                                                                                                           | 89.0 ms: 1.02x faster                                                                                                   |
| xml_etree_parse      | 127 ms                                                                                                            | 129 ms: 1.02x slower                                                                                                    |
| json_loads           | 28.4 us                                                                                                           | 31.0 us: 1.09x slower                                                                                                   |
| json_dumps           | 11.3 ms                                                                                                           | 13.1 ms: 1.16x slower                                                                                                   |
| xml_etree_generate   | 83.6 ms                                                                                                           | 98.7 ms: 1.18x slower                                                                                                   |
| xml_etree_process    | 59.2 ms                                                                                                           | 70.8 ms: 1.20x slower                                                                                                   |
| unpickle_pure_python | 212 us                                                                                                            | 259 us: 1.22x slower                                                                                                    |
| pickle_pure_python   | 312 us                                                                                                            | 382 us: 1.22x slower                                                                                                    |
| tomli_loads          | 1.94 sec                                                                                                          | 2.43 sec: 1.25x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                                                           | 15.3 ms: 1.05x slower                                                                                                   |
| python_startup_no_site | 7.42 ms                                                                                                           | 9.60 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.9 ms                                                                                                           | 44.1 ms: 1.26x slower                                                                                                   |
| genshi_xml      | 48.4 ms                                                                                                           | 61.9 ms: 1.28x slower                                                                                                   |
| genshi_text     | 21.3 ms                                                                                                           | 28.5 ms: 1.34x slower                                                                                                   |
| mako            | 11.7 ms                                                                                                           | 16.2 ms: 1.38x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.32x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json | results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles           | 1.86 ms                                                                                                           | 1.37 ms: 1.36x faster                                                                                                   |
| gc_traversal               | 4.21 ms                                                                                                           | 3.16 ms: 1.33x faster                                                                                                   |
| sqlite_synth               | 2.20 us                                                                                                           | 2.07 us: 1.06x faster                                                                                                   |
| async_tree_io_tg           | 619 ms                                                                                                            | 587 ms: 1.05x faster                                                                                                    |
| async_tree_none_tg         | 264 ms                                                                                                            | 255 ms: 1.04x faster                                                                                                    |
| xml_etree_iterparse        | 90.5 ms                                                                                                           | 89.0 ms: 1.02x faster                                                                                                   |
| async_tree_io              | 626 ms                                                                                                            | 616 ms: 1.02x faster                                                                                                    |
| pidigits                   | 194 ms                                                                                                            | 193 ms: 1.01x faster                                                                                                    |
| regex_effbot               | 2.88 ms                                                                                                           | 2.88 ms: 1.00x faster                                                                                                   |
| xml_etree_parse            | 127 ms                                                                                                            | 129 ms: 1.02x slower                                                                                                    |
| pathlib                    | 18.5 ms                                                                                                           | 18.8 ms: 1.02x slower                                                                                                   |
| async_tree_memoization_tg  | 316 ms                                                                                                            | 325 ms: 1.03x slower                                                                                                    |
| python_startup             | 14.6 ms                                                                                                           | 15.3 ms: 1.05x slower                                                                                                   |
| regex_dna                  | 172 ms                                                                                                            | 182 ms: 1.06x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                                                            | 512 ms: 1.06x slower                                                                                                    |
| json                       | 5.05 ms                                                                                                           | 5.36 ms: 1.06x slower                                                                                                   |
| float                      | 72.0 ms                                                                                                           | 77.9 ms: 1.08x slower                                                                                                   |
| async_tree_none            | 272 ms                                                                                                            | 294 ms: 1.08x slower                                                                                                    |
| bench_mp_pool              | 87.8 ms                                                                                                           | 95.2 ms: 1.08x slower                                                                                                   |
| json_loads                 | 28.4 us                                                                                                           | 31.0 us: 1.09x slower                                                                                                   |
| pycparser                  | 1.11 sec                                                                                                          | 1.22 sec: 1.10x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 494 ms                                                                                                            | 543 ms: 1.10x slower                                                                                                    |
| async_tree_memoization     | 325 ms                                                                                                            | 359 ms: 1.10x slower                                                                                                    |
| docutils                   | 2.56 sec                                                                                                          | 2.88 sec: 1.13x slower                                                                                                  |
| dulwich_log                | 74.5 ms                                                                                                           | 84.1 ms: 1.13x slower                                                                                                   |
| coroutines                 | 21.8 ms                                                                                                           | 24.6 ms: 1.13x slower                                                                                                   |
| logging_silent             | 106 ns                                                                                                            | 121 ns: 1.14x slower                                                                                                    |
| k_core                     | 2.04 sec                                                                                                          | 2.33 sec: 1.14x slower                                                                                                  |
| mdp                        | 2.44 sec                                                                                                          | 2.79 sec: 1.15x slower                                                                                                  |
| bpe_tokeniser              | 4.21 sec                                                                                                          | 4.83 sec: 1.15x slower                                                                                                  |
| json_dumps                 | 11.3 ms                                                                                                           | 13.1 ms: 1.16x slower                                                                                                   |
| pylint                     | 280 ms                                                                                                            | 325 ms: 1.16x slower                                                                                                    |
| sphinx                     | 983 ms                                                                                                            | 1.14 sec: 1.16x slower                                                                                                  |
| generators                 | 28.3 ms                                                                                                           | 33.2 ms: 1.17x slower                                                                                                   |
| async_generators           | 320 ms                                                                                                            | 375 ms: 1.17x slower                                                                                                    |
| xml_etree_generate         | 83.6 ms                                                                                                           | 98.7 ms: 1.18x slower                                                                                                   |
| many_optionals             | 1.01 ms                                                                                                           | 1.20 ms: 1.18x slower                                                                                                   |
| sqlglot_normalize          | 104 ms                                                                                                            | 124 ms: 1.19x slower                                                                                                    |
| xml_etree_process          | 59.2 ms                                                                                                           | 70.8 ms: 1.20x slower                                                                                                   |
| subparsers                 | 21.7 ms                                                                                                           | 26.0 ms: 1.20x slower                                                                                                   |
| scimark_sor                | 116 ms                                                                                                            | 139 ms: 1.20x slower                                                                                                    |
| pprint_safe_repr           | 703 ms                                                                                                            | 854 ms: 1.21x slower                                                                                                    |
| sqlglot_optimize           | 51.8 ms                                                                                                           | 63.1 ms: 1.22x slower                                                                                                   |
| unpickle_pure_python       | 212 us                                                                                                            | 259 us: 1.22x slower                                                                                                    |
| spectral_norm              | 90.5 ms                                                                                                           | 111 ms: 1.22x slower                                                                                                    |
| telco                      | 7.21 ms                                                                                                           | 8.82 ms: 1.22x slower                                                                                                   |
| pickle_pure_python         | 312 us                                                                                                            | 382 us: 1.22x slower                                                                                                    |
| logging_simple             | 6.04 us                                                                                                           | 7.40 us: 1.22x slower                                                                                                   |
| pprint_pformat             | 1.44 sec                                                                                                          | 1.76 sec: 1.23x slower                                                                                                  |
| coverage                   | 79.5 ms                                                                                                           | 97.6 ms: 1.23x slower                                                                                                   |
| 2to3                       | 254 ms                                                                                                            | 313 ms: 1.23x slower                                                                                                    |
| regex_compile              | 126 ms                                                                                                            | 157 ms: 1.25x slower                                                                                                    |
| scimark_fft                | 317 ms                                                                                                            | 396 ms: 1.25x slower                                                                                                    |
| pyflate                    | 415 ms                                                                                                            | 519 ms: 1.25x slower                                                                                                    |
| sympy_expand               | 456 ms                                                                                                            | 570 ms: 1.25x slower                                                                                                    |
| go                         | 115 ms                                                                                                            | 145 ms: 1.25x slower                                                                                                    |
| tomli_loads                | 1.94 sec                                                                                                          | 2.43 sec: 1.25x slower                                                                                                  |
| sympy_sum                  | 152 ms                                                                                                            | 190 ms: 1.25x slower                                                                                                    |
| sympy_integrate            | 19.7 ms                                                                                                           | 24.7 ms: 1.26x slower                                                                                                   |
| deepcopy                   | 256 us                                                                                                            | 322 us: 1.26x slower                                                                                                    |
| django_template            | 34.9 ms                                                                                                           | 44.1 ms: 1.26x slower                                                                                                   |
| logging_format             | 6.73 us                                                                                                           | 8.50 us: 1.26x slower                                                                                                   |
| comprehensions             | 16.8 us                                                                                                           | 21.3 us: 1.27x slower                                                                                                   |
| thrift                     | 732 us                                                                                                            | 927 us: 1.27x slower                                                                                                    |
| connected_components       | 391 ms                                                                                                            | 495 ms: 1.27x slower                                                                                                    |
| deepcopy_reduce            | 2.60 us                                                                                                           | 3.30 us: 1.27x slower                                                                                                   |
| sqlalchemy_declarative     | 128 ms                                                                                                            | 162 ms: 1.27x slower                                                                                                    |
| sympy_str                  | 271 ms                                                                                                            | 345 ms: 1.27x slower                                                                                                    |
| nqueens                    | 77.2 ms                                                                                                           | 98.1 ms: 1.27x slower                                                                                                   |
| raytrace                   | 268 ms                                                                                                            | 341 ms: 1.27x slower                                                                                                    |
| scimark_lu                 | 111 ms                                                                                                            | 142 ms: 1.27x slower                                                                                                    |
| shortest_path              | 430 ms                                                                                                            | 549 ms: 1.28x slower                                                                                                    |
| genshi_xml                 | 48.4 ms                                                                                                           | 61.9 ms: 1.28x slower                                                                                                   |
| sqlglot_transpile          | 1.54 ms                                                                                                           | 1.97 ms: 1.28x slower                                                                                                   |
| sqlalchemy_imperative      | 19.2 ms                                                                                                           | 24.6 ms: 1.29x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.44 ms                                                                                                           | 5.72 ms: 1.29x slower                                                                                                   |
| python_startup_no_site     | 7.42 ms                                                                                                           | 9.60 ms: 1.29x slower                                                                                                   |
| fannkuch                   | 377 ms                                                                                                            | 490 ms: 1.30x slower                                                                                                    |
| chaos                      | 55.5 ms                                                                                                           | 72.4 ms: 1.30x slower                                                                                                   |
| deepcopy_memo              | 30.1 us                                                                                                           | 39.3 us: 1.31x slower                                                                                                   |
| hexiom                     | 5.80 ms                                                                                                           | 7.59 ms: 1.31x slower                                                                                                   |
| scimark_monte_carlo        | 64.3 ms                                                                                                           | 84.5 ms: 1.31x slower                                                                                                   |
| crypto_pyaes               | 67.9 ms                                                                                                           | 89.3 ms: 1.32x slower                                                                                                   |
| sqlglot_parse              | 1.24 ms                                                                                                           | 1.63 ms: 1.32x slower                                                                                                   |
| typing_runtime_protocols   | 155 us                                                                                                            | 205 us: 1.33x slower                                                                                                    |
| meteor_contest             | 99.4 ms                                                                                                           | 132 ms: 1.33x slower                                                                                                    |
| genshi_text                | 21.3 ms                                                                                                           | 28.5 ms: 1.34x slower                                                                                                   |
| mako                       | 11.7 ms                                                                                                           | 16.2 ms: 1.38x slower                                                                                                   |
| richards                   | 42.5 ms                                                                                                           | 59.3 ms: 1.40x slower                                                                                                   |
| richards_super             | 48.6 ms                                                                                                           | 68.1 ms: 1.40x slower                                                                                                   |
| deltablue                  | 3.18 ms                                                                                                           | 4.83 ms: 1.52x slower                                                                                                   |
| nbody                      | 89.3 ms                                                                                                           | 140 ms: 1.56x slower                                                                                                    |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.33 ms: 3.23x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, regex_v8
Ignored benchmarks (1) of results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json: html5lib

- Geometric mean (including insignificant results): 1.153x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.20x