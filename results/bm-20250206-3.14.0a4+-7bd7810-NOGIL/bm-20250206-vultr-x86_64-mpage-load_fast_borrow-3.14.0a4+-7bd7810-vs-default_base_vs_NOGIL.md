# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow
- machine: linux-x86_64
- commit hash: 7bd7810
- commit date: 2025-02-06
- overall geometric mean: 1.125x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 305 ms: 1.20x slower                                              |
| docutils       | 2.55 sec                                                               | 2.81 sec: 1.10x slower                                            |
| sphinx         | 979 ms                                                                 | 1.11 sec: 1.14x slower                                            |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 632 ms                                                                 | 563 ms: 1.12x faster                                              |
| async_tree_none_tg         | 265 ms                                                                 | 242 ms: 1.09x faster                                              |
| async_tree_io              | 624 ms                                                                 | 602 ms: 1.04x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                              |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 495 ms: 1.01x slower                                              |
| async_tree_none            | 271 ms                                                                 | 284 ms: 1.05x slower                                              |
| coroutines                 | 22.1 ms                                                                | 23.3 ms: 1.05x slower                                             |
| async_tree_memoization     | 327 ms                                                                 | 345 ms: 1.06x slower                                              |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 532 ms: 1.06x slower                                              |
| async_generators           | 323 ms                                                                 | 375 ms: 1.16x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 196 ms                                                                 | 191 ms: 1.02x faster                                              |
| nbody          | 91.6 ms                                                                | 132 ms: 1.44x slower                                              |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                      |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 23.6 ms                                                                | 24.6 ms: 1.04x slower                                             |
| regex_effbot   | 2.80 ms                                                                | 2.94 ms: 1.05x slower                                             |
| regex_dna      | 165 ms                                                                 | 185 ms: 1.12x slower                                              |
| regex_compile  | 126 ms                                                                 | 151 ms: 1.20x slower                                              |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 91.6 ms                                                                | 87.9 ms: 1.04x faster                                             |
| json_loads           | 28.8 us                                                                | 31.6 us: 1.10x slower                                             |
| json_dumps           | 11.6 ms                                                                | 12.8 ms: 1.10x slower                                             |
| unpickle_pure_python | 212 us                                                                 | 243 us: 1.14x slower                                              |
| pickle_pure_python   | 311 us                                                                 | 355 us: 1.14x slower                                              |
| xml_etree_generate   | 83.4 ms                                                                | 95.8 ms: 1.15x slower                                             |
| xml_etree_process    | 58.0 ms                                                                | 68.1 ms: 1.17x slower                                             |
| tomli_loads          | 1.90 sec                                                               | 2.34 sec: 1.23x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                      |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                | 15.6 ms: 1.06x slower                                             |
| python_startup_no_site | 7.52 ms                                                                | 9.78 ms: 1.30x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 48.2 ms                                                                | 58.5 ms: 1.21x slower                                             |
| django_template | 34.1 ms                                                                | 41.5 ms: 1.22x slower                                             |
| genshi_text     | 20.9 ms                                                                | 27.6 ms: 1.32x slower                                             |
| mako            | 11.6 ms                                                                | 15.9 ms: 1.38x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 4.57 ms                                                                | 1.68 ms: 2.71x faster                                             |
| create_gc_cycles           | 1.86 ms                                                                | 1.41 ms: 1.32x faster                                             |
| async_tree_io_tg           | 632 ms                                                                 | 563 ms: 1.12x faster                                              |
| async_tree_none_tg         | 265 ms                                                                 | 242 ms: 1.09x faster                                              |
| xml_etree_iterparse        | 91.6 ms                                                                | 87.9 ms: 1.04x faster                                             |
| sqlite_synth               | 2.14 us                                                                | 2.05 us: 1.04x faster                                             |
| async_tree_io              | 624 ms                                                                 | 602 ms: 1.04x faster                                              |
| pidigits                   | 196 ms                                                                 | 191 ms: 1.02x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                              |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 495 ms: 1.01x slower                                              |
| pathlib                    | 18.2 ms                                                                | 18.8 ms: 1.04x slower                                             |
| regex_v8                   | 23.6 ms                                                                | 24.6 ms: 1.04x slower                                             |
| regex_effbot               | 2.80 ms                                                                | 2.94 ms: 1.05x slower                                             |
| async_tree_none            | 271 ms                                                                 | 284 ms: 1.05x slower                                              |
| coroutines                 | 22.1 ms                                                                | 23.3 ms: 1.05x slower                                             |
| async_tree_memoization     | 327 ms                                                                 | 345 ms: 1.06x slower                                              |
| logging_silent             | 104 ns                                                                 | 110 ns: 1.06x slower                                              |
| python_startup             | 14.8 ms                                                                | 15.6 ms: 1.06x slower                                             |
| json                       | 5.15 ms                                                                | 5.46 ms: 1.06x slower                                             |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 532 ms: 1.06x slower                                              |
| pycparser                  | 1.11 sec                                                               | 1.19 sec: 1.07x slower                                            |
| bench_mp_pool              | 88.8 ms                                                                | 95.5 ms: 1.08x slower                                             |
| generators                 | 29.4 ms                                                                | 31.9 ms: 1.09x slower                                             |
| json_loads                 | 28.8 us                                                                | 31.6 us: 1.10x slower                                             |
| json_dumps                 | 11.6 ms                                                                | 12.8 ms: 1.10x slower                                             |
| docutils                   | 2.55 sec                                                               | 2.81 sec: 1.10x slower                                            |
| mdp                        | 2.45 sec                                                               | 2.71 sec: 1.10x slower                                            |
| dulwich_log                | 75.0 ms                                                                | 83.4 ms: 1.11x slower                                             |
| k_core                     | 2.06 sec                                                               | 2.31 sec: 1.12x slower                                            |
| regex_dna                  | 165 ms                                                                 | 185 ms: 1.12x slower                                              |
| bpe_tokeniser              | 4.14 sec                                                               | 4.66 sec: 1.13x slower                                            |
| scimark_sor                | 113 ms                                                                 | 128 ms: 1.13x slower                                              |
| sphinx                     | 979 ms                                                                 | 1.11 sec: 1.14x slower                                            |
| unpickle_pure_python       | 212 us                                                                 | 243 us: 1.14x slower                                              |
| pickle_pure_python         | 311 us                                                                 | 355 us: 1.14x slower                                              |
| sqlglot_normalize          | 102 ms                                                                 | 117 ms: 1.15x slower                                              |
| xml_etree_generate         | 83.4 ms                                                                | 95.8 ms: 1.15x slower                                             |
| subparsers                 | 22.3 ms                                                                | 25.8 ms: 1.15x slower                                             |
| pylint                     | 277 ms                                                                 | 320 ms: 1.16x slower                                              |
| async_generators           | 323 ms                                                                 | 375 ms: 1.16x slower                                              |
| pprint_safe_repr           | 687 ms                                                                 | 803 ms: 1.17x slower                                              |
| many_optionals             | 1.02 ms                                                                | 1.19 ms: 1.17x slower                                             |
| xml_etree_process          | 58.0 ms                                                                | 68.1 ms: 1.17x slower                                             |
| sqlglot_optimize           | 51.4 ms                                                                | 60.4 ms: 1.17x slower                                             |
| logging_simple             | 6.10 us                                                                | 7.22 us: 1.18x slower                                             |
| pprint_pformat             | 1.40 sec                                                               | 1.66 sec: 1.19x slower                                            |
| logging_format             | 6.82 us                                                                | 8.14 us: 1.19x slower                                             |
| go                         | 115 ms                                                                 | 138 ms: 1.19x slower                                              |
| 2to3                       | 255 ms                                                                 | 305 ms: 1.20x slower                                              |
| sqlglot_transpile          | 1.55 ms                                                                | 1.85 ms: 1.20x slower                                             |
| regex_compile              | 126 ms                                                                 | 151 ms: 1.20x slower                                              |
| nqueens                    | 78.9 ms                                                                | 95.2 ms: 1.21x slower                                             |
| pyflate                    | 410 ms                                                                 | 494 ms: 1.21x slower                                              |
| coverage                   | 78.7 ms                                                                | 95.1 ms: 1.21x slower                                             |
| sympy_expand               | 455 ms                                                                 | 549 ms: 1.21x slower                                              |
| raytrace                   | 263 ms                                                                 | 318 ms: 1.21x slower                                              |
| deepcopy                   | 252 us                                                                 | 305 us: 1.21x slower                                              |
| telco                      | 7.19 ms                                                                | 8.71 ms: 1.21x slower                                             |
| thrift                     | 744 us                                                                 | 902 us: 1.21x slower                                              |
| chaos                      | 56.4 ms                                                                | 68.4 ms: 1.21x slower                                             |
| genshi_xml                 | 48.2 ms                                                                | 58.5 ms: 1.21x slower                                             |
| django_template            | 34.1 ms                                                                | 41.5 ms: 1.22x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 137 ms: 1.22x slower                                              |
| comprehensions             | 16.3 us                                                                | 19.9 us: 1.22x slower                                             |
| sympy_sum                  | 152 ms                                                                 | 187 ms: 1.23x slower                                              |
| sqlglot_parse              | 1.25 ms                                                                | 1.53 ms: 1.23x slower                                             |
| sympy_integrate            | 19.7 ms                                                                | 24.2 ms: 1.23x slower                                             |
| tomli_loads                | 1.90 sec                                                               | 2.34 sec: 1.23x slower                                            |
| deepcopy_reduce            | 2.58 us                                                                | 3.18 us: 1.23x slower                                             |
| sympy_str                  | 271 ms                                                                 | 336 ms: 1.24x slower                                              |
| sqlalchemy_declarative     | 127 ms                                                                 | 158 ms: 1.25x slower                                              |
| connected_components       | 394 ms                                                                 | 491 ms: 1.25x slower                                              |
| spectral_norm              | 88.7 ms                                                                | 111 ms: 1.25x slower                                              |
| scimark_fft                | 311 ms                                                                 | 392 ms: 1.26x slower                                              |
| deepcopy_memo              | 29.8 us                                                                | 37.6 us: 1.26x slower                                             |
| shortest_path              | 431 ms                                                                 | 545 ms: 1.26x slower                                              |
| meteor_contest             | 99.7 ms                                                                | 128 ms: 1.28x slower                                              |
| hexiom                     | 5.86 ms                                                                | 7.50 ms: 1.28x slower                                             |
| typing_runtime_protocols   | 153 us                                                                 | 197 us: 1.29x slower                                              |
| sqlalchemy_imperative      | 19.1 ms                                                                | 24.7 ms: 1.29x slower                                             |
| python_startup_no_site     | 7.52 ms                                                                | 9.78 ms: 1.30x slower                                             |
| scimark_monte_carlo        | 62.8 ms                                                                | 81.8 ms: 1.30x slower                                             |
| richards                   | 42.6 ms                                                                | 55.6 ms: 1.30x slower                                             |
| crypto_pyaes               | 66.9 ms                                                                | 87.7 ms: 1.31x slower                                             |
| genshi_text                | 20.9 ms                                                                | 27.6 ms: 1.32x slower                                             |
| scimark_sparse_mat_mult    | 4.37 ms                                                                | 5.83 ms: 1.33x slower                                             |
| fannkuch                   | 365 ms                                                                 | 490 ms: 1.34x slower                                              |
| richards_super             | 48.2 ms                                                                | 65.0 ms: 1.35x slower                                             |
| mako                       | 11.6 ms                                                                | 15.9 ms: 1.38x slower                                             |
| nbody                      | 91.6 ms                                                                | 132 ms: 1.44x slower                                              |
| deltablue                  | 3.14 ms                                                                | 4.62 ms: 1.47x slower                                             |
| bench_thread_pool          | 1.03 ms                                                                | 3.31 ms: 3.22x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.15x slower                                                      |

Benchmark hidden because not significant (3): async_tree_memoization_tg, float, xml_etree_parse
Ignored benchmarks (1) of results/bm-20250206-3.14.0a4+-7bd7810-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-7bd7810.json: html5lib

- Geometric mean (including insignificant results): 1.125x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x