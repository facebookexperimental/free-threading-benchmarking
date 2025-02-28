# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 0d98b60
- commit date: 2025-02-27
- overall geometric mean: 1.034x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 296 ms: 1.03x faster                                                  |
| docutils       | 2.80 sec                                                               | 2.75 sec: 1.02x faster                                                |
| html5lib       | 73.7 ms                                                                | 69.3 ms: 1.06x faster                                                 |
| sphinx         | 1.11 sec                                                               | 1.09 sec: 1.02x faster                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 542 ms                                                                 | 488 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 575 ms                                                                 | 521 ms: 1.10x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 298 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 551 ms                                                                 | 537 ms: 1.03x faster                                                  |
| async_tree_io              | 581 ms                                                                 | 569 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 238 ms                                                                 | 233 ms: 1.02x faster                                                  |
| async_tree_memoization     | 337 ms                                                                 | 331 ms: 1.02x faster                                                  |
| async_tree_none            | 275 ms                                                                 | 271 ms: 1.02x faster                                                  |
| async_generators           | 372 ms                                                                 | 369 ms: 1.01x faster                                                  |
| coroutines                 | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 135 ms                                                                 | 121 ms: 1.11x faster                                                  |
| pidigits       | 210 ms                                                                 | 193 ms: 1.08x faster                                                  |
| float          | 76.3 ms                                                                | 70.4 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                | 22.8 ms: 1.07x faster                                                 |
| regex_dna      | 183 ms                                                                 | 172 ms: 1.06x faster                                                  |
| regex_compile  | 157 ms                                                                 | 152 ms: 1.03x faster                                                  |
| regex_effbot   | 2.86 ms                                                                | 2.83 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 251 us                                                                 | 235 us: 1.07x faster                                                  |
| pickle_pure_python   | 367 us                                                                 | 345 us: 1.07x faster                                                  |
| tomli_loads          | 2.36 sec                                                               | 2.27 sec: 1.04x faster                                                |
| json_dumps           | 13.1 ms                                                                | 12.7 ms: 1.03x faster                                                 |
| json_loads           | 29.6 us                                                                | 28.9 us: 1.03x faster                                                 |
| xml_etree_process    | 69.5 ms                                                                | 68.1 ms: 1.02x faster                                                 |
| xml_etree_generate   | 95.4 ms                                                                | 95.1 ms: 1.00x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.64 ms                                                                | 9.61 ms: 1.00x faster                                                 |
| python_startup         | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 27.9 ms                                                                | 26.7 ms: 1.05x faster                                                 |
| django_template | 43.3 ms                                                                | 41.5 ms: 1.05x faster                                                 |
| genshi_xml      | 60.0 ms                                                                | 57.6 ms: 1.04x faster                                                 |
| mako            | 15.9 ms                                                                | 15.6 ms: 1.02x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.04x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-0d98b60 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody                      | 135 ms                                                                 | 121 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 542 ms                                                                 | 488 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 575 ms                                                                 | 521 ms: 1.10x faster                                                  |
| scimark_fft                | 493 ms                                                                 | 450 ms: 1.10x faster                                                  |
| go                         | 141 ms                                                                 | 129 ms: 1.09x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 35.0 us: 1.09x faster                                                 |
| pidigits                   | 210 ms                                                                 | 193 ms: 1.08x faster                                                  |
| float                      | 76.3 ms                                                                | 70.4 ms: 1.08x faster                                                 |
| scimark_monte_carlo        | 95.3 ms                                                                | 88.4 ms: 1.08x faster                                                 |
| scimark_sor                | 144 ms                                                                 | 134 ms: 1.08x faster                                                  |
| unpickle_pure_python       | 251 us                                                                 | 235 us: 1.07x faster                                                  |
| regex_v8                   | 24.4 ms                                                                | 22.8 ms: 1.07x faster                                                 |
| pickle_pure_python         | 367 us                                                                 | 345 us: 1.07x faster                                                  |
| pprint_safe_repr           | 844 ms                                                                 | 792 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.74 sec                                                               | 1.63 sec: 1.07x faster                                                |
| spectral_norm              | 115 ms                                                                 | 108 ms: 1.07x faster                                                  |
| html5lib                   | 73.7 ms                                                                | 69.3 ms: 1.06x faster                                                 |
| regex_dna                  | 183 ms                                                                 | 172 ms: 1.06x faster                                                  |
| raytrace                   | 319 ms                                                                 | 300 ms: 1.06x faster                                                  |
| fannkuch                   | 494 ms                                                                 | 465 ms: 1.06x faster                                                  |
| logging_silent             | 112 ns                                                                 | 106 ns: 1.06x faster                                                  |
| sqlglot_parse              | 1.59 ms                                                                | 1.50 ms: 1.06x faster                                                 |
| sqlglot_transpile          | 1.92 ms                                                                | 1.82 ms: 1.06x faster                                                 |
| pyflate                    | 498 ms                                                                 | 471 ms: 1.06x faster                                                  |
| deepcopy                   | 310 us                                                                 | 294 us: 1.06x faster                                                  |
| chaos                      | 69.3 ms                                                                | 65.8 ms: 1.05x faster                                                 |
| richards_super             | 63.9 ms                                                                | 61.0 ms: 1.05x faster                                                 |
| deltablue                  | 3.78 ms                                                                | 3.61 ms: 1.05x faster                                                 |
| hexiom                     | 7.45 ms                                                                | 7.12 ms: 1.05x faster                                                 |
| genshi_text                | 27.9 ms                                                                | 26.7 ms: 1.05x faster                                                 |
| django_template            | 43.3 ms                                                                | 41.5 ms: 1.05x faster                                                 |
| richards                   | 54.7 ms                                                                | 52.4 ms: 1.04x faster                                                 |
| comprehensions             | 20.0 us                                                                | 19.2 us: 1.04x faster                                                 |
| genshi_xml                 | 60.0 ms                                                                | 57.6 ms: 1.04x faster                                                 |
| logging_format             | 8.32 us                                                                | 7.99 us: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 7.76 ms                                                                | 7.45 ms: 1.04x faster                                                 |
| telco                      | 8.75 ms                                                                | 8.41 ms: 1.04x faster                                                 |
| tomli_loads                | 2.36 sec                                                               | 2.27 sec: 1.04x faster                                                |
| bpe_tokeniser              | 4.80 sec                                                               | 4.63 sec: 1.04x faster                                                |
| json_dumps                 | 13.1 ms                                                                | 12.7 ms: 1.03x faster                                                 |
| 2to3                       | 305 ms                                                                 | 296 ms: 1.03x faster                                                  |
| sqlglot_normalize          | 122 ms                                                                 | 118 ms: 1.03x faster                                                  |
| crypto_pyaes               | 88.0 ms                                                                | 85.4 ms: 1.03x faster                                                 |
| deepcopy_reduce            | 3.17 us                                                                | 3.08 us: 1.03x faster                                                 |
| async_tree_memoization_tg  | 307 ms                                                                 | 298 ms: 1.03x faster                                                  |
| sympy_integrate            | 24.2 ms                                                                | 23.5 ms: 1.03x faster                                                 |
| regex_compile              | 157 ms                                                                 | 152 ms: 1.03x faster                                                  |
| connected_components       | 498 ms                                                                 | 485 ms: 1.03x faster                                                  |
| sqlglot_optimize           | 61.6 ms                                                                | 60.0 ms: 1.03x faster                                                 |
| async_tree_io_tg           | 551 ms                                                                 | 537 ms: 1.03x faster                                                  |
| sympy_str                  | 341 ms                                                                 | 332 ms: 1.03x faster                                                  |
| json_loads                 | 29.6 us                                                                | 28.9 us: 1.03x faster                                                 |
| many_optionals             | 1.17 ms                                                                | 1.15 ms: 1.02x faster                                                 |
| json                       | 5.12 ms                                                                | 5.00 ms: 1.02x faster                                                 |
| mako                       | 15.9 ms                                                                | 15.6 ms: 1.02x faster                                                 |
| shortest_path              | 548 ms                                                                 | 536 ms: 1.02x faster                                                  |
| nqueens                    | 98.1 ms                                                                | 96.0 ms: 1.02x faster                                                 |
| async_tree_io              | 581 ms                                                                 | 569 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 238 ms                                                                 | 233 ms: 1.02x faster                                                  |
| xml_etree_process          | 69.5 ms                                                                | 68.1 ms: 1.02x faster                                                 |
| sphinx                     | 1.11 sec                                                               | 1.09 sec: 1.02x faster                                                |
| scimark_lu                 | 156 ms                                                                 | 153 ms: 1.02x faster                                                  |
| docutils                   | 2.80 sec                                                               | 2.75 sec: 1.02x faster                                                |
| pycparser                  | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                                |
| sympy_sum                  | 188 ms                                                                 | 184 ms: 1.02x faster                                                  |
| thrift                     | 881 us                                                                 | 865 us: 1.02x faster                                                  |
| async_tree_memoization     | 337 ms                                                                 | 331 ms: 1.02x faster                                                  |
| logging_simple             | 7.24 us                                                                | 7.12 us: 1.02x faster                                                 |
| async_tree_none            | 275 ms                                                                 | 271 ms: 1.02x faster                                                  |
| coverage                   | 97.2 ms                                                                | 95.7 ms: 1.02x faster                                                 |
| k_core                     | 2.32 sec                                                               | 2.29 sec: 1.01x faster                                                |
| sympy_expand               | 558 ms                                                                 | 551 ms: 1.01x faster                                                  |
| meteor_contest             | 128 ms                                                                 | 126 ms: 1.01x faster                                                  |
| regex_effbot               | 2.86 ms                                                                | 2.83 ms: 1.01x faster                                                 |
| typing_runtime_protocols   | 199 us                                                                 | 197 us: 1.01x faster                                                  |
| sqlite_synth               | 2.04 us                                                                | 2.02 us: 1.01x faster                                                 |
| bench_thread_pool          | 3.31 ms                                                                | 3.28 ms: 1.01x faster                                                 |
| async_generators           | 372 ms                                                                 | 369 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.30 ms                                                                | 1.29 ms: 1.01x faster                                                 |
| sqlalchemy_declarative     | 156 ms                                                                 | 156 ms: 1.00x faster                                                  |
| xml_etree_generate         | 95.4 ms                                                                | 95.1 ms: 1.00x faster                                                 |
| python_startup_no_site     | 9.64 ms                                                                | 9.61 ms: 1.00x faster                                                 |
| python_startup             | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                 |
| dulwich_log                | 82.6 ms                                                                | 83.1 ms: 1.01x slower                                                 |
| coroutines                 | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                 |
| pathlib                    | 19.4 ms                                                                | 19.6 ms: 1.01x slower                                                 |
| generators                 | 31.3 ms                                                                | 32.7 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (9): sqlalchemy_imperative, pylint, asyncio_websockets, bench_mp_pool, mdp, gc_traversal, subparsers, xml_etree_iterparse, xml_etree_parse

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x