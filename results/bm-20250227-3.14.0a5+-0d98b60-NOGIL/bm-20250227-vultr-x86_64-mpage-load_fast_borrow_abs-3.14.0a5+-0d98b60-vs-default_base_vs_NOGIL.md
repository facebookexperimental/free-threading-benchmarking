# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 0d98b60
- commit date: 2025-02-27
- overall geometric mean: 1.121x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 296 ms: 1.19x slower                                                  |
| docutils       | 2.53 sec                                                               | 2.75 sec: 1.09x slower                                                |
| sphinx         | 967 ms                                                                 | 1.09 sec: 1.12x slower                                                |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 602 ms                                                                 | 537 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 251 ms                                                                 | 233 ms: 1.08x faster                                                  |
| async_tree_io              | 604 ms                                                                 | 569 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 298 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 488 ms: 1.03x slower                                                  |
| async_tree_none            | 257 ms                                                                 | 271 ms: 1.05x slower                                                  |
| async_tree_memoization     | 312 ms                                                                 | 331 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed    | 484 ms                                                                 | 521 ms: 1.08x slower                                                  |
| coroutines                 | 21.1 ms                                                                | 23.4 ms: 1.11x slower                                                 |
| async_generators           | 322 ms                                                                 | 369 ms: 1.15x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 198 ms                                                                 | 193 ms: 1.02x faster                                                  |
| float          | 71.5 ms                                                                | 70.4 ms: 1.02x faster                                                 |
| nbody          | 87.3 ms                                                                | 121 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 25.2 ms                                                                | 22.8 ms: 1.10x faster                                                 |
| regex_dna      | 176 ms                                                                 | 172 ms: 1.02x faster                                                  |
| regex_effbot   | 2.86 ms                                                                | 2.83 ms: 1.01x faster                                                 |
| regex_compile  | 123 ms                                                                 | 152 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.0 ms                                                                | 87.9 ms: 1.02x faster                                                 |
| json_loads           | 28.0 us                                                                | 28.9 us: 1.03x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 235 us: 1.13x slower                                                  |
| json_dumps           | 11.1 ms                                                                | 12.7 ms: 1.14x slower                                                 |
| pickle_pure_python   | 303 us                                                                 | 345 us: 1.14x slower                                                  |
| xml_etree_generate   | 82.8 ms                                                                | 95.1 ms: 1.15x slower                                                 |
| xml_etree_process    | 57.3 ms                                                                | 68.1 ms: 1.19x slower                                                 |
| tomli_loads          | 1.88 sec                                                               | 2.27 sec: 1.21x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.6 ms: 1.06x slower                                                 |
| python_startup_no_site | 7.51 ms                                                                | 9.61 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 47.4 ms                                                                | 57.6 ms: 1.21x slower                                                 |
| django_template | 32.9 ms                                                                | 41.5 ms: 1.26x slower                                                 |
| genshi_text     | 20.4 ms                                                                | 26.7 ms: 1.31x slower                                                 |
| mako            | 11.5 ms                                                                | 15.6 ms: 1.35x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.46 ms                                                                | 1.71 ms: 2.61x faster                                                 |
| create_gc_cycles           | 1.83 ms                                                                | 1.29 ms: 1.42x faster                                                 |
| async_tree_io_tg           | 602 ms                                                                 | 537 ms: 1.12x faster                                                  |
| regex_v8                   | 25.2 ms                                                                | 22.8 ms: 1.10x faster                                                 |
| sqlite_synth               | 2.19 us                                                                | 2.02 us: 1.08x faster                                                 |
| async_tree_none_tg         | 251 ms                                                                 | 233 ms: 1.08x faster                                                  |
| async_tree_io              | 604 ms                                                                 | 569 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 298 ms: 1.03x faster                                                  |
| regex_dna                  | 176 ms                                                                 | 172 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 90.0 ms                                                                | 87.9 ms: 1.02x faster                                                 |
| pidigits                   | 198 ms                                                                 | 193 ms: 1.02x faster                                                  |
| float                      | 71.5 ms                                                                | 70.4 ms: 1.02x faster                                                 |
| regex_effbot               | 2.86 ms                                                                | 2.83 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| json                       | 4.92 ms                                                                | 5.00 ms: 1.02x slower                                                 |
| logging_silent             | 103 ns                                                                 | 106 ns: 1.03x slower                                                  |
| json_loads                 | 28.0 us                                                                | 28.9 us: 1.03x slower                                                 |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 488 ms: 1.03x slower                                                  |
| pathlib                    | 18.8 ms                                                                | 19.6 ms: 1.05x slower                                                 |
| pycparser                  | 1.11 sec                                                               | 1.17 sec: 1.05x slower                                                |
| async_tree_none            | 257 ms                                                                 | 271 ms: 1.05x slower                                                  |
| python_startup             | 14.7 ms                                                                | 15.6 ms: 1.06x slower                                                 |
| async_tree_memoization     | 312 ms                                                                 | 331 ms: 1.06x slower                                                  |
| bench_mp_pool              | 88.1 ms                                                                | 94.7 ms: 1.07x slower                                                 |
| async_tree_cpu_io_mixed    | 484 ms                                                                 | 521 ms: 1.08x slower                                                  |
| docutils                   | 2.53 sec                                                               | 2.75 sec: 1.09x slower                                                |
| coroutines                 | 21.1 ms                                                                | 23.4 ms: 1.11x slower                                                 |
| dulwich_log                | 74.7 ms                                                                | 83.1 ms: 1.11x slower                                                 |
| bpe_tokeniser              | 4.13 sec                                                               | 4.63 sec: 1.12x slower                                                |
| sphinx                     | 967 ms                                                                 | 1.09 sec: 1.12x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 235 us: 1.13x slower                                                  |
| json_dumps                 | 11.1 ms                                                                | 12.7 ms: 1.14x slower                                                 |
| k_core                     | 2.01 sec                                                               | 2.29 sec: 1.14x slower                                                |
| pickle_pure_python         | 303 us                                                                 | 345 us: 1.14x slower                                                  |
| many_optionals             | 1.00 ms                                                                | 1.15 ms: 1.14x slower                                                 |
| pylint                     | 273 ms                                                                 | 313 ms: 1.14x slower                                                  |
| async_generators           | 322 ms                                                                 | 369 ms: 1.15x slower                                                  |
| xml_etree_generate         | 82.8 ms                                                                | 95.1 ms: 1.15x slower                                                 |
| pprint_safe_repr           | 681 ms                                                                 | 792 ms: 1.16x slower                                                  |
| mdp                        | 2.29 sec                                                               | 2.67 sec: 1.17x slower                                                |
| subparsers                 | 21.7 ms                                                                | 25.3 ms: 1.17x slower                                                 |
| pyflate                    | 403 ms                                                                 | 471 ms: 1.17x slower                                                  |
| go                         | 110 ms                                                                 | 129 ms: 1.17x slower                                                  |
| telco                      | 7.15 ms                                                                | 8.41 ms: 1.18x slower                                                 |
| sqlglot_transpile          | 1.54 ms                                                                | 1.82 ms: 1.18x slower                                                 |
| pprint_pformat             | 1.38 sec                                                               | 1.63 sec: 1.18x slower                                                |
| sqlglot_optimize           | 50.7 ms                                                                | 60.0 ms: 1.18x slower                                                 |
| sqlglot_normalize          | 99.8 ms                                                                | 118 ms: 1.19x slower                                                  |
| raytrace                   | 253 ms                                                                 | 300 ms: 1.19x slower                                                  |
| xml_etree_process          | 57.3 ms                                                                | 68.1 ms: 1.19x slower                                                 |
| 2to3                       | 249 ms                                                                 | 296 ms: 1.19x slower                                                  |
| spectral_norm              | 90.6 ms                                                                | 108 ms: 1.19x slower                                                  |
| deltablue                  | 3.02 ms                                                                | 3.61 ms: 1.19x slower                                                 |
| scimark_sor                | 112 ms                                                                 | 134 ms: 1.20x slower                                                  |
| deepcopy_memo              | 29.2 us                                                                | 35.0 us: 1.20x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                                | 1.50 ms: 1.20x slower                                                 |
| coverage                   | 79.5 ms                                                                | 95.7 ms: 1.20x slower                                                 |
| comprehensions             | 16.0 us                                                                | 19.2 us: 1.20x slower                                                 |
| logging_simple             | 5.91 us                                                                | 7.12 us: 1.20x slower                                                 |
| deepcopy                   | 244 us                                                                 | 294 us: 1.20x slower                                                  |
| chaos                      | 54.5 ms                                                                | 65.8 ms: 1.21x slower                                                 |
| thrift                     | 715 us                                                                 | 865 us: 1.21x slower                                                  |
| tomli_loads                | 1.88 sec                                                               | 2.27 sec: 1.21x slower                                                |
| logging_format             | 6.60 us                                                                | 7.99 us: 1.21x slower                                                 |
| genshi_xml                 | 47.4 ms                                                                | 57.6 ms: 1.21x slower                                                 |
| sympy_integrate            | 19.3 ms                                                                | 23.5 ms: 1.22x slower                                                 |
| deepcopy_reduce            | 2.53 us                                                                | 3.08 us: 1.22x slower                                                 |
| generators                 | 26.8 ms                                                                | 32.7 ms: 1.22x slower                                                 |
| sympy_expand               | 450 ms                                                                 | 551 ms: 1.22x slower                                                  |
| sympy_sum                  | 150 ms                                                                 | 184 ms: 1.23x slower                                                  |
| sqlalchemy_imperative      | 19.0 ms                                                                | 23.5 ms: 1.23x slower                                                 |
| regex_compile              | 123 ms                                                                 | 152 ms: 1.24x slower                                                  |
| sqlalchemy_declarative     | 126 ms                                                                 | 156 ms: 1.24x slower                                                  |
| sympy_str                  | 267 ms                                                                 | 332 ms: 1.24x slower                                                  |
| hexiom                     | 5.70 ms                                                                | 7.12 ms: 1.25x slower                                                 |
| richards                   | 41.9 ms                                                                | 52.4 ms: 1.25x slower                                                 |
| shortest_path              | 427 ms                                                                 | 536 ms: 1.25x slower                                                  |
| connected_components       | 386 ms                                                                 | 485 ms: 1.25x slower                                                  |
| django_template            | 32.9 ms                                                                | 41.5 ms: 1.26x slower                                                 |
| richards_super             | 47.9 ms                                                                | 61.0 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.51 ms                                                                | 9.61 ms: 1.28x slower                                                 |
| nqueens                    | 74.9 ms                                                                | 96.0 ms: 1.28x slower                                                 |
| fannkuch                   | 363 ms                                                                 | 465 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 153 us                                                                 | 197 us: 1.29x slower                                                  |
| crypto_pyaes               | 66.2 ms                                                                | 85.4 ms: 1.29x slower                                                 |
| meteor_contest             | 97.1 ms                                                                | 126 ms: 1.30x slower                                                  |
| genshi_text                | 20.4 ms                                                                | 26.7 ms: 1.31x slower                                                 |
| mako                       | 11.5 ms                                                                | 15.6 ms: 1.35x slower                                                 |
| scimark_fft                | 331 ms                                                                 | 450 ms: 1.36x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 153 ms: 1.37x slower                                                  |
| nbody                      | 87.3 ms                                                                | 121 ms: 1.39x slower                                                  |
| scimark_monte_carlo        | 63.4 ms                                                                | 88.4 ms: 1.39x slower                                                 |
| scimark_sparse_mat_mult    | 4.26 ms                                                                | 7.45 ms: 1.75x slower                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 3.28 ms: 3.19x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.15x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse
Ignored benchmarks (1) of results/bm-20250227-3.14.0a5+-0d98b60-NOGIL/bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60.json: html5lib

- Geometric mean (including insignificant results): 1.121x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.21x