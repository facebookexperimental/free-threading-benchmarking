# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: dcbd5da
- commit date: 2025-02-13
- overall geometric mean: 1.054x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 304 ms                                                                 | 289 ms: 1.05x faster                                                  |
| docutils       | 2.83 sec                                                               | 2.73 sec: 1.04x faster                                                |
| html5lib       | 69.6 ms                                                                | 65.4 ms: 1.06x faster                                                 |
| sphinx         | 1.11 sec                                                               | 1.08 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 23.9 ms                                                                | 22.1 ms: 1.08x faster                                                 |
| async_tree_memoization     | 353 ms                                                                 | 335 ms: 1.05x faster                                                  |
| async_generators           | 376 ms                                                                 | 359 ms: 1.05x faster                                                  |
| async_tree_memoization_tg  | 318 ms                                                                 | 304 ms: 1.05x faster                                                  |
| async_tree_none            | 288 ms                                                                 | 276 ms: 1.05x faster                                                  |
| async_tree_io              | 608 ms                                                                 | 583 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 257 ms                                                                 | 248 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 575 ms                                                                 | 554 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                 | 489 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 537 ms                                                                 | 523 ms: 1.03x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 131 ms                                                                 | 114 ms: 1.16x faster                                                  |
| float          | 76.2 ms                                                                | 67.5 ms: 1.13x faster                                                 |
| pidigits       | 191 ms                                                                 | 209 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 151 ms                                                                 | 141 ms: 1.07x faster                                                  |
| regex_effbot   | 2.82 ms                                                                | 2.70 ms: 1.05x faster                                                 |
| regex_v8       | 24.3 ms                                                                | 23.8 ms: 1.02x faster                                                 |
| regex_dna      | 179 ms                                                                 | 180 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.35 sec                                                               | 2.07 sec: 1.14x faster                                                |
| unpickle_pure_python | 251 us                                                                 | 224 us: 1.12x faster                                                  |
| pickle_pure_python   | 362 us                                                                 | 326 us: 1.11x faster                                                  |
| xml_etree_process    | 70.3 ms                                                                | 66.7 ms: 1.05x faster                                                 |
| xml_etree_generate   | 96.5 ms                                                                | 92.8 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 88.1 ms                                                                | 85.5 ms: 1.03x faster                                                 |
| json_dumps           | 12.8 ms                                                                | 12.6 ms: 1.02x faster                                                 |
| json_loads           | 31.7 us                                                                | 31.1 us: 1.02x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.01x faster                                                  |
| Geometric mean       | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 28.1 ms                                                                | 26.0 ms: 1.08x faster                                                 |
| mako            | 15.8 ms                                                                | 15.0 ms: 1.06x faster                                                 |
| genshi_xml      | 58.9 ms                                                                | 56.0 ms: 1.05x faster                                                 |
| django_template | 42.2 ms                                                                | 40.8 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250213-vultr-x86_64-python-07f5e33f2eed50984d7a-3.14.0a5+-07f5e33 | bm-20250213-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-dcbd5da |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| go                         | 140 ms                                                                 | 120 ms: 1.16x faster                                                  |
| nbody                      | 131 ms                                                                 | 114 ms: 1.16x faster                                                  |
| pyflate                    | 511 ms                                                                 | 450 ms: 1.14x faster                                                  |
| deltablue                  | 3.89 ms                                                                | 3.43 ms: 1.14x faster                                                 |
| tomli_loads                | 2.35 sec                                                               | 2.07 sec: 1.14x faster                                                |
| deepcopy_memo              | 39.0 us                                                                | 34.5 us: 1.13x faster                                                 |
| float                      | 76.2 ms                                                                | 67.5 ms: 1.13x faster                                                 |
| scimark_sor                | 132 ms                                                                 | 117 ms: 1.12x faster                                                  |
| unpickle_pure_python       | 251 us                                                                 | 224 us: 1.12x faster                                                  |
| richards                   | 56.8 ms                                                                | 50.6 ms: 1.12x faster                                                 |
| scimark_sparse_mat_mult    | 5.86 ms                                                                | 5.24 ms: 1.12x faster                                                 |
| logging_silent             | 113 ns                                                                 | 101 ns: 1.12x faster                                                  |
| richards_super             | 65.5 ms                                                                | 58.9 ms: 1.11x faster                                                 |
| pickle_pure_python         | 362 us                                                                 | 326 us: 1.11x faster                                                  |
| scimark_monte_carlo        | 83.3 ms                                                                | 75.0 ms: 1.11x faster                                                 |
| raytrace                   | 324 ms                                                                 | 293 ms: 1.11x faster                                                  |
| scimark_fft                | 389 ms                                                                 | 352 ms: 1.11x faster                                                  |
| fannkuch                   | 493 ms                                                                 | 446 ms: 1.10x faster                                                  |
| chaos                      | 69.9 ms                                                                | 63.4 ms: 1.10x faster                                                 |
| hexiom                     | 7.40 ms                                                                | 6.71 ms: 1.10x faster                                                 |
| generators                 | 32.0 ms                                                                | 29.3 ms: 1.09x faster                                                 |
| sqlglot_parse              | 1.59 ms                                                                | 1.46 ms: 1.09x faster                                                 |
| pprint_safe_repr           | 816 ms                                                                 | 755 ms: 1.08x faster                                                  |
| coroutines                 | 23.9 ms                                                                | 22.1 ms: 1.08x faster                                                 |
| scimark_lu                 | 139 ms                                                                 | 129 ms: 1.08x faster                                                  |
| genshi_text                | 28.1 ms                                                                | 26.0 ms: 1.08x faster                                                 |
| pprint_pformat             | 1.68 sec                                                               | 1.55 sec: 1.08x faster                                                |
| sqlglot_transpile          | 1.92 ms                                                                | 1.78 ms: 1.08x faster                                                 |
| regex_compile              | 151 ms                                                                 | 141 ms: 1.07x faster                                                  |
| html5lib                   | 69.6 ms                                                                | 65.4 ms: 1.06x faster                                                 |
| crypto_pyaes               | 89.0 ms                                                                | 83.8 ms: 1.06x faster                                                 |
| comprehensions             | 20.1 us                                                                | 19.0 us: 1.06x faster                                                 |
| nqueens                    | 96.8 ms                                                                | 91.4 ms: 1.06x faster                                                 |
| spectral_norm              | 109 ms                                                                 | 103 ms: 1.06x faster                                                  |
| mako                       | 15.8 ms                                                                | 15.0 ms: 1.06x faster                                                 |
| many_optionals             | 1.19 ms                                                                | 1.13 ms: 1.06x faster                                                 |
| deepcopy_reduce            | 3.15 us                                                                | 2.98 us: 1.05x faster                                                 |
| xml_etree_process          | 70.3 ms                                                                | 66.7 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.65 sec                                                               | 4.42 sec: 1.05x faster                                                |
| async_tree_memoization     | 353 ms                                                                 | 335 ms: 1.05x faster                                                  |
| 2to3                       | 304 ms                                                                 | 289 ms: 1.05x faster                                                  |
| genshi_xml                 | 58.9 ms                                                                | 56.0 ms: 1.05x faster                                                 |
| sqlglot_optimize           | 61.3 ms                                                                | 58.3 ms: 1.05x faster                                                 |
| async_generators           | 376 ms                                                                 | 359 ms: 1.05x faster                                                  |
| pycparser                  | 1.19 sec                                                               | 1.14 sec: 1.05x faster                                                |
| async_tree_memoization_tg  | 318 ms                                                                 | 304 ms: 1.05x faster                                                  |
| regex_effbot               | 2.82 ms                                                                | 2.70 ms: 1.05x faster                                                 |
| typing_runtime_protocols   | 199 us                                                                 | 190 us: 1.05x faster                                                  |
| async_tree_none            | 288 ms                                                                 | 276 ms: 1.05x faster                                                  |
| sqlglot_normalize          | 121 ms                                                                 | 115 ms: 1.05x faster                                                  |
| telco                      | 8.56 ms                                                                | 8.20 ms: 1.04x faster                                                 |
| async_tree_io              | 608 ms                                                                 | 583 ms: 1.04x faster                                                  |
| connected_components       | 499 ms                                                                 | 479 ms: 1.04x faster                                                  |
| deepcopy                   | 308 us                                                                 | 296 us: 1.04x faster                                                  |
| logging_simple             | 7.17 us                                                                | 6.89 us: 1.04x faster                                                 |
| sympy_integrate            | 24.1 ms                                                                | 23.2 ms: 1.04x faster                                                 |
| meteor_contest             | 129 ms                                                                 | 124 ms: 1.04x faster                                                  |
| xml_etree_generate         | 96.5 ms                                                                | 92.8 ms: 1.04x faster                                                 |
| sympy_str                  | 334 ms                                                                 | 322 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 257 ms                                                                 | 248 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 575 ms                                                                 | 554 ms: 1.04x faster                                                  |
| django_template            | 42.2 ms                                                                | 40.8 ms: 1.04x faster                                                 |
| docutils                   | 2.83 sec                                                               | 2.73 sec: 1.04x faster                                                |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                 | 489 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 88.1 ms                                                                | 85.5 ms: 1.03x faster                                                 |
| sphinx                     | 1.11 sec                                                               | 1.08 sec: 1.03x faster                                                |
| shortest_path              | 549 ms                                                                 | 533 ms: 1.03x faster                                                  |
| dulwich_log                | 82.6 ms                                                                | 80.3 ms: 1.03x faster                                                 |
| logging_format             | 8.10 us                                                                | 7.88 us: 1.03x faster                                                 |
| pylint                     | 318 ms                                                                 | 309 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 537 ms                                                                 | 523 ms: 1.03x faster                                                  |
| bench_thread_pool          | 3.34 ms                                                                | 3.25 ms: 1.03x faster                                                 |
| subparsers                 | 25.4 ms                                                                | 24.8 ms: 1.03x faster                                                 |
| sqlalchemy_imperative      | 24.2 ms                                                                | 23.6 ms: 1.03x faster                                                 |
| sympy_expand               | 545 ms                                                                 | 531 ms: 1.03x faster                                                  |
| sqlalchemy_declarative     | 157 ms                                                                 | 153 ms: 1.03x faster                                                  |
| sympy_sum                  | 186 ms                                                                 | 181 ms: 1.02x faster                                                  |
| regex_v8                   | 24.3 ms                                                                | 23.8 ms: 1.02x faster                                                 |
| k_core                     | 2.31 sec                                                               | 2.27 sec: 1.02x faster                                                |
| json_dumps                 | 12.8 ms                                                                | 12.6 ms: 1.02x faster                                                 |
| json_loads                 | 31.7 us                                                                | 31.1 us: 1.02x faster                                                 |
| coverage                   | 97.1 ms                                                                | 95.6 ms: 1.02x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.03 us                                                                | 2.01 us: 1.01x faster                                                 |
| thrift                     | 890 us                                                                 | 882 us: 1.01x faster                                                  |
| bench_mp_pool              | 94.7 ms                                                                | 94.1 ms: 1.01x faster                                                 |
| pathlib                    | 19.0 ms                                                                | 19.0 ms: 1.00x faster                                                 |
| mdp                        | 2.70 sec                                                               | 2.72 sec: 1.01x slower                                                |
| regex_dna                  | 179 ms                                                                 | 180 ms: 1.01x slower                                                  |
| pidigits                   | 191 ms                                                                 | 209 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (6): json, asyncio_websockets, python_startup_no_site, python_startup, create_gc_cycles, gc_traversal

- Geometric mean (including insignificant results): 1.054x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.00x