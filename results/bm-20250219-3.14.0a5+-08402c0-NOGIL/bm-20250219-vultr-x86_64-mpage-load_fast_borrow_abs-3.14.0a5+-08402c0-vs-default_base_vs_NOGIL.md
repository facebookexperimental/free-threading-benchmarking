# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 08402c0
- commit date: 2025-02-19
- overall geometric mean: 1.077x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 285 ms: 1.12x slower                                                  |
| docutils       | 2.56 sec                                                               | 2.70 sec: 1.05x slower                                                |
| sphinx         | 983 ms                                                                 | 1.06 sec: 1.08x slower                                                |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 619 ms                                                                 | 534 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 259 ms                                                                 | 228 ms: 1.13x faster                                                  |
| async_tree_io              | 618 ms                                                                 | 559 ms: 1.10x faster                                                  |
| async_tree_memoization_tg  | 317 ms                                                                 | 295 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed_tg | 488 ms                                                                 | 483 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| coroutines                 | 22.0 ms                                                                | 22.3 ms: 1.02x slower                                                 |
| async_tree_memoization     | 318 ms                                                                 | 326 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed    | 495 ms                                                                 | 515 ms: 1.04x slower                                                  |
| async_generators           | 331 ms                                                                 | 367 ms: 1.11x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 70.9 ms                                                                | 67.7 ms: 1.05x faster                                                 |
| pidigits       | 195 ms                                                                 | 203 ms: 1.05x slower                                                  |
| nbody          | 91.5 ms                                                                | 114 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.88 ms                                                                | 2.76 ms: 1.04x faster                                                 |
| regex_v8       | 24.6 ms                                                                | 23.9 ms: 1.03x faster                                                 |
| regex_dna      | 175 ms                                                                 | 181 ms: 1.03x slower                                                  |
| regex_compile  | 128 ms                                                                 | 143 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.7 ms                                                                | 85.5 ms: 1.07x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.01x faster                                                  |
| unpickle_pure_python | 216 us                                                                 | 227 us: 1.05x slower                                                  |
| pickle_pure_python   | 310 us                                                                 | 330 us: 1.06x slower                                                  |
| xml_etree_generate   | 84.4 ms                                                                | 91.6 ms: 1.09x slower                                                 |
| tomli_loads          | 1.91 sec                                                               | 2.07 sec: 1.09x slower                                                |
| json_loads           | 28.3 us                                                                | 31.5 us: 1.11x slower                                                 |
| xml_etree_process    | 58.6 ms                                                                | 66.1 ms: 1.13x slower                                                 |
| json_dumps           | 11.1 ms                                                                | 12.7 ms: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.5 ms: 1.05x slower                                                 |
| python_startup_no_site | 7.45 ms                                                                | 9.58 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.3 ms                                                                | 55.3 ms: 1.12x slower                                                 |
| genshi_text     | 21.6 ms                                                                | 25.8 ms: 1.19x slower                                                 |
| django_template | 33.9 ms                                                                | 41.6 ms: 1.23x slower                                                 |
| mako            | 11.7 ms                                                                | 14.8 ms: 1.27x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.20x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250219-vultr-x86_64-python-6c982aeb547528174f8b-3.14.0a5+-6c982ae | bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.99 ms                                                                | 1.71 ms: 2.33x faster                                                 |
| create_gc_cycles           | 1.84 ms                                                                | 1.35 ms: 1.37x faster                                                 |
| async_tree_io_tg           | 619 ms                                                                 | 534 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 259 ms                                                                 | 228 ms: 1.13x faster                                                  |
| async_tree_io              | 618 ms                                                                 | 559 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.22 us                                                                | 2.02 us: 1.10x faster                                                 |
| async_tree_memoization_tg  | 317 ms                                                                 | 295 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 91.7 ms                                                                | 85.5 ms: 1.07x faster                                                 |
| logging_silent             | 103 ns                                                                 | 96.7 ns: 1.07x faster                                                 |
| float                      | 70.9 ms                                                                | 67.7 ms: 1.05x faster                                                 |
| regex_effbot               | 2.88 ms                                                                | 2.76 ms: 1.04x faster                                                 |
| regex_v8                   | 24.6 ms                                                                | 23.9 ms: 1.03x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 488 ms                                                                 | 483 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| generators                 | 28.9 ms                                                                | 29.4 ms: 1.02x slower                                                 |
| coroutines                 | 22.0 ms                                                                | 22.3 ms: 1.02x slower                                                 |
| pathlib                    | 19.0 ms                                                                | 19.4 ms: 1.02x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                |
| async_tree_memoization     | 318 ms                                                                 | 326 ms: 1.03x slower                                                  |
| regex_dna                  | 175 ms                                                                 | 181 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed    | 495 ms                                                                 | 515 ms: 1.04x slower                                                  |
| scimark_sor                | 115 ms                                                                 | 120 ms: 1.04x slower                                                  |
| go                         | 116 ms                                                                 | 121 ms: 1.04x slower                                                  |
| pidigits                   | 195 ms                                                                 | 203 ms: 1.05x slower                                                  |
| unpickle_pure_python       | 216 us                                                                 | 227 us: 1.05x slower                                                  |
| python_startup             | 14.7 ms                                                                | 15.5 ms: 1.05x slower                                                 |
| docutils                   | 2.56 sec                                                               | 2.70 sec: 1.05x slower                                                |
| bpe_tokeniser              | 4.17 sec                                                               | 4.42 sec: 1.06x slower                                                |
| pickle_pure_python         | 310 us                                                                 | 330 us: 1.06x slower                                                  |
| mdp                        | 2.36 sec                                                               | 2.51 sec: 1.07x slower                                                |
| bench_mp_pool              | 88.3 ms                                                                | 94.3 ms: 1.07x slower                                                 |
| dulwich_log                | 75.3 ms                                                                | 80.8 ms: 1.07x slower                                                 |
| json                       | 4.93 ms                                                                | 5.30 ms: 1.08x slower                                                 |
| sphinx                     | 983 ms                                                                 | 1.06 sec: 1.08x slower                                                |
| xml_etree_generate         | 84.4 ms                                                                | 91.6 ms: 1.09x slower                                                 |
| tomli_loads                | 1.91 sec                                                               | 2.07 sec: 1.09x slower                                                |
| k_core                     | 2.05 sec                                                               | 2.25 sec: 1.10x slower                                                |
| pprint_safe_repr           | 700 ms                                                                 | 770 ms: 1.10x slower                                                  |
| deltablue                  | 3.14 ms                                                                | 3.45 ms: 1.10x slower                                                 |
| many_optionals             | 1.02 ms                                                                | 1.12 ms: 1.10x slower                                                 |
| pylint                     | 278 ms                                                                 | 306 ms: 1.10x slower                                                  |
| sqlglot_normalize          | 104 ms                                                                 | 115 ms: 1.11x slower                                                  |
| pprint_pformat             | 1.44 sec                                                               | 1.59 sec: 1.11x slower                                                |
| async_generators           | 331 ms                                                                 | 367 ms: 1.11x slower                                                  |
| hexiom                     | 5.98 ms                                                                | 6.66 ms: 1.11x slower                                                 |
| json_loads                 | 28.3 us                                                                | 31.5 us: 1.11x slower                                                 |
| chaos                      | 56.7 ms                                                                | 63.2 ms: 1.11x slower                                                 |
| scimark_fft                | 309 ms                                                                 | 345 ms: 1.12x slower                                                  |
| pyflate                    | 413 ms                                                                 | 462 ms: 1.12x slower                                                  |
| 2to3                       | 254 ms                                                                 | 285 ms: 1.12x slower                                                  |
| genshi_xml                 | 49.3 ms                                                                | 55.3 ms: 1.12x slower                                                 |
| nqueens                    | 79.1 ms                                                                | 88.8 ms: 1.12x slower                                                 |
| regex_compile              | 128 ms                                                                 | 143 ms: 1.12x slower                                                  |
| sqlglot_optimize           | 51.9 ms                                                                | 58.4 ms: 1.13x slower                                                 |
| raytrace                   | 259 ms                                                                 | 292 ms: 1.13x slower                                                  |
| xml_etree_process          | 58.6 ms                                                                | 66.1 ms: 1.13x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                                | 1.76 ms: 1.13x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 127 ms: 1.13x slower                                                  |
| comprehensions             | 16.4 us                                                                | 18.6 us: 1.13x slower                                                 |
| subparsers                 | 21.9 ms                                                                | 25.0 ms: 1.14x slower                                                 |
| json_dumps                 | 11.1 ms                                                                | 12.7 ms: 1.15x slower                                                 |
| sympy_expand               | 457 ms                                                                 | 526 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 63.8 ms                                                                | 73.5 ms: 1.15x slower                                                 |
| deepcopy_memo              | 29.7 us                                                                | 34.2 us: 1.15x slower                                                 |
| telco                      | 7.31 ms                                                                | 8.45 ms: 1.16x slower                                                 |
| logging_simple             | 5.97 us                                                                | 6.90 us: 1.16x slower                                                 |
| scimark_sparse_mat_mult    | 4.38 ms                                                                | 5.08 ms: 1.16x slower                                                 |
| deepcopy_reduce            | 2.62 us                                                                | 3.04 us: 1.16x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.0 ms: 1.17x slower                                                 |
| deepcopy                   | 252 us                                                                 | 295 us: 1.17x slower                                                  |
| sqlglot_parse              | 1.24 ms                                                                | 1.46 ms: 1.17x slower                                                 |
| thrift                     | 741 us                                                                 | 872 us: 1.18x slower                                                  |
| richards                   | 41.9 ms                                                                | 49.3 ms: 1.18x slower                                                 |
| logging_format             | 6.63 us                                                                | 7.81 us: 1.18x slower                                                 |
| sympy_str                  | 272 ms                                                                 | 321 ms: 1.18x slower                                                  |
| fannkuch                   | 385 ms                                                                 | 453 ms: 1.18x slower                                                  |
| sympy_sum                  | 153 ms                                                                 | 181 ms: 1.18x slower                                                  |
| genshi_text                | 21.6 ms                                                                | 25.8 ms: 1.19x slower                                                 |
| coverage                   | 79.7 ms                                                                | 95.3 ms: 1.20x slower                                                 |
| sqlalchemy_declarative     | 128 ms                                                                 | 153 ms: 1.20x slower                                                  |
| sqlalchemy_imperative      | 19.2 ms                                                                | 23.3 ms: 1.21x slower                                                 |
| richards_super             | 47.7 ms                                                                | 57.8 ms: 1.21x slower                                                 |
| crypto_pyaes               | 68.5 ms                                                                | 83.2 ms: 1.22x slower                                                 |
| spectral_norm              | 86.7 ms                                                                | 106 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 157 us                                                                 | 192 us: 1.22x slower                                                  |
| django_template            | 33.9 ms                                                                | 41.6 ms: 1.23x slower                                                 |
| connected_components       | 389 ms                                                                 | 478 ms: 1.23x slower                                                  |
| shortest_path              | 431 ms                                                                 | 533 ms: 1.24x slower                                                  |
| nbody                      | 91.5 ms                                                                | 114 ms: 1.24x slower                                                  |
| mako                       | 11.7 ms                                                                | 14.8 ms: 1.27x slower                                                 |
| meteor_contest             | 99.6 ms                                                                | 127 ms: 1.27x slower                                                  |
| python_startup_no_site     | 7.45 ms                                                                | 9.58 ms: 1.29x slower                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 3.26 ms: 3.17x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (1): async_tree_none
Ignored benchmarks (1) of results/bm-20250219-3.14.0a5+-08402c0-NOGIL/bm-20250219-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-08402c0.json: html5lib

- Geometric mean (including insignificant results): 1.077x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.21x