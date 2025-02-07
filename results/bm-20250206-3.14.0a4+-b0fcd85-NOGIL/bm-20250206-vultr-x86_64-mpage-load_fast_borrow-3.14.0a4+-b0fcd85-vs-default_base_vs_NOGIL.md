# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow
- machine: linux-x86_64
- commit hash: b0fcd85
- commit date: 2025-02-06
- overall geometric mean: 1.121x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 303 ms: 1.19x slower                                              |
| docutils       | 2.55 sec                                                               | 2.81 sec: 1.10x slower                                            |
| sphinx         | 979 ms                                                                 | 1.11 sec: 1.13x slower                                            |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 632 ms                                                                 | 556 ms: 1.14x faster                                              |
| async_tree_none_tg         | 265 ms                                                                 | 241 ms: 1.10x faster                                              |
| async_tree_io              | 624 ms                                                                 | 589 ms: 1.06x faster                                              |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 497 ms: 1.02x slower                                              |
| async_tree_none            | 271 ms                                                                 | 281 ms: 1.04x slower                                              |
| coroutines                 | 22.1 ms                                                                | 22.9 ms: 1.04x slower                                             |
| async_tree_memoization     | 327 ms                                                                 | 344 ms: 1.05x slower                                              |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 531 ms: 1.06x slower                                              |
| async_generators           | 323 ms                                                                 | 372 ms: 1.15x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (2): async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 196 ms                                                                 | 202 ms: 1.03x slower                                              |
| nbody          | 91.6 ms                                                                | 131 ms: 1.43x slower                                              |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                      |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 23.6 ms                                                                | 23.2 ms: 1.02x faster                                             |
| regex_effbot   | 2.80 ms                                                                | 2.79 ms: 1.01x faster                                             |
| regex_dna      | 165 ms                                                                 | 184 ms: 1.11x slower                                              |
| regex_compile  | 126 ms                                                                 | 152 ms: 1.21x slower                                              |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 91.6 ms                                                                | 87.3 ms: 1.05x faster                                             |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                              |
| json_loads           | 28.8 us                                                                | 31.6 us: 1.10x slower                                             |
| json_dumps           | 11.6 ms                                                                | 12.7 ms: 1.10x slower                                             |
| unpickle_pure_python | 212 us                                                                 | 240 us: 1.13x slower                                              |
| pickle_pure_python   | 311 us                                                                 | 354 us: 1.14x slower                                              |
| xml_etree_generate   | 83.4 ms                                                                | 95.2 ms: 1.14x slower                                             |
| xml_etree_process    | 58.0 ms                                                                | 68.0 ms: 1.17x slower                                             |
| tomli_loads          | 1.90 sec                                                               | 2.33 sec: 1.23x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                | 15.6 ms: 1.06x slower                                             |
| python_startup_no_site | 7.52 ms                                                                | 9.77 ms: 1.30x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 34.1 ms                                                                | 41.4 ms: 1.21x slower                                             |
| genshi_xml      | 48.2 ms                                                                | 58.7 ms: 1.22x slower                                             |
| genshi_text     | 20.9 ms                                                                | 27.6 ms: 1.32x slower                                             |
| mako            | 11.6 ms                                                                | 16.0 ms: 1.38x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 4.57 ms                                                                | 1.67 ms: 2.73x faster                                             |
| create_gc_cycles           | 1.86 ms                                                                | 1.40 ms: 1.33x faster                                             |
| async_tree_io_tg           | 632 ms                                                                 | 556 ms: 1.14x faster                                              |
| async_tree_none_tg         | 265 ms                                                                 | 241 ms: 1.10x faster                                              |
| sqlite_synth               | 2.14 us                                                                | 2.01 us: 1.06x faster                                             |
| async_tree_io              | 624 ms                                                                 | 589 ms: 1.06x faster                                              |
| xml_etree_iterparse        | 91.6 ms                                                                | 87.3 ms: 1.05x faster                                             |
| regex_v8                   | 23.6 ms                                                                | 23.2 ms: 1.02x faster                                             |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                              |
| regex_effbot               | 2.80 ms                                                                | 2.79 ms: 1.01x faster                                             |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 497 ms: 1.02x slower                                              |
| logging_silent             | 104 ns                                                                 | 106 ns: 1.02x slower                                              |
| pathlib                    | 18.2 ms                                                                | 18.6 ms: 1.03x slower                                             |
| pidigits                   | 196 ms                                                                 | 202 ms: 1.03x slower                                              |
| async_tree_none            | 271 ms                                                                 | 281 ms: 1.04x slower                                              |
| coroutines                 | 22.1 ms                                                                | 22.9 ms: 1.04x slower                                             |
| json                       | 5.15 ms                                                                | 5.41 ms: 1.05x slower                                             |
| async_tree_memoization     | 327 ms                                                                 | 344 ms: 1.05x slower                                              |
| python_startup             | 14.8 ms                                                                | 15.6 ms: 1.06x slower                                             |
| pycparser                  | 1.11 sec                                                               | 1.18 sec: 1.06x slower                                            |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 531 ms: 1.06x slower                                              |
| bench_mp_pool              | 88.8 ms                                                                | 95.9 ms: 1.08x slower                                             |
| generators                 | 29.4 ms                                                                | 32.1 ms: 1.09x slower                                             |
| mdp                        | 2.45 sec                                                               | 2.68 sec: 1.09x slower                                            |
| json_loads                 | 28.8 us                                                                | 31.6 us: 1.10x slower                                             |
| json_dumps                 | 11.6 ms                                                                | 12.7 ms: 1.10x slower                                             |
| docutils                   | 2.55 sec                                                               | 2.81 sec: 1.10x slower                                            |
| dulwich_log                | 75.0 ms                                                                | 82.7 ms: 1.10x slower                                             |
| regex_dna                  | 165 ms                                                                 | 184 ms: 1.11x slower                                              |
| k_core                     | 2.06 sec                                                               | 2.31 sec: 1.12x slower                                            |
| bpe_tokeniser              | 4.14 sec                                                               | 4.65 sec: 1.12x slower                                            |
| unpickle_pure_python       | 212 us                                                                 | 240 us: 1.13x slower                                              |
| sphinx                     | 979 ms                                                                 | 1.11 sec: 1.13x slower                                            |
| pickle_pure_python         | 311 us                                                                 | 354 us: 1.14x slower                                              |
| scimark_sor                | 113 ms                                                                 | 129 ms: 1.14x slower                                              |
| xml_etree_generate         | 83.4 ms                                                                | 95.2 ms: 1.14x slower                                             |
| sqlglot_normalize          | 102 ms                                                                 | 117 ms: 1.14x slower                                              |
| subparsers                 | 22.3 ms                                                                | 25.5 ms: 1.14x slower                                             |
| async_generators           | 323 ms                                                                 | 372 ms: 1.15x slower                                              |
| pylint                     | 277 ms                                                                 | 318 ms: 1.15x slower                                              |
| pprint_safe_repr           | 687 ms                                                                 | 795 ms: 1.16x slower                                              |
| many_optionals             | 1.02 ms                                                                | 1.18 ms: 1.16x slower                                             |
| logging_simple             | 6.10 us                                                                | 7.14 us: 1.17x slower                                             |
| xml_etree_process          | 58.0 ms                                                                | 68.0 ms: 1.17x slower                                             |
| sqlglot_optimize           | 51.4 ms                                                                | 60.4 ms: 1.18x slower                                             |
| raytrace                   | 263 ms                                                                 | 310 ms: 1.18x slower                                              |
| pprint_pformat             | 1.40 sec                                                               | 1.65 sec: 1.18x slower                                            |
| pyflate                    | 410 ms                                                                 | 485 ms: 1.18x slower                                              |
| go                         | 115 ms                                                                 | 137 ms: 1.18x slower                                              |
| thrift                     | 744 us                                                                 | 883 us: 1.19x slower                                              |
| chaos                      | 56.4 ms                                                                | 67.1 ms: 1.19x slower                                             |
| 2to3                       | 255 ms                                                                 | 303 ms: 1.19x slower                                              |
| sqlglot_transpile          | 1.55 ms                                                                | 1.84 ms: 1.19x slower                                             |
| comprehensions             | 16.3 us                                                                | 19.5 us: 1.19x slower                                             |
| telco                      | 7.19 ms                                                                | 8.64 ms: 1.20x slower                                             |
| logging_format             | 6.82 us                                                                | 8.22 us: 1.20x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 136 ms: 1.21x slower                                              |
| regex_compile              | 126 ms                                                                 | 152 ms: 1.21x slower                                              |
| deepcopy                   | 252 us                                                                 | 304 us: 1.21x slower                                              |
| deepcopy_reduce            | 2.58 us                                                                | 3.12 us: 1.21x slower                                             |
| django_template            | 34.1 ms                                                                | 41.4 ms: 1.21x slower                                             |
| genshi_xml                 | 48.2 ms                                                                | 58.7 ms: 1.22x slower                                             |
| sqlglot_parse              | 1.25 ms                                                                | 1.52 ms: 1.22x slower                                             |
| nqueens                    | 78.9 ms                                                                | 96.2 ms: 1.22x slower                                             |
| sympy_expand               | 455 ms                                                                 | 555 ms: 1.22x slower                                              |
| sympy_integrate            | 19.7 ms                                                                | 24.1 ms: 1.22x slower                                             |
| tomli_loads                | 1.90 sec                                                               | 2.33 sec: 1.23x slower                                            |
| coverage                   | 78.7 ms                                                                | 97.2 ms: 1.23x slower                                             |
| sympy_sum                  | 152 ms                                                                 | 188 ms: 1.24x slower                                              |
| scimark_fft                | 311 ms                                                                 | 385 ms: 1.24x slower                                              |
| spectral_norm              | 88.7 ms                                                                | 110 ms: 1.24x slower                                              |
| deepcopy_memo              | 29.8 us                                                                | 37.1 us: 1.25x slower                                             |
| sqlalchemy_declarative     | 127 ms                                                                 | 158 ms: 1.25x slower                                              |
| sympy_str                  | 271 ms                                                                 | 337 ms: 1.25x slower                                              |
| hexiom                     | 5.86 ms                                                                | 7.36 ms: 1.26x slower                                             |
| connected_components       | 394 ms                                                                 | 495 ms: 1.26x slower                                              |
| shortest_path              | 431 ms                                                                 | 548 ms: 1.27x slower                                              |
| sqlalchemy_imperative      | 19.1 ms                                                                | 24.7 ms: 1.29x slower                                             |
| scimark_monte_carlo        | 62.8 ms                                                                | 81.2 ms: 1.29x slower                                             |
| meteor_contest             | 99.7 ms                                                                | 129 ms: 1.30x slower                                              |
| typing_runtime_protocols   | 153 us                                                                 | 199 us: 1.30x slower                                              |
| python_startup_no_site     | 7.52 ms                                                                | 9.77 ms: 1.30x slower                                             |
| richards                   | 42.6 ms                                                                | 55.6 ms: 1.30x slower                                             |
| genshi_text                | 20.9 ms                                                                | 27.6 ms: 1.32x slower                                             |
| crypto_pyaes               | 66.9 ms                                                                | 88.1 ms: 1.32x slower                                             |
| scimark_sparse_mat_mult    | 4.37 ms                                                                | 5.83 ms: 1.33x slower                                             |
| fannkuch                   | 365 ms                                                                 | 489 ms: 1.34x slower                                              |
| richards_super             | 48.2 ms                                                                | 65.0 ms: 1.35x slower                                             |
| mako                       | 11.6 ms                                                                | 16.0 ms: 1.38x slower                                             |
| nbody                      | 91.6 ms                                                                | 131 ms: 1.43x slower                                              |
| deltablue                  | 3.14 ms                                                                | 4.55 ms: 1.45x slower                                             |
| bench_thread_pool          | 1.03 ms                                                                | 3.30 ms: 3.21x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.15x slower                                                      |

Benchmark hidden because not significant (3): async_tree_memoization_tg, asyncio_websockets, float
Ignored benchmarks (1) of results/bm-20250206-3.14.0a4+-b0fcd85-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4+-b0fcd85.json: html5lib

- Geometric mean (including insignificant results): 1.121x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x