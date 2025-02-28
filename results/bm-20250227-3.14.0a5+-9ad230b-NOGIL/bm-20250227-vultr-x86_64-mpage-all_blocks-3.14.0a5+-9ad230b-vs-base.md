# Results vs. base

- fork: mpage
- ref: all_blocks
- machine: linux-x86_64
- commit hash: 9ad230b
- commit date: 2025-02-27
- overall geometric mean: 1.028x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 296 ms: 1.03x faster                                        |
| docutils       | 2.80 sec                                                               | 2.77 sec: 1.01x faster                                      |
| html5lib       | 73.7 ms                                                                | 68.9 ms: 1.07x faster                                       |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 551 ms                                                                 | 532 ms: 1.03x faster                                        |
| async_tree_io              | 581 ms                                                                 | 563 ms: 1.03x faster                                        |
| async_tree_memoization_tg  | 307 ms                                                                 | 297 ms: 1.03x faster                                        |
| async_tree_none_tg         | 238 ms                                                                 | 231 ms: 1.03x faster                                        |
| async_tree_cpu_io_mixed    | 575 ms                                                                 | 562 ms: 1.02x faster                                        |
| async_tree_cpu_io_mixed_tg | 542 ms                                                                 | 530 ms: 1.02x faster                                        |
| async_tree_memoization     | 337 ms                                                                 | 330 ms: 1.02x faster                                        |
| async_tree_none            | 275 ms                                                                 | 270 ms: 1.02x faster                                        |
| async_generators           | 372 ms                                                                 | 374 ms: 1.00x slower                                        |
| coroutines                 | 23.2 ms                                                                | 24.1 ms: 1.04x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 135 ms                                                                 | 120 ms: 1.12x faster                                        |
| float          | 76.3 ms                                                                | 70.7 ms: 1.08x faster                                       |
| pidigits       | 210 ms                                                                 | 216 ms: 1.03x slower                                        |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 2.86 ms                                                                | 2.74 ms: 1.04x faster                                       |
| regex_compile  | 157 ms                                                                 | 151 ms: 1.04x faster                                        |
| regex_v8       | 24.4 ms                                                                | 23.7 ms: 1.03x faster                                       |
| regex_dna      | 183 ms                                                                 | 183 ms: 1.00x slower                                        |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| pickle_pure_python   | 367 us                                                                 | 342 us: 1.07x faster                                        |
| tomli_loads          | 2.36 sec                                                               | 2.20 sec: 1.07x faster                                      |
| unpickle_pure_python | 251 us                                                                 | 236 us: 1.06x faster                                        |
| json_dumps           | 13.1 ms                                                                | 12.6 ms: 1.04x faster                                       |
| xml_etree_parse      | 128 ms                                                                 | 127 ms: 1.01x faster                                        |
| xml_etree_generate   | 95.4 ms                                                                | 95.7 ms: 1.00x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                |

Benchmark hidden because not significant (3): xml_etree_process, json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup | 15.6 ms                                                                | 15.6 ms: 1.00x slower                                       |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_text     | 27.9 ms                                                                | 26.5 ms: 1.05x faster                                       |
| genshi_xml      | 60.0 ms                                                                | 57.8 ms: 1.04x faster                                       |
| django_template | 43.3 ms                                                                | 42.1 ms: 1.03x faster                                       |
| mako            | 15.9 ms                                                                | 15.6 ms: 1.02x faster                                       |
| Geometric mean  | (ref)                                                                  | 1.04x faster                                                |

All benchmarks:
===============

| Benchmark                  | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody                      | 135 ms                                                                 | 120 ms: 1.12x faster                                        |
| go                         | 141 ms                                                                 | 129 ms: 1.09x faster                                        |
| scimark_fft                | 493 ms                                                                 | 454 ms: 1.09x faster                                        |
| float                      | 76.3 ms                                                                | 70.7 ms: 1.08x faster                                       |
| deepcopy_memo              | 38.1 us                                                                | 35.3 us: 1.08x faster                                       |
| pickle_pure_python         | 367 us                                                                 | 342 us: 1.07x faster                                        |
| tomli_loads                | 2.36 sec                                                               | 2.20 sec: 1.07x faster                                      |
| html5lib                   | 73.7 ms                                                                | 68.9 ms: 1.07x faster                                       |
| scimark_monte_carlo        | 95.3 ms                                                                | 89.1 ms: 1.07x faster                                       |
| sqlglot_parse              | 1.59 ms                                                                | 1.49 ms: 1.07x faster                                       |
| pprint_pformat             | 1.74 sec                                                               | 1.63 sec: 1.06x faster                                      |
| unpickle_pure_python       | 251 us                                                                 | 236 us: 1.06x faster                                        |
| pprint_safe_repr           | 844 ms                                                                 | 793 ms: 1.06x faster                                        |
| spectral_norm              | 115 ms                                                                 | 108 ms: 1.06x faster                                        |
| raytrace                   | 319 ms                                                                 | 300 ms: 1.06x faster                                        |
| scimark_sor                | 144 ms                                                                 | 136 ms: 1.06x faster                                        |
| sqlglot_transpile          | 1.92 ms                                                                | 1.81 ms: 1.06x faster                                       |
| logging_silent             | 112 ns                                                                 | 106 ns: 1.06x faster                                        |
| deepcopy                   | 310 us                                                                 | 294 us: 1.06x faster                                        |
| genshi_text                | 27.9 ms                                                                | 26.5 ms: 1.05x faster                                       |
| scimark_sparse_mat_mult    | 7.76 ms                                                                | 7.38 ms: 1.05x faster                                       |
| chaos                      | 69.3 ms                                                                | 66.1 ms: 1.05x faster                                       |
| fannkuch                   | 494 ms                                                                 | 471 ms: 1.05x faster                                        |
| deepcopy_reduce            | 3.17 us                                                                | 3.03 us: 1.05x faster                                       |
| richards_super             | 63.9 ms                                                                | 61.1 ms: 1.05x faster                                       |
| deltablue                  | 3.78 ms                                                                | 3.62 ms: 1.05x faster                                       |
| mdp                        | 2.68 sec                                                               | 2.57 sec: 1.04x faster                                      |
| regex_effbot               | 2.86 ms                                                                | 2.74 ms: 1.04x faster                                       |
| pyflate                    | 498 ms                                                                 | 478 ms: 1.04x faster                                        |
| hexiom                     | 7.45 ms                                                                | 7.15 ms: 1.04x faster                                       |
| richards                   | 54.7 ms                                                                | 52.6 ms: 1.04x faster                                       |
| regex_compile              | 157 ms                                                                 | 151 ms: 1.04x faster                                        |
| bpe_tokeniser              | 4.80 sec                                                               | 4.62 sec: 1.04x faster                                      |
| genshi_xml                 | 60.0 ms                                                                | 57.8 ms: 1.04x faster                                       |
| crypto_pyaes               | 88.0 ms                                                                | 84.9 ms: 1.04x faster                                       |
| comprehensions             | 20.0 us                                                                | 19.4 us: 1.04x faster                                       |
| nqueens                    | 98.1 ms                                                                | 94.7 ms: 1.04x faster                                       |
| json_dumps                 | 13.1 ms                                                                | 12.6 ms: 1.04x faster                                       |
| async_tree_io_tg           | 551 ms                                                                 | 532 ms: 1.03x faster                                        |
| async_tree_io              | 581 ms                                                                 | 563 ms: 1.03x faster                                        |
| async_tree_memoization_tg  | 307 ms                                                                 | 297 ms: 1.03x faster                                        |
| async_tree_none_tg         | 238 ms                                                                 | 231 ms: 1.03x faster                                        |
| 2to3                       | 305 ms                                                                 | 296 ms: 1.03x faster                                        |
| sympy_str                  | 341 ms                                                                 | 331 ms: 1.03x faster                                        |
| django_template            | 43.3 ms                                                                | 42.1 ms: 1.03x faster                                       |
| regex_v8                   | 24.4 ms                                                                | 23.7 ms: 1.03x faster                                       |
| sqlglot_normalize          | 122 ms                                                                 | 119 ms: 1.03x faster                                        |
| many_optionals             | 1.17 ms                                                                | 1.14 ms: 1.03x faster                                       |
| sympy_integrate            | 24.2 ms                                                                | 23.6 ms: 1.03x faster                                       |
| sympy_expand               | 558 ms                                                                 | 545 ms: 1.02x faster                                        |
| k_core                     | 2.32 sec                                                               | 2.27 sec: 1.02x faster                                      |
| async_tree_cpu_io_mixed    | 575 ms                                                                 | 562 ms: 1.02x faster                                        |
| mako                       | 15.9 ms                                                                | 15.6 ms: 1.02x faster                                       |
| async_tree_cpu_io_mixed_tg | 542 ms                                                                 | 530 ms: 1.02x faster                                        |
| async_tree_memoization     | 337 ms                                                                 | 330 ms: 1.02x faster                                        |
| sqlglot_optimize           | 61.6 ms                                                                | 60.3 ms: 1.02x faster                                       |
| scimark_lu                 | 156 ms                                                                 | 153 ms: 1.02x faster                                        |
| connected_components       | 498 ms                                                                 | 488 ms: 1.02x faster                                        |
| async_tree_none            | 275 ms                                                                 | 270 ms: 1.02x faster                                        |
| meteor_contest             | 128 ms                                                                 | 125 ms: 1.02x faster                                        |
| telco                      | 8.75 ms                                                                | 8.60 ms: 1.02x faster                                       |
| shortest_path              | 548 ms                                                                 | 539 ms: 1.02x faster                                        |
| logging_format             | 8.32 us                                                                | 8.19 us: 1.02x faster                                       |
| pycparser                  | 1.19 sec                                                               | 1.17 sec: 1.01x faster                                      |
| docutils                   | 2.80 sec                                                               | 2.77 sec: 1.01x faster                                      |
| bench_thread_pool          | 3.31 ms                                                                | 3.27 ms: 1.01x faster                                       |
| json                       | 5.12 ms                                                                | 5.06 ms: 1.01x faster                                       |
| typing_runtime_protocols   | 199 us                                                                 | 196 us: 1.01x faster                                        |
| sympy_sum                  | 188 ms                                                                 | 185 ms: 1.01x faster                                        |
| logging_simple             | 7.24 us                                                                | 7.16 us: 1.01x faster                                       |
| thrift                     | 881 us                                                                 | 872 us: 1.01x faster                                        |
| xml_etree_parse            | 128 ms                                                                 | 127 ms: 1.01x faster                                        |
| coverage                   | 97.2 ms                                                                | 96.5 ms: 1.01x faster                                       |
| dulwich_log                | 82.6 ms                                                                | 82.1 ms: 1.01x faster                                       |
| python_startup             | 15.6 ms                                                                | 15.6 ms: 1.00x slower                                       |
| xml_etree_generate         | 95.4 ms                                                                | 95.7 ms: 1.00x slower                                       |
| async_generators           | 372 ms                                                                 | 374 ms: 1.00x slower                                        |
| regex_dna                  | 183 ms                                                                 | 183 ms: 1.00x slower                                        |
| pidigits                   | 210 ms                                                                 | 216 ms: 1.03x slower                                        |
| coroutines                 | 23.2 ms                                                                | 24.1 ms: 1.04x slower                                       |
| generators                 | 31.3 ms                                                                | 33.0 ms: 1.05x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                |

Benchmark hidden because not significant (15): sphinx, gc_traversal, asyncio_websockets, create_gc_cycles, sqlite_synth, python_startup_no_site, pylint, xml_etree_process, subparsers, json_loads, pathlib, sqlalchemy_declarative, bench_mp_pool, xml_etree_iterparse, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.00x