# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: e093464
- commit date: 2025-02-11
- overall geometric mean: 1.121x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 301 ms: 1.18x slower                                                  |
| docutils       | 2.55 sec                                                               | 2.81 sec: 1.10x slower                                                |
| sphinx         | 979 ms                                                                 | 1.11 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 632 ms                                                                 | 565 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 265 ms                                                                 | 247 ms: 1.07x faster                                                  |
| async_tree_io              | 624 ms                                                                 | 604 ms: 1.03x faster                                                  |
| async_tree_memoization_tg  | 314 ms                                                                 | 318 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 500 ms: 1.02x slower                                                  |
| async_tree_none            | 271 ms                                                                 | 286 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 533 ms: 1.06x slower                                                  |
| async_tree_memoization     | 327 ms                                                                 | 351 ms: 1.07x slower                                                  |
| coroutines                 | 22.1 ms                                                                | 24.4 ms: 1.11x slower                                                 |
| async_generators           | 323 ms                                                                 | 371 ms: 1.15x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.7 ms                                                                | 71.8 ms: 1.01x faster                                                 |
| pidigits       | 196 ms                                                                 | 194 ms: 1.01x faster                                                  |
| nbody          | 91.6 ms                                                                | 124 ms: 1.36x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.6 ms                                                                | 23.4 ms: 1.01x faster                                                 |
| regex_effbot   | 2.80 ms                                                                | 2.84 ms: 1.01x slower                                                 |
| regex_dna      | 165 ms                                                                 | 177 ms: 1.07x slower                                                  |
| regex_compile  | 126 ms                                                                 | 150 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.6 ms                                                                | 88.8 ms: 1.03x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| json_loads           | 28.8 us                                                                | 31.3 us: 1.09x slower                                                 |
| json_dumps           | 11.6 ms                                                                | 12.8 ms: 1.10x slower                                                 |
| xml_etree_generate   | 83.4 ms                                                                | 96.1 ms: 1.15x slower                                                 |
| unpickle_pure_python | 212 us                                                                 | 247 us: 1.16x slower                                                  |
| pickle_pure_python   | 311 us                                                                 | 364 us: 1.17x slower                                                  |
| xml_etree_process    | 58.0 ms                                                                | 68.8 ms: 1.19x slower                                                 |
| tomli_loads          | 1.90 sec                                                               | 2.27 sec: 1.19x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                | 15.3 ms: 1.04x slower                                                 |
| python_startup_no_site | 7.52 ms                                                                | 9.60 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.15x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.2 ms                                                                | 58.7 ms: 1.22x slower                                                 |
| django_template | 34.1 ms                                                                | 42.7 ms: 1.25x slower                                                 |
| genshi_text     | 20.9 ms                                                                | 27.4 ms: 1.31x slower                                                 |
| mako            | 11.6 ms                                                                | 15.8 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.57 ms                                                                | 1.74 ms: 2.63x faster                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.37 ms: 1.36x faster                                                 |
| async_tree_io_tg           | 632 ms                                                                 | 565 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 265 ms                                                                 | 247 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.14 us                                                                | 2.04 us: 1.05x faster                                                 |
| async_tree_io              | 624 ms                                                                 | 604 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 91.6 ms                                                                | 88.8 ms: 1.03x faster                                                 |
| float                      | 72.7 ms                                                                | 71.8 ms: 1.01x faster                                                 |
| pidigits                   | 196 ms                                                                 | 194 ms: 1.01x faster                                                  |
| regex_v8                   | 23.6 ms                                                                | 23.4 ms: 1.01x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 314 ms                                                                 | 318 ms: 1.01x slower                                                  |
| regex_effbot               | 2.80 ms                                                                | 2.84 ms: 1.01x slower                                                 |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 500 ms: 1.02x slower                                                  |
| python_startup             | 14.8 ms                                                                | 15.3 ms: 1.04x slower                                                 |
| pathlib                    | 18.2 ms                                                                | 18.8 ms: 1.04x slower                                                 |
| json                       | 5.15 ms                                                                | 5.37 ms: 1.04x slower                                                 |
| bench_mp_pool              | 88.8 ms                                                                | 93.2 ms: 1.05x slower                                                 |
| async_tree_none            | 271 ms                                                                 | 286 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 533 ms: 1.06x slower                                                  |
| logging_silent             | 104 ns                                                                 | 111 ns: 1.07x slower                                                  |
| async_tree_memoization     | 327 ms                                                                 | 351 ms: 1.07x slower                                                  |
| regex_dna                  | 165 ms                                                                 | 177 ms: 1.07x slower                                                  |
| mdp                        | 2.45 sec                                                               | 2.63 sec: 1.07x slower                                                |
| pycparser                  | 1.11 sec                                                               | 1.20 sec: 1.07x slower                                                |
| json_loads                 | 28.8 us                                                                | 31.3 us: 1.09x slower                                                 |
| docutils                   | 2.55 sec                                                               | 2.81 sec: 1.10x slower                                                |
| dulwich_log                | 75.0 ms                                                                | 82.5 ms: 1.10x slower                                                 |
| json_dumps                 | 11.6 ms                                                                | 12.8 ms: 1.10x slower                                                 |
| coroutines                 | 22.1 ms                                                                | 24.4 ms: 1.11x slower                                                 |
| k_core                     | 2.06 sec                                                               | 2.30 sec: 1.11x slower                                                |
| bpe_tokeniser              | 4.14 sec                                                               | 4.66 sec: 1.13x slower                                                |
| many_optionals             | 1.02 ms                                                                | 1.15 ms: 1.13x slower                                                 |
| sphinx                     | 979 ms                                                                 | 1.11 sec: 1.13x slower                                                |
| subparsers                 | 22.3 ms                                                                | 25.5 ms: 1.14x slower                                                 |
| async_generators           | 323 ms                                                                 | 371 ms: 1.15x slower                                                  |
| telco                      | 7.19 ms                                                                | 8.28 ms: 1.15x slower                                                 |
| xml_etree_generate         | 83.4 ms                                                                | 96.1 ms: 1.15x slower                                                 |
| pylint                     | 277 ms                                                                 | 319 ms: 1.15x slower                                                  |
| scimark_fft                | 311 ms                                                                 | 360 ms: 1.16x slower                                                  |
| pprint_safe_repr           | 687 ms                                                                 | 797 ms: 1.16x slower                                                  |
| unpickle_pure_python       | 212 us                                                                 | 247 us: 1.16x slower                                                  |
| sqlglot_normalize          | 102 ms                                                                 | 120 ms: 1.17x slower                                                  |
| pickle_pure_python         | 311 us                                                                 | 364 us: 1.17x slower                                                  |
| pprint_pformat             | 1.40 sec                                                               | 1.64 sec: 1.17x slower                                                |
| scimark_sor                | 113 ms                                                                 | 133 ms: 1.18x slower                                                  |
| 2to3                       | 255 ms                                                                 | 301 ms: 1.18x slower                                                  |
| scimark_sparse_mat_mult    | 4.37 ms                                                                | 5.17 ms: 1.18x slower                                                 |
| xml_etree_process          | 58.0 ms                                                                | 68.8 ms: 1.19x slower                                                 |
| sqlglot_optimize           | 51.4 ms                                                                | 61.0 ms: 1.19x slower                                                 |
| go                         | 115 ms                                                                 | 137 ms: 1.19x slower                                                  |
| logging_simple             | 6.10 us                                                                | 7.27 us: 1.19x slower                                                 |
| tomli_loads                | 1.90 sec                                                               | 2.27 sec: 1.19x slower                                                |
| regex_compile              | 126 ms                                                                 | 150 ms: 1.20x slower                                                  |
| thrift                     | 744 us                                                                 | 891 us: 1.20x slower                                                  |
| generators                 | 29.4 ms                                                                | 35.2 ms: 1.20x slower                                                 |
| sqlglot_transpile          | 1.55 ms                                                                | 1.86 ms: 1.20x slower                                                 |
| deepcopy                   | 252 us                                                                 | 303 us: 1.20x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 135 ms: 1.20x slower                                                  |
| raytrace                   | 263 ms                                                                 | 318 ms: 1.21x slower                                                  |
| pyflate                    | 410 ms                                                                 | 496 ms: 1.21x slower                                                  |
| sympy_expand               | 455 ms                                                                 | 552 ms: 1.21x slower                                                  |
| logging_format             | 6.82 us                                                                | 8.29 us: 1.22x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.9 ms: 1.22x slower                                                 |
| genshi_xml                 | 48.2 ms                                                                | 58.7 ms: 1.22x slower                                                 |
| nqueens                    | 78.9 ms                                                                | 96.4 ms: 1.22x slower                                                 |
| sympy_sum                  | 152 ms                                                                 | 186 ms: 1.22x slower                                                  |
| comprehensions             | 16.3 us                                                                | 20.0 us: 1.23x slower                                                 |
| deepcopy_reduce            | 2.58 us                                                                | 3.17 us: 1.23x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                                | 1.54 ms: 1.23x slower                                                 |
| connected_components       | 394 ms                                                                 | 484 ms: 1.23x slower                                                  |
| deepcopy_memo              | 29.8 us                                                                | 36.7 us: 1.23x slower                                                 |
| chaos                      | 56.4 ms                                                                | 69.7 ms: 1.24x slower                                                 |
| sympy_str                  | 271 ms                                                                 | 335 ms: 1.24x slower                                                  |
| sqlalchemy_declarative     | 127 ms                                                                 | 158 ms: 1.24x slower                                                  |
| shortest_path              | 431 ms                                                                 | 539 ms: 1.25x slower                                                  |
| spectral_norm              | 88.7 ms                                                                | 111 ms: 1.25x slower                                                  |
| django_template            | 34.1 ms                                                                | 42.7 ms: 1.25x slower                                                 |
| coverage                   | 78.7 ms                                                                | 99.0 ms: 1.26x slower                                                 |
| hexiom                     | 5.86 ms                                                                | 7.39 ms: 1.26x slower                                                 |
| sqlalchemy_imperative      | 19.1 ms                                                                | 24.2 ms: 1.26x slower                                                 |
| scimark_monte_carlo        | 62.8 ms                                                                | 79.5 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.52 ms                                                                | 9.60 ms: 1.28x slower                                                 |
| meteor_contest             | 99.7 ms                                                                | 128 ms: 1.28x slower                                                  |
| richards                   | 42.6 ms                                                                | 55.1 ms: 1.29x slower                                                 |
| crypto_pyaes               | 66.9 ms                                                                | 86.6 ms: 1.29x slower                                                 |
| fannkuch                   | 365 ms                                                                 | 473 ms: 1.30x slower                                                  |
| genshi_text                | 20.9 ms                                                                | 27.4 ms: 1.31x slower                                                 |
| typing_runtime_protocols   | 153 us                                                                 | 203 us: 1.32x slower                                                  |
| richards_super             | 48.2 ms                                                                | 64.1 ms: 1.33x slower                                                 |
| nbody                      | 91.6 ms                                                                | 124 ms: 1.36x slower                                                  |
| mako                       | 11.6 ms                                                                | 15.8 ms: 1.37x slower                                                 |
| deltablue                  | 3.14 ms                                                                | 4.64 ms: 1.48x slower                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 3.29 ms: 3.20x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.15x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (1) of results/bm-20250211-3.14.0a4+-e093464-NOGIL/bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464.json: html5lib

- Geometric mean (including insignificant results): 1.121x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x