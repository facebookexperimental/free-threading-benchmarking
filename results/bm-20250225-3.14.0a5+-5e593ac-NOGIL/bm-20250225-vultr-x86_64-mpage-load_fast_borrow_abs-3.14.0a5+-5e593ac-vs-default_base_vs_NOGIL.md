# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 5e593ac
- commit date: 2025-02-25
- overall geometric mean: 1.104x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                 | 296 ms: 1.18x slower                                                  |
| docutils       | 2.54 sec                                                               | 2.76 sec: 1.09x slower                                                |
| sphinx         | 971 ms                                                                 | 1.09 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 597 ms                                                                 | 539 ms: 1.11x faster                                                  |
| async_tree_none_tg         | 253 ms                                                                 | 232 ms: 1.09x faster                                                  |
| async_tree_io              | 603 ms                                                                 | 570 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 299 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                                  |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 484 ms: 1.03x slower                                                  |
| async_tree_none            | 258 ms                                                                 | 269 ms: 1.04x slower                                                  |
| async_tree_memoization     | 312 ms                                                                 | 331 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed    | 482 ms                                                                 | 515 ms: 1.07x slower                                                  |
| coroutines                 | 21.4 ms                                                                | 23.5 ms: 1.09x slower                                                 |
| async_generators           | 318 ms                                                                 | 368 ms: 1.16x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 208 ms                                                                 | 191 ms: 1.09x faster                                                  |
| nbody          | 86.9 ms                                                                | 117 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.7 ms                                                                | 24.4 ms: 1.01x faster                                                 |
| regex_effbot   | 2.65 ms                                                                | 2.82 ms: 1.06x slower                                                 |
| regex_dna      | 171 ms                                                                 | 186 ms: 1.09x slower                                                  |
| regex_compile  | 124 ms                                                                 | 151 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.4 ms                                                                | 88.2 ms: 1.03x faster                                                 |
| json_loads           | 28.0 us                                                                | 30.3 us: 1.08x slower                                                 |
| unpickle_pure_python | 211 us                                                                 | 237 us: 1.12x slower                                                  |
| pickle_pure_python   | 307 us                                                                 | 345 us: 1.13x slower                                                  |
| json_dumps           | 11.1 ms                                                                | 12.7 ms: 1.14x slower                                                 |
| xml_etree_generate   | 82.0 ms                                                                | 95.1 ms: 1.16x slower                                                 |
| xml_etree_process    | 57.0 ms                                                                | 68.2 ms: 1.20x slower                                                 |
| tomli_loads          | 1.89 sec                                                               | 2.28 sec: 1.20x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.6 ms: 1.06x slower                                                 |
| python_startup_no_site | 7.51 ms                                                                | 9.62 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 47.7 ms                                                                | 58.3 ms: 1.22x slower                                                 |
| django_template | 32.4 ms                                                                | 41.2 ms: 1.27x slower                                                 |
| genshi_text     | 20.4 ms                                                                | 27.0 ms: 1.32x slower                                                 |
| mako            | 11.6 ms                                                                | 15.5 ms: 1.34x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.21 ms                                                                | 1.71 ms: 2.46x faster                                                 |
| sqlglot_normalize          | 280 ms                                                                 | 118 ms: 2.37x faster                                                  |
| create_gc_cycles           | 1.81 ms                                                                | 1.29 ms: 1.40x faster                                                 |
| async_tree_io_tg           | 597 ms                                                                 | 539 ms: 1.11x faster                                                  |
| async_tree_none_tg         | 253 ms                                                                 | 232 ms: 1.09x faster                                                  |
| pidigits                   | 208 ms                                                                 | 191 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                                | 2.07 us: 1.06x faster                                                 |
| async_tree_io              | 603 ms                                                                 | 570 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 299 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 90.4 ms                                                                | 88.2 ms: 1.03x faster                                                 |
| regex_v8                   | 24.7 ms                                                                | 24.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                                  |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 484 ms: 1.03x slower                                                  |
| pathlib                    | 19.1 ms                                                                | 19.6 ms: 1.03x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.16 sec: 1.04x slower                                                |
| async_tree_none            | 258 ms                                                                 | 269 ms: 1.04x slower                                                  |
| json                       | 4.99 ms                                                                | 5.24 ms: 1.05x slower                                                 |
| mdp                        | 2.42 sec                                                               | 2.55 sec: 1.06x slower                                                |
| python_startup             | 14.7 ms                                                                | 15.6 ms: 1.06x slower                                                 |
| regex_effbot               | 2.65 ms                                                                | 2.82 ms: 1.06x slower                                                 |
| async_tree_memoization     | 312 ms                                                                 | 331 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed    | 482 ms                                                                 | 515 ms: 1.07x slower                                                  |
| bench_mp_pool              | 88.3 ms                                                                | 94.8 ms: 1.07x slower                                                 |
| logging_silent             | 98.4 ns                                                                | 106 ns: 1.08x slower                                                  |
| json_loads                 | 28.0 us                                                                | 30.3 us: 1.08x slower                                                 |
| regex_dna                  | 171 ms                                                                 | 186 ms: 1.09x slower                                                  |
| docutils                   | 2.54 sec                                                               | 2.76 sec: 1.09x slower                                                |
| coroutines                 | 21.4 ms                                                                | 23.5 ms: 1.09x slower                                                 |
| dulwich_log                | 75.0 ms                                                                | 83.0 ms: 1.11x slower                                                 |
| bpe_tokeniser              | 4.15 sec                                                               | 4.62 sec: 1.11x slower                                                |
| k_core                     | 2.03 sec                                                               | 2.26 sec: 1.11x slower                                                |
| scimark_fft                | 309 ms                                                                 | 344 ms: 1.11x slower                                                  |
| unpickle_pure_python       | 211 us                                                                 | 237 us: 1.12x slower                                                  |
| pickle_pure_python         | 307 us                                                                 | 345 us: 1.13x slower                                                  |
| sphinx                     | 971 ms                                                                 | 1.09 sec: 1.13x slower                                                |
| many_optionals             | 1.01 ms                                                                | 1.14 ms: 1.13x slower                                                 |
| json_dumps                 | 11.1 ms                                                                | 12.7 ms: 1.14x slower                                                 |
| scimark_sor                | 112 ms                                                                 | 128 ms: 1.14x slower                                                  |
| pylint                     | 274 ms                                                                 | 314 ms: 1.15x slower                                                  |
| pyflate                    | 402 ms                                                                 | 465 ms: 1.16x slower                                                  |
| async_generators           | 318 ms                                                                 | 368 ms: 1.16x slower                                                  |
| spectral_norm              | 90.5 ms                                                                | 105 ms: 1.16x slower                                                  |
| xml_etree_generate         | 82.0 ms                                                                | 95.1 ms: 1.16x slower                                                 |
| subparsers                 | 21.7 ms                                                                | 25.2 ms: 1.16x slower                                                 |
| go                         | 111 ms                                                                 | 129 ms: 1.16x slower                                                  |
| raytrace                   | 257 ms                                                                 | 299 ms: 1.17x slower                                                  |
| telco                      | 7.19 ms                                                                | 8.44 ms: 1.17x slower                                                 |
| pprint_safe_repr           | 677 ms                                                                 | 798 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.39 sec                                                               | 1.64 sec: 1.18x slower                                                |
| sqlglot_optimize           | 51.0 ms                                                                | 60.2 ms: 1.18x slower                                                 |
| 2to3                       | 250 ms                                                                 | 296 ms: 1.18x slower                                                  |
| deltablue                  | 3.02 ms                                                                | 3.60 ms: 1.19x slower                                                 |
| sqlglot_transpile          | 1.53 ms                                                                | 1.82 ms: 1.19x slower                                                 |
| chaos                      | 54.8 ms                                                                | 65.4 ms: 1.19x slower                                                 |
| xml_etree_process          | 57.0 ms                                                                | 68.2 ms: 1.20x slower                                                 |
| thrift                     | 726 us                                                                 | 870 us: 1.20x slower                                                  |
| tomli_loads                | 1.89 sec                                                               | 2.28 sec: 1.20x slower                                                |
| sympy_expand               | 453 ms                                                                 | 545 ms: 1.20x slower                                                  |
| logging_simple             | 5.82 us                                                                | 7.01 us: 1.20x slower                                                 |
| deepcopy                   | 245 us                                                                 | 295 us: 1.21x slower                                                  |
| logging_format             | 6.63 us                                                                | 8.01 us: 1.21x slower                                                 |
| coverage                   | 79.5 ms                                                                | 96.2 ms: 1.21x slower                                                 |
| regex_compile              | 124 ms                                                                 | 151 ms: 1.21x slower                                                  |
| comprehensions             | 15.9 us                                                                | 19.3 us: 1.21x slower                                                 |
| deepcopy_reduce            | 2.53 us                                                                | 3.07 us: 1.21x slower                                                 |
| scimark_lu                 | 111 ms                                                                 | 134 ms: 1.22x slower                                                  |
| sqlglot_parse              | 1.23 ms                                                                | 1.50 ms: 1.22x slower                                                 |
| genshi_xml                 | 47.7 ms                                                                | 58.3 ms: 1.22x slower                                                 |
| scimark_monte_carlo        | 62.3 ms                                                                | 76.3 ms: 1.22x slower                                                 |
| sympy_integrate            | 19.3 ms                                                                | 23.6 ms: 1.23x slower                                                 |
| generators                 | 26.7 ms                                                                | 32.9 ms: 1.23x slower                                                 |
| sqlalchemy_imperative      | 19.2 ms                                                                | 23.6 ms: 1.23x slower                                                 |
| sympy_sum                  | 151 ms                                                                 | 186 ms: 1.23x slower                                                  |
| sympy_str                  | 267 ms                                                                 | 332 ms: 1.24x slower                                                  |
| deepcopy_memo              | 29.1 us                                                                | 36.1 us: 1.24x slower                                                 |
| sqlalchemy_declarative     | 126 ms                                                                 | 157 ms: 1.24x slower                                                  |
| connected_components       | 388 ms                                                                 | 483 ms: 1.25x slower                                                  |
| shortest_path              | 429 ms                                                                 | 536 ms: 1.25x slower                                                  |
| richards                   | 41.9 ms                                                                | 52.7 ms: 1.26x slower                                                 |
| hexiom                     | 5.67 ms                                                                | 7.14 ms: 1.26x slower                                                 |
| scimark_sparse_mat_mult    | 4.15 ms                                                                | 5.22 ms: 1.26x slower                                                 |
| crypto_pyaes               | 67.0 ms                                                                | 84.4 ms: 1.26x slower                                                 |
| fannkuch                   | 366 ms                                                                 | 464 ms: 1.27x slower                                                  |
| django_template            | 32.4 ms                                                                | 41.2 ms: 1.27x slower                                                 |
| meteor_contest             | 99.2 ms                                                                | 126 ms: 1.27x slower                                                  |
| nqueens                    | 74.7 ms                                                                | 95.3 ms: 1.28x slower                                                 |
| python_startup_no_site     | 7.51 ms                                                                | 9.62 ms: 1.28x slower                                                 |
| typing_runtime_protocols   | 152 us                                                                 | 196 us: 1.29x slower                                                  |
| richards_super             | 47.4 ms                                                                | 61.3 ms: 1.29x slower                                                 |
| genshi_text                | 20.4 ms                                                                | 27.0 ms: 1.32x slower                                                 |
| mako                       | 11.6 ms                                                                | 15.5 ms: 1.34x slower                                                 |
| nbody                      | 86.9 ms                                                                | 117 ms: 1.35x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.29 ms: 3.18x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_parse, float
Ignored benchmarks (1) of results/bm-20250225-3.14.0a5+-5e593ac-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac.json: html5lib

- Geometric mean (including insignificant results): 1.104x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.22x