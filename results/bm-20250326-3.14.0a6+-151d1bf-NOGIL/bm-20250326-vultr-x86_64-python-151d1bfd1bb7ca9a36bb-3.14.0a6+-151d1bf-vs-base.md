# Results vs. base

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: linux-x86_64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.181x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                            | 314 ms: 1.25x slower                                                                                                    |
| docutils       | 2.54 sec                                                                                                          | 2.87 sec: 1.13x slower                                                                                                  |
| sphinx         | 976 ms                                                                                                            | 1.14 sec: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 621 ms                                                                                                            | 576 ms: 1.08x faster                                                                                                    |
| async_tree_io              | 610 ms                                                                                                            | 604 ms: 1.01x faster                                                                                                    |
| async_tree_none            | 269 ms                                                                                                            | 284 ms: 1.05x slower                                                                                                    |
| async_tree_memoization_tg  | 297 ms                                                                                                            | 314 ms: 1.06x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 476 ms                                                                                                            | 517 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 501 ms                                                                                                            | 547 ms: 1.09x slower                                                                                                    |
| async_tree_memoization     | 311 ms                                                                                                            | 343 ms: 1.10x slower                                                                                                    |
| coroutines                 | 21.8 ms                                                                                                           | 25.7 ms: 1.18x slower                                                                                                   |
| async_generators           | 325 ms                                                                                                            | 399 ms: 1.23x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                                                                            | 208 ms: 1.05x slower                                                                                                    |
| float          | 70.6 ms                                                                                                           | 81.2 ms: 1.15x slower                                                                                                   |
| nbody          | 94.5 ms                                                                                                           | 153 ms: 1.62x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.25x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.1 ms                                                                                                           | 21.0 ms: 1.05x faster                                                                                                   |
| regex_dna      | 174 ms                                                                                                            | 171 ms: 1.02x faster                                                                                                    |
| regex_effbot   | 2.74 ms                                                                                                           | 2.76 ms: 1.01x slower                                                                                                   |
| regex_compile  | 124 ms                                                                                                            | 170 ms: 1.36x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                                                            | 130 ms: 1.01x slower                                                                                                    |
| json_loads           | 27.3 us                                                                                                           | 29.5 us: 1.08x slower                                                                                                   |
| json_dumps           | 11.2 ms                                                                                                           | 13.3 ms: 1.18x slower                                                                                                   |
| xml_etree_generate   | 82.6 ms                                                                                                           | 101 ms: 1.22x slower                                                                                                    |
| xml_etree_process    | 57.7 ms                                                                                                           | 73.6 ms: 1.28x slower                                                                                                   |
| pickle_pure_python   | 303 us                                                                                                            | 388 us: 1.28x slower                                                                                                    |
| unpickle_pure_python | 208 us                                                                                                            | 277 us: 1.33x slower                                                                                                    |
| tomli_loads          | 1.91 sec                                                                                                          | 2.54 sec: 1.33x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 15.0 ms                                                                                                           | 15.8 ms: 1.06x slower                                                                                                   |
| python_startup_no_site | 8.63 ms                                                                                                           | 11.2 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.3 ms                                                                                                           | 44.7 ms: 1.30x slower                                                                                                   |
| genshi_xml      | 47.7 ms                                                                                                           | 66.2 ms: 1.39x slower                                                                                                   |
| mako            | 11.8 ms                                                                                                           | 16.5 ms: 1.40x slower                                                                                                   |
| genshi_text     | 20.4 ms                                                                                                           | 30.7 ms: 1.50x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.40x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json | results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.27 ms                                                                                                           | 1.80 ms: 2.37x faster                                                                                                   |
| create_gc_cycles           | 1.88 ms                                                                                                           | 1.35 ms: 1.39x faster                                                                                                   |
| async_tree_io_tg           | 621 ms                                                                                                            | 576 ms: 1.08x faster                                                                                                    |
| sqlite_synth               | 2.23 us                                                                                                           | 2.08 us: 1.07x faster                                                                                                   |
| regex_v8                   | 22.1 ms                                                                                                           | 21.0 ms: 1.05x faster                                                                                                   |
| regex_dna                  | 174 ms                                                                                                            | 171 ms: 1.02x faster                                                                                                    |
| async_tree_io              | 610 ms                                                                                                            | 604 ms: 1.01x faster                                                                                                    |
| xml_etree_parse            | 130 ms                                                                                                            | 130 ms: 1.01x slower                                                                                                    |
| regex_effbot               | 2.74 ms                                                                                                           | 2.76 ms: 1.01x slower                                                                                                   |
| pathlib                    | 19.1 ms                                                                                                           | 19.9 ms: 1.04x slower                                                                                                   |
| pidigits                   | 199 ms                                                                                                            | 208 ms: 1.05x slower                                                                                                    |
| async_tree_none            | 269 ms                                                                                                            | 284 ms: 1.05x slower                                                                                                    |
| async_tree_memoization_tg  | 297 ms                                                                                                            | 314 ms: 1.06x slower                                                                                                    |
| python_startup             | 15.0 ms                                                                                                           | 15.8 ms: 1.06x slower                                                                                                   |
| json                       | 4.80 ms                                                                                                           | 5.16 ms: 1.07x slower                                                                                                   |
| json_loads                 | 27.3 us                                                                                                           | 29.5 us: 1.08x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 476 ms                                                                                                            | 517 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 501 ms                                                                                                            | 547 ms: 1.09x slower                                                                                                    |
| bench_mp_pool              | 89.4 ms                                                                                                           | 98.1 ms: 1.10x slower                                                                                                   |
| async_tree_memoization     | 311 ms                                                                                                            | 343 ms: 1.10x slower                                                                                                    |
| pycparser                  | 1.11 sec                                                                                                          | 1.24 sec: 1.12x slower                                                                                                  |
| docutils                   | 2.54 sec                                                                                                          | 2.87 sec: 1.13x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                          | 2.32 sec: 1.14x slower                                                                                                  |
| float                      | 70.6 ms                                                                                                           | 81.2 ms: 1.15x slower                                                                                                   |
| sphinx                     | 976 ms                                                                                                            | 1.14 sec: 1.17x slower                                                                                                  |
| coroutines                 | 21.8 ms                                                                                                           | 25.7 ms: 1.18x slower                                                                                                   |
| pylint                     | 277 ms                                                                                                            | 327 ms: 1.18x slower                                                                                                    |
| json_dumps                 | 11.2 ms                                                                                                           | 13.3 ms: 1.18x slower                                                                                                   |
| mdp                        | 2.28 sec                                                                                                          | 2.70 sec: 1.19x slower                                                                                                  |
| dulwich_log                | 65.2 ms                                                                                                           | 77.4 ms: 1.19x slower                                                                                                   |
| bpe_tokeniser              | 4.23 sec                                                                                                          | 5.05 sec: 1.20x slower                                                                                                  |
| many_optionals             | 1.02 ms                                                                                                           | 1.22 ms: 1.20x slower                                                                                                   |
| thrift                     | 744 us                                                                                                            | 908 us: 1.22x slower                                                                                                    |
| xml_etree_generate         | 82.6 ms                                                                                                           | 101 ms: 1.22x slower                                                                                                    |
| async_generators           | 325 ms                                                                                                            | 399 ms: 1.23x slower                                                                                                    |
| subparsers                 | 21.7 ms                                                                                                           | 27.0 ms: 1.24x slower                                                                                                   |
| pprint_safe_repr           | 709 ms                                                                                                            | 887 ms: 1.25x slower                                                                                                    |
| sqlglot_v2_optimize        | 51.0 ms                                                                                                           | 63.9 ms: 1.25x slower                                                                                                   |
| 2to3                       | 250 ms                                                                                                            | 314 ms: 1.25x slower                                                                                                    |
| sqlglot_v2_normalize       | 99.5 ms                                                                                                           | 125 ms: 1.26x slower                                                                                                    |
| telco                      | 7.26 ms                                                                                                           | 9.19 ms: 1.27x slower                                                                                                   |
| pprint_pformat             | 1.45 sec                                                                                                          | 1.83 sec: 1.27x slower                                                                                                  |
| sympy_sum                  | 152 ms                                                                                                            | 194 ms: 1.27x slower                                                                                                    |
| scimark_fft                | 326 ms                                                                                                            | 415 ms: 1.28x slower                                                                                                    |
| shortest_path              | 437 ms                                                                                                            | 557 ms: 1.28x slower                                                                                                    |
| xml_etree_process          | 57.7 ms                                                                                                           | 73.6 ms: 1.28x slower                                                                                                   |
| deepcopy_reduce            | 2.64 us                                                                                                           | 3.37 us: 1.28x slower                                                                                                   |
| pickle_pure_python         | 303 us                                                                                                            | 388 us: 1.28x slower                                                                                                    |
| sympy_integrate            | 19.2 ms                                                                                                           | 24.6 ms: 1.28x slower                                                                                                   |
| sympy_expand               | 454 ms                                                                                                            | 582 ms: 1.28x slower                                                                                                    |
| sqlalchemy_declarative     | 127 ms                                                                                                            | 164 ms: 1.29x slower                                                                                                    |
| python_startup_no_site     | 8.63 ms                                                                                                           | 11.2 ms: 1.29x slower                                                                                                   |
| nqueens                    | 78.2 ms                                                                                                           | 101 ms: 1.29x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.58 ms                                                                                                           | 5.94 ms: 1.30x slower                                                                                                   |
| sqlalchemy_imperative      | 19.2 ms                                                                                                           | 25.0 ms: 1.30x slower                                                                                                   |
| connected_components       | 395 ms                                                                                                            | 514 ms: 1.30x slower                                                                                                    |
| django_template            | 34.3 ms                                                                                                           | 44.7 ms: 1.30x slower                                                                                                   |
| sympy_str                  | 270 ms                                                                                                            | 352 ms: 1.31x slower                                                                                                    |
| scimark_lu                 | 112 ms                                                                                                            | 147 ms: 1.31x slower                                                                                                    |
| logging_silent             | 95.5 ns                                                                                                           | 126 ns: 1.32x slower                                                                                                    |
| deepcopy                   | 252 us                                                                                                            | 334 us: 1.32x slower                                                                                                    |
| unpickle_pure_python       | 208 us                                                                                                            | 277 us: 1.33x slower                                                                                                    |
| tomli_loads                | 1.91 sec                                                                                                          | 2.54 sec: 1.33x slower                                                                                                  |
| typing_runtime_protocols   | 154 us                                                                                                            | 206 us: 1.34x slower                                                                                                    |
| pyflate                    | 404 ms                                                                                                            | 543 ms: 1.35x slower                                                                                                    |
| sqlglot_v2_transpile       | 1.52 ms                                                                                                           | 2.07 ms: 1.36x slower                                                                                                   |
| regex_compile              | 124 ms                                                                                                            | 170 ms: 1.36x slower                                                                                                    |
| spectral_norm              | 90.2 ms                                                                                                           | 123 ms: 1.37x slower                                                                                                    |
| fannkuch                   | 389 ms                                                                                                            | 533 ms: 1.37x slower                                                                                                    |
| raytrace                   | 255 ms                                                                                                            | 352 ms: 1.38x slower                                                                                                    |
| meteor_contest             | 100 ms                                                                                                            | 139 ms: 1.38x slower                                                                                                    |
| chaos                      | 54.7 ms                                                                                                           | 75.9 ms: 1.39x slower                                                                                                   |
| genshi_xml                 | 47.7 ms                                                                                                           | 66.2 ms: 1.39x slower                                                                                                   |
| comprehensions             | 16.3 us                                                                                                           | 22.7 us: 1.39x slower                                                                                                   |
| sqlglot_v2_parse           | 1.23 ms                                                                                                           | 1.72 ms: 1.40x slower                                                                                                   |
| coverage                   | 77.9 ms                                                                                                           | 109 ms: 1.40x slower                                                                                                    |
| mako                       | 11.8 ms                                                                                                           | 16.5 ms: 1.40x slower                                                                                                   |
| crypto_pyaes               | 66.6 ms                                                                                                           | 94.0 ms: 1.41x slower                                                                                                   |
| logging_simple             | 5.82 us                                                                                                           | 8.28 us: 1.42x slower                                                                                                   |
| hexiom                     | 5.72 ms                                                                                                           | 8.21 ms: 1.44x slower                                                                                                   |
| generators                 | 26.9 ms                                                                                                           | 38.7 ms: 1.44x slower                                                                                                   |
| deepcopy_memo              | 29.2 us                                                                                                           | 42.3 us: 1.45x slower                                                                                                   |
| logging_format             | 6.48 us                                                                                                           | 9.38 us: 1.45x slower                                                                                                   |
| scimark_monte_carlo        | 62.9 ms                                                                                                           | 91.4 ms: 1.45x slower                                                                                                   |
| richards_super             | 46.8 ms                                                                                                           | 69.2 ms: 1.48x slower                                                                                                   |
| go                         | 108 ms                                                                                                            | 160 ms: 1.48x slower                                                                                                    |
| richards                   | 40.8 ms                                                                                                           | 61.0 ms: 1.49x slower                                                                                                   |
| genshi_text                | 20.4 ms                                                                                                           | 30.7 ms: 1.50x slower                                                                                                   |
| scimark_sor                | 109 ms                                                                                                            | 164 ms: 1.51x slower                                                                                                    |
| deltablue                  | 2.98 ms                                                                                                           | 4.58 ms: 1.54x slower                                                                                                   |
| nbody                      | 94.5 ms                                                                                                           | 153 ms: 1.62x slower                                                                                                    |
| bench_thread_pool          | 1.04 ms                                                                                                           | 3.19 ms: 3.08x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.23x slower                                                                                                            |

Benchmark hidden because not significant (3): asyncio_websockets, xml_etree_iterparse, async_tree_none_tg
Ignored benchmarks (1) of results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: html5lib

- Geometric mean (including insignificant results): 1.181x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.20x