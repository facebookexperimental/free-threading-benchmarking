# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 48e2f9e
- commit date: 2025-02-25
- overall geometric mean: 1.109x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                 | 296 ms: 1.18x slower                                                  |
| docutils       | 2.54 sec                                                               | 2.78 sec: 1.09x slower                                                |
| sphinx         | 971 ms                                                                 | 1.10 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 597 ms                                                                 | 544 ms: 1.10x faster                                                  |
| async_tree_none_tg         | 253 ms                                                                 | 234 ms: 1.08x faster                                                  |
| async_tree_io              | 603 ms                                                                 | 575 ms: 1.05x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 301 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 485 ms: 1.03x slower                                                  |
| async_tree_none            | 258 ms                                                                 | 270 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed    | 482 ms                                                                 | 518 ms: 1.08x slower                                                  |
| async_tree_memoization     | 312 ms                                                                 | 335 ms: 1.08x slower                                                  |
| coroutines                 | 21.4 ms                                                                | 23.8 ms: 1.11x slower                                                 |
| async_generators           | 318 ms                                                                 | 367 ms: 1.15x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 86.9 ms                                                                | 118 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.7 ms                                                                | 23.9 ms: 1.03x faster                                                 |
| regex_effbot   | 2.65 ms                                                                | 2.73 ms: 1.03x slower                                                 |
| regex_dna      | 171 ms                                                                 | 185 ms: 1.08x slower                                                  |
| regex_compile  | 124 ms                                                                 | 152 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.4 ms                                                                | 88.1 ms: 1.03x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.01x faster                                                  |
| json_loads           | 28.0 us                                                                | 29.8 us: 1.06x slower                                                 |
| pickle_pure_python   | 307 us                                                                 | 345 us: 1.12x slower                                                  |
| unpickle_pure_python | 211 us                                                                 | 238 us: 1.13x slower                                                  |
| json_dumps           | 11.1 ms                                                                | 12.9 ms: 1.16x slower                                                 |
| xml_etree_generate   | 82.0 ms                                                                | 95.4 ms: 1.16x slower                                                 |
| tomli_loads          | 1.89 sec                                                               | 2.27 sec: 1.20x slower                                                |
| xml_etree_process    | 57.0 ms                                                                | 69.1 ms: 1.21x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.6 ms: 1.06x slower                                                 |
| python_startup_no_site | 7.51 ms                                                                | 9.65 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 47.7 ms                                                                | 57.7 ms: 1.21x slower                                                 |
| django_template | 32.4 ms                                                                | 42.3 ms: 1.30x slower                                                 |
| genshi_text     | 20.4 ms                                                                | 26.8 ms: 1.31x slower                                                 |
| mako            | 11.6 ms                                                                | 15.4 ms: 1.33x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.21 ms                                                                | 1.71 ms: 2.47x faster                                                 |
| sqlglot_normalize          | 280 ms                                                                 | 119 ms: 2.35x faster                                                  |
| create_gc_cycles           | 1.81 ms                                                                | 1.29 ms: 1.40x faster                                                 |
| async_tree_io_tg           | 597 ms                                                                 | 544 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.20 us                                                                | 2.03 us: 1.08x faster                                                 |
| async_tree_none_tg         | 253 ms                                                                 | 234 ms: 1.08x faster                                                  |
| async_tree_io              | 603 ms                                                                 | 575 ms: 1.05x faster                                                  |
| regex_v8                   | 24.7 ms                                                                | 23.9 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 90.4 ms                                                                | 88.1 ms: 1.03x faster                                                 |
| async_tree_memoization_tg  | 307 ms                                                                 | 301 ms: 1.02x faster                                                  |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.01x faster                                                  |
| json                       | 4.99 ms                                                                | 5.07 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 485 ms: 1.03x slower                                                  |
| regex_effbot               | 2.65 ms                                                                | 2.73 ms: 1.03x slower                                                 |
| async_tree_none            | 258 ms                                                                 | 270 ms: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.05x slower                                                |
| pathlib                    | 19.1 ms                                                                | 20.1 ms: 1.05x slower                                                 |
| python_startup             | 14.7 ms                                                                | 15.6 ms: 1.06x slower                                                 |
| json_loads                 | 28.0 us                                                                | 29.8 us: 1.06x slower                                                 |
| mdp                        | 2.42 sec                                                               | 2.57 sec: 1.06x slower                                                |
| bench_mp_pool              | 88.3 ms                                                                | 94.8 ms: 1.07x slower                                                 |
| async_tree_cpu_io_mixed    | 482 ms                                                                 | 518 ms: 1.08x slower                                                  |
| async_tree_memoization     | 312 ms                                                                 | 335 ms: 1.08x slower                                                  |
| regex_dna                  | 171 ms                                                                 | 185 ms: 1.08x slower                                                  |
| docutils                   | 2.54 sec                                                               | 2.78 sec: 1.09x slower                                                |
| logging_silent             | 98.4 ns                                                                | 108 ns: 1.10x slower                                                  |
| dulwich_log                | 75.0 ms                                                                | 83.0 ms: 1.11x slower                                                 |
| bpe_tokeniser              | 4.15 sec                                                               | 4.61 sec: 1.11x slower                                                |
| coroutines                 | 21.4 ms                                                                | 23.8 ms: 1.11x slower                                                 |
| k_core                     | 2.03 sec                                                               | 2.27 sec: 1.12x slower                                                |
| pickle_pure_python         | 307 us                                                                 | 345 us: 1.12x slower                                                  |
| unpickle_pure_python       | 211 us                                                                 | 238 us: 1.13x slower                                                  |
| many_optionals             | 1.01 ms                                                                | 1.14 ms: 1.13x slower                                                 |
| sphinx                     | 971 ms                                                                 | 1.10 sec: 1.13x slower                                                |
| pylint                     | 274 ms                                                                 | 314 ms: 1.15x slower                                                  |
| scimark_sor                | 112 ms                                                                 | 129 ms: 1.15x slower                                                  |
| scimark_fft                | 309 ms                                                                 | 356 ms: 1.15x slower                                                  |
| async_generators           | 318 ms                                                                 | 367 ms: 1.15x slower                                                  |
| json_dumps                 | 11.1 ms                                                                | 12.9 ms: 1.16x slower                                                 |
| subparsers                 | 21.7 ms                                                                | 25.2 ms: 1.16x slower                                                 |
| go                         | 111 ms                                                                 | 129 ms: 1.16x slower                                                  |
| xml_etree_generate         | 82.0 ms                                                                | 95.4 ms: 1.16x slower                                                 |
| raytrace                   | 257 ms                                                                 | 303 ms: 1.18x slower                                                  |
| sqlglot_optimize           | 51.0 ms                                                                | 60.2 ms: 1.18x slower                                                 |
| 2to3                       | 250 ms                                                                 | 296 ms: 1.18x slower                                                  |
| pyflate                    | 402 ms                                                                 | 478 ms: 1.19x slower                                                  |
| spectral_norm              | 90.5 ms                                                                | 108 ms: 1.19x slower                                                  |
| sympy_expand               | 453 ms                                                                 | 541 ms: 1.19x slower                                                  |
| tomli_loads                | 1.89 sec                                                               | 2.27 sec: 1.20x slower                                                |
| deltablue                  | 3.02 ms                                                                | 3.62 ms: 1.20x slower                                                 |
| sqlglot_transpile          | 1.53 ms                                                                | 1.84 ms: 1.20x slower                                                 |
| pprint_safe_repr           | 677 ms                                                                 | 816 ms: 1.21x slower                                                  |
| comprehensions             | 15.9 us                                                                | 19.2 us: 1.21x slower                                                 |
| chaos                      | 54.8 ms                                                                | 66.2 ms: 1.21x slower                                                 |
| genshi_xml                 | 47.7 ms                                                                | 57.7 ms: 1.21x slower                                                 |
| coverage                   | 79.5 ms                                                                | 96.2 ms: 1.21x slower                                                 |
| xml_etree_process          | 57.0 ms                                                                | 69.1 ms: 1.21x slower                                                 |
| pprint_pformat             | 1.39 sec                                                               | 1.68 sec: 1.21x slower                                                |
| thrift                     | 726 us                                                                 | 879 us: 1.21x slower                                                  |
| scimark_monte_carlo        | 62.3 ms                                                                | 76.0 ms: 1.22x slower                                                 |
| telco                      | 7.19 ms                                                                | 8.77 ms: 1.22x slower                                                 |
| regex_compile              | 124 ms                                                                 | 152 ms: 1.22x slower                                                  |
| sympy_integrate            | 19.3 ms                                                                | 23.6 ms: 1.23x slower                                                 |
| generators                 | 26.7 ms                                                                | 32.8 ms: 1.23x slower                                                 |
| sqlalchemy_imperative      | 19.2 ms                                                                | 23.6 ms: 1.23x slower                                                 |
| logging_format             | 6.63 us                                                                | 8.17 us: 1.23x slower                                                 |
| sympy_sum                  | 151 ms                                                                 | 186 ms: 1.23x slower                                                  |
| sympy_str                  | 267 ms                                                                 | 330 ms: 1.23x slower                                                  |
| sqlglot_parse              | 1.23 ms                                                                | 1.52 ms: 1.23x slower                                                 |
| logging_simple             | 5.82 us                                                                | 7.19 us: 1.24x slower                                                 |
| scimark_lu                 | 111 ms                                                                 | 137 ms: 1.24x slower                                                  |
| deepcopy_memo              | 29.1 us                                                                | 36.1 us: 1.24x slower                                                 |
| deepcopy                   | 245 us                                                                 | 304 us: 1.24x slower                                                  |
| scimark_sparse_mat_mult    | 4.15 ms                                                                | 5.16 ms: 1.24x slower                                                 |
| sqlalchemy_declarative     | 126 ms                                                                 | 157 ms: 1.25x slower                                                  |
| richards                   | 41.9 ms                                                                | 52.3 ms: 1.25x slower                                                 |
| connected_components       | 388 ms                                                                 | 484 ms: 1.25x slower                                                  |
| shortest_path              | 429 ms                                                                 | 536 ms: 1.25x slower                                                  |
| deepcopy_reduce            | 2.53 us                                                                | 3.17 us: 1.25x slower                                                 |
| nqueens                    | 74.7 ms                                                                | 94.2 ms: 1.26x slower                                                 |
| hexiom                     | 5.67 ms                                                                | 7.18 ms: 1.26x slower                                                 |
| crypto_pyaes               | 67.0 ms                                                                | 84.8 ms: 1.27x slower                                                 |
| fannkuch                   | 366 ms                                                                 | 465 ms: 1.27x slower                                                  |
| python_startup_no_site     | 7.51 ms                                                                | 9.65 ms: 1.29x slower                                                 |
| richards_super             | 47.4 ms                                                                | 61.1 ms: 1.29x slower                                                 |
| meteor_contest             | 99.2 ms                                                                | 128 ms: 1.29x slower                                                  |
| django_template            | 32.4 ms                                                                | 42.3 ms: 1.30x slower                                                 |
| typing_runtime_protocols   | 152 us                                                                 | 199 us: 1.31x slower                                                  |
| genshi_text                | 20.4 ms                                                                | 26.8 ms: 1.31x slower                                                 |
| mako                       | 11.6 ms                                                                | 15.4 ms: 1.33x slower                                                 |
| nbody                      | 86.9 ms                                                                | 118 ms: 1.35x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.29 ms: 3.18x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                          |

Benchmark hidden because not significant (3): float, pidigits, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250225-3.14.0a5+-48e2f9e-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e.json: html5lib

- Geometric mean (including insignificant results): 1.109x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.20x