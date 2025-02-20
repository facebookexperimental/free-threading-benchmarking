# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 08402c0
- commit date: 2025-02-19
- overall geometric mean: 1.051x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 302 ms                                                                 | 285 ms: 1.06x faster                                                  |
| docutils       | 2.79 sec                                                               | 2.70 sec: 1.04x faster                                                |
| html5lib       | 72.2 ms                                                                | 65.6 ms: 1.10x faster                                                 |
| sphinx         | 1.09 sec                                                               | 1.06 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 242 ms                                                                 | 228 ms: 1.06x faster                                                  |
| async_tree_io              | 588 ms                                                                 | 559 ms: 1.05x faster                                                  |
| async_tree_memoization     | 341 ms                                                                 | 326 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 556 ms                                                                 | 534 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 295 ms: 1.04x faster                                                  |
| async_tree_none            | 278 ms                                                                 | 267 ms: 1.04x faster                                                  |
| coroutines                 | 23.1 ms                                                                | 22.3 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 528 ms                                                                 | 515 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                 | 483 ms: 1.02x faster                                                  |
| async_generators           | 372 ms                                                                 | 367 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 130 ms                                                                 | 114 ms: 1.14x faster                                                  |
| float          | 75.8 ms                                                                | 67.7 ms: 1.12x faster                                                 |
| pidigits       | 189 ms                                                                 | 203 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 154 ms                                                                 | 143 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                                 | 181 ms: 1.00x slower                                                  |
| regex_effbot   | 2.74 ms                                                                | 2.76 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                                               | 2.07 sec: 1.13x faster                                                |
| unpickle_pure_python | 250 us                                                                 | 227 us: 1.10x faster                                                  |
| pickle_pure_python   | 361 us                                                                 | 330 us: 1.09x faster                                                  |
| xml_etree_process    | 69.8 ms                                                                | 66.1 ms: 1.06x faster                                                 |
| xml_etree_generate   | 95.6 ms                                                                | 91.6 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 88.0 ms                                                                | 85.5 ms: 1.03x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.01x faster                                                  |
| json_dumps           | 12.9 ms                                                                | 12.7 ms: 1.01x faster                                                 |
| json_loads           | 31.4 us                                                                | 31.5 us: 1.00x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.57 ms                                                                | 9.58 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 15.9 ms                                                                | 14.8 ms: 1.07x faster                                                 |
| genshi_text     | 27.6 ms                                                                | 25.8 ms: 1.07x faster                                                 |
| genshi_xml      | 58.3 ms                                                                | 55.3 ms: 1.06x faster                                                 |
| django_template | 42.6 ms                                                                | 41.6 ms: 1.03x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| go                         | 139 ms                                                                 | 121 ms: 1.15x faster                                                  |
| nbody                      | 130 ms                                                                 | 114 ms: 1.14x faster                                                  |
| logging_silent             | 110 ns                                                                 | 96.7 ns: 1.14x faster                                                 |
| tomli_loads                | 2.33 sec                                                               | 2.07 sec: 1.13x faster                                                |
| scimark_fft                | 387 ms                                                                 | 345 ms: 1.12x faster                                                  |
| float                      | 75.8 ms                                                                | 67.7 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 82.1 ms                                                                | 73.5 ms: 1.12x faster                                                 |
| deltablue                  | 3.84 ms                                                                | 3.45 ms: 1.11x faster                                                 |
| chaos                      | 70.3 ms                                                                | 63.2 ms: 1.11x faster                                                 |
| richards                   | 54.9 ms                                                                | 49.3 ms: 1.11x faster                                                 |
| scimark_sparse_mat_mult    | 5.65 ms                                                                | 5.08 ms: 1.11x faster                                                 |
| raytrace                   | 324 ms                                                                 | 292 ms: 1.11x faster                                                  |
| hexiom                     | 7.35 ms                                                                | 6.66 ms: 1.11x faster                                                 |
| deepcopy_memo              | 37.8 us                                                                | 34.2 us: 1.10x faster                                                 |
| richards_super             | 63.8 ms                                                                | 57.8 ms: 1.10x faster                                                 |
| unpickle_pure_python       | 250 us                                                                 | 227 us: 1.10x faster                                                  |
| html5lib                   | 72.2 ms                                                                | 65.6 ms: 1.10x faster                                                 |
| pprint_pformat             | 1.75 sec                                                               | 1.59 sec: 1.10x faster                                                |
| pprint_safe_repr           | 845 ms                                                                 | 770 ms: 1.10x faster                                                  |
| nqueens                    | 97.1 ms                                                                | 88.8 ms: 1.09x faster                                                 |
| pickle_pure_python         | 361 us                                                                 | 330 us: 1.09x faster                                                  |
| sqlglot_parse              | 1.58 ms                                                                | 1.46 ms: 1.09x faster                                                 |
| fannkuch                   | 492 ms                                                                 | 453 ms: 1.09x faster                                                  |
| scimark_sor                | 130 ms                                                                 | 120 ms: 1.08x faster                                                  |
| generators                 | 31.9 ms                                                                | 29.4 ms: 1.08x faster                                                 |
| sqlglot_transpile          | 1.91 ms                                                                | 1.76 ms: 1.08x faster                                                 |
| scimark_lu                 | 138 ms                                                                 | 127 ms: 1.08x faster                                                  |
| mako                       | 15.9 ms                                                                | 14.8 ms: 1.07x faster                                                 |
| pyflate                    | 496 ms                                                                 | 462 ms: 1.07x faster                                                  |
| regex_compile              | 154 ms                                                                 | 143 ms: 1.07x faster                                                  |
| genshi_text                | 27.6 ms                                                                | 25.8 ms: 1.07x faster                                                 |
| mdp                        | 2.69 sec                                                               | 2.51 sec: 1.07x faster                                                |
| async_tree_none_tg         | 242 ms                                                                 | 228 ms: 1.06x faster                                                  |
| 2to3                       | 302 ms                                                                 | 285 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.69 sec                                                               | 4.42 sec: 1.06x faster                                                |
| comprehensions             | 19.7 us                                                                | 18.6 us: 1.06x faster                                                 |
| xml_etree_process          | 69.8 ms                                                                | 66.1 ms: 1.06x faster                                                 |
| genshi_xml                 | 58.3 ms                                                                | 55.3 ms: 1.06x faster                                                 |
| sqlglot_normalize          | 121 ms                                                                 | 115 ms: 1.05x faster                                                  |
| sqlglot_optimize           | 61.4 ms                                                                | 58.4 ms: 1.05x faster                                                 |
| many_optionals             | 1.18 ms                                                                | 1.12 ms: 1.05x faster                                                 |
| async_tree_io              | 588 ms                                                                 | 559 ms: 1.05x faster                                                  |
| async_tree_memoization     | 341 ms                                                                 | 326 ms: 1.04x faster                                                  |
| xml_etree_generate         | 95.6 ms                                                                | 91.6 ms: 1.04x faster                                                 |
| logging_format             | 8.15 us                                                                | 7.81 us: 1.04x faster                                                 |
| pycparser                  | 1.19 sec                                                               | 1.14 sec: 1.04x faster                                                |
| crypto_pyaes               | 86.8 ms                                                                | 83.2 ms: 1.04x faster                                                 |
| deepcopy                   | 308 us                                                                 | 295 us: 1.04x faster                                                  |
| connected_components       | 499 ms                                                                 | 478 ms: 1.04x faster                                                  |
| logging_simple             | 7.19 us                                                                | 6.90 us: 1.04x faster                                                 |
| async_tree_io_tg           | 556 ms                                                                 | 534 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 295 ms: 1.04x faster                                                  |
| async_tree_none            | 278 ms                                                                 | 267 ms: 1.04x faster                                                  |
| sympy_integrate            | 23.9 ms                                                                | 23.0 ms: 1.04x faster                                                 |
| docutils                   | 2.79 sec                                                               | 2.70 sec: 1.04x faster                                                |
| coroutines                 | 23.1 ms                                                                | 22.3 ms: 1.03x faster                                                 |
| sphinx                     | 1.09 sec                                                               | 1.06 sec: 1.03x faster                                                |
| sympy_str                  | 331 ms                                                                 | 321 ms: 1.03x faster                                                  |
| sympy_expand               | 542 ms                                                                 | 526 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 88.0 ms                                                                | 85.5 ms: 1.03x faster                                                 |
| deepcopy_reduce            | 3.13 us                                                                | 3.04 us: 1.03x faster                                                 |
| shortest_path              | 548 ms                                                                 | 533 ms: 1.03x faster                                                  |
| sqlite_synth               | 2.07 us                                                                | 2.02 us: 1.03x faster                                                 |
| sqlalchemy_imperative      | 23.9 ms                                                                | 23.3 ms: 1.03x faster                                                 |
| django_template            | 42.6 ms                                                                | 41.6 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 528 ms                                                                 | 515 ms: 1.03x faster                                                  |
| telco                      | 8.66 ms                                                                | 8.45 ms: 1.03x faster                                                 |
| k_core                     | 2.31 sec                                                               | 2.25 sec: 1.02x faster                                                |
| pathlib                    | 19.8 ms                                                                | 19.4 ms: 1.02x faster                                                 |
| sympy_sum                  | 186 ms                                                                 | 181 ms: 1.02x faster                                                  |
| pylint                     | 314 ms                                                                 | 306 ms: 1.02x faster                                                  |
| dulwich_log                | 82.6 ms                                                                | 80.8 ms: 1.02x faster                                                 |
| meteor_contest             | 129 ms                                                                 | 127 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                 | 483 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 195 us                                                                 | 192 us: 1.02x faster                                                  |
| sqlalchemy_declarative     | 156 ms                                                                 | 153 ms: 1.02x faster                                                  |
| coverage                   | 96.9 ms                                                                | 95.3 ms: 1.02x faster                                                 |
| bench_thread_pool          | 3.31 ms                                                                | 3.26 ms: 1.02x faster                                                 |
| async_generators           | 372 ms                                                                 | 367 ms: 1.01x faster                                                  |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.01x faster                                                  |
| thrift                     | 883 us                                                                 | 872 us: 1.01x faster                                                  |
| json_dumps                 | 12.9 ms                                                                | 12.7 ms: 1.01x faster                                                 |
| subparsers                 | 25.3 ms                                                                | 25.0 ms: 1.01x faster                                                 |
| bench_mp_pool              | 95.0 ms                                                                | 94.3 ms: 1.01x faster                                                 |
| create_gc_cycles           | 1.36 ms                                                                | 1.35 ms: 1.01x faster                                                 |
| gc_traversal               | 1.72 ms                                                                | 1.71 ms: 1.01x faster                                                 |
| spectral_norm              | 106 ms                                                                 | 106 ms: 1.00x faster                                                  |
| python_startup_no_site     | 9.57 ms                                                                | 9.58 ms: 1.00x slower                                                 |
| regex_dna                  | 180 ms                                                                 | 181 ms: 1.00x slower                                                  |
| json_loads                 | 31.4 us                                                                | 31.5 us: 1.00x slower                                                 |
| regex_effbot               | 2.74 ms                                                                | 2.76 ms: 1.01x slower                                                 |
| pidigits                   | 189 ms                                                                 | 203 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (4): regex_v8, json, asyncio_websockets, python_startup

- Geometric mean (including insignificant results): 1.051x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.00x