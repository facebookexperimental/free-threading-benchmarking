# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: all_blocks
- machine: linux-x86_64
- commit hash: 9ad230b
- commit date: 2025-02-27
- overall geometric mean: 1.126x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 296 ms: 1.19x slower                                        |
| docutils       | 2.53 sec                                                               | 2.77 sec: 1.10x slower                                      |
| sphinx         | 967 ms                                                                 | 1.10 sec: 1.14x slower                                      |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 602 ms                                                                 | 532 ms: 1.13x faster                                        |
| async_tree_none_tg         | 251 ms                                                                 | 231 ms: 1.09x faster                                        |
| async_tree_io              | 604 ms                                                                 | 563 ms: 1.07x faster                                        |
| async_tree_memoization_tg  | 307 ms                                                                 | 297 ms: 1.03x faster                                        |
| async_tree_none            | 257 ms                                                                 | 270 ms: 1.05x slower                                        |
| async_tree_memoization     | 312 ms                                                                 | 330 ms: 1.06x slower                                        |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 530 ms: 1.12x slower                                        |
| coroutines                 | 21.1 ms                                                                | 24.1 ms: 1.14x slower                                       |
| async_tree_cpu_io_mixed    | 484 ms                                                                 | 562 ms: 1.16x slower                                        |
| async_generators           | 322 ms                                                                 | 374 ms: 1.16x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 71.5 ms                                                                | 70.7 ms: 1.01x faster                                       |
| pidigits       | 198 ms                                                                 | 216 ms: 1.09x slower                                        |
| nbody          | 87.3 ms                                                                | 120 ms: 1.38x slower                                        |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_v8       | 25.2 ms                                                                | 23.7 ms: 1.06x faster                                       |
| regex_effbot   | 2.86 ms                                                                | 2.74 ms: 1.04x faster                                       |
| regex_dna      | 176 ms                                                                 | 183 ms: 1.04x slower                                        |
| regex_compile  | 123 ms                                                                 | 151 ms: 1.22x slower                                        |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 90.0 ms                                                                | 88.1 ms: 1.02x faster                                       |
| xml_etree_parse      | 128 ms                                                                 | 127 ms: 1.01x faster                                        |
| json_loads           | 28.0 us                                                                | 29.6 us: 1.06x slower                                       |
| pickle_pure_python   | 303 us                                                                 | 342 us: 1.13x slower                                        |
| json_dumps           | 11.1 ms                                                                | 12.6 ms: 1.13x slower                                       |
| unpickle_pure_python | 208 us                                                                 | 236 us: 1.14x slower                                        |
| xml_etree_generate   | 82.8 ms                                                                | 95.7 ms: 1.16x slower                                       |
| tomli_loads          | 1.88 sec                                                               | 2.20 sec: 1.17x slower                                      |
| xml_etree_process    | 57.3 ms                                                                | 69.5 ms: 1.21x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.6 ms: 1.06x slower                                       |
| python_startup_no_site | 7.51 ms                                                                | 9.64 ms: 1.28x slower                                       |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 47.4 ms                                                                | 57.8 ms: 1.22x slower                                       |
| django_template | 32.9 ms                                                                | 42.1 ms: 1.28x slower                                       |
| genshi_text     | 20.4 ms                                                                | 26.5 ms: 1.30x slower                                       |
| mako            | 11.5 ms                                                                | 15.6 ms: 1.35x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d | bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| gc_traversal               | 4.46 ms                                                                | 1.71 ms: 2.61x faster                                       |
| create_gc_cycles           | 1.83 ms                                                                | 1.30 ms: 1.41x faster                                       |
| async_tree_io_tg           | 602 ms                                                                 | 532 ms: 1.13x faster                                        |
| async_tree_none_tg         | 251 ms                                                                 | 231 ms: 1.09x faster                                        |
| async_tree_io              | 604 ms                                                                 | 563 ms: 1.07x faster                                        |
| sqlite_synth               | 2.19 us                                                                | 2.04 us: 1.07x faster                                       |
| regex_v8                   | 25.2 ms                                                                | 23.7 ms: 1.06x faster                                       |
| regex_effbot               | 2.86 ms                                                                | 2.74 ms: 1.04x faster                                       |
| async_tree_memoization_tg  | 307 ms                                                                 | 297 ms: 1.03x faster                                        |
| xml_etree_iterparse        | 90.0 ms                                                                | 88.1 ms: 1.02x faster                                       |
| float                      | 71.5 ms                                                                | 70.7 ms: 1.01x faster                                       |
| xml_etree_parse            | 128 ms                                                                 | 127 ms: 1.01x faster                                        |
| json                       | 4.92 ms                                                                | 5.06 ms: 1.03x slower                                       |
| logging_silent             | 103 ns                                                                 | 106 ns: 1.03x slower                                        |
| pathlib                    | 18.8 ms                                                                | 19.5 ms: 1.04x slower                                       |
| regex_dna                  | 176 ms                                                                 | 183 ms: 1.04x slower                                        |
| async_tree_none            | 257 ms                                                                 | 270 ms: 1.05x slower                                        |
| pycparser                  | 1.11 sec                                                               | 1.17 sec: 1.06x slower                                      |
| json_loads                 | 28.0 us                                                                | 29.6 us: 1.06x slower                                       |
| async_tree_memoization     | 312 ms                                                                 | 330 ms: 1.06x slower                                        |
| python_startup             | 14.7 ms                                                                | 15.6 ms: 1.06x slower                                       |
| bench_mp_pool              | 88.1 ms                                                                | 95.3 ms: 1.08x slower                                       |
| pidigits                   | 198 ms                                                                 | 216 ms: 1.09x slower                                        |
| docutils                   | 2.53 sec                                                               | 2.77 sec: 1.10x slower                                      |
| dulwich_log                | 74.7 ms                                                                | 82.1 ms: 1.10x slower                                       |
| bpe_tokeniser              | 4.13 sec                                                               | 4.62 sec: 1.12x slower                                      |
| mdp                        | 2.29 sec                                                               | 2.57 sec: 1.12x slower                                      |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 530 ms: 1.12x slower                                        |
| k_core                     | 2.01 sec                                                               | 2.27 sec: 1.13x slower                                      |
| pickle_pure_python         | 303 us                                                                 | 342 us: 1.13x slower                                        |
| json_dumps                 | 11.1 ms                                                                | 12.6 ms: 1.13x slower                                       |
| unpickle_pure_python       | 208 us                                                                 | 236 us: 1.14x slower                                        |
| sphinx                     | 967 ms                                                                 | 1.10 sec: 1.14x slower                                      |
| coroutines                 | 21.1 ms                                                                | 24.1 ms: 1.14x slower                                       |
| many_optionals             | 1.00 ms                                                                | 1.14 ms: 1.14x slower                                       |
| pylint                     | 273 ms                                                                 | 315 ms: 1.15x slower                                        |
| xml_etree_generate         | 82.8 ms                                                                | 95.7 ms: 1.16x slower                                       |
| async_tree_cpu_io_mixed    | 484 ms                                                                 | 562 ms: 1.16x slower                                        |
| async_generators           | 322 ms                                                                 | 374 ms: 1.16x slower                                        |
| pprint_safe_repr           | 681 ms                                                                 | 793 ms: 1.17x slower                                        |
| subparsers                 | 21.7 ms                                                                | 25.3 ms: 1.17x slower                                       |
| go                         | 110 ms                                                                 | 129 ms: 1.17x slower                                        |
| tomli_loads                | 1.88 sec                                                               | 2.20 sec: 1.17x slower                                      |
| sqlglot_transpile          | 1.54 ms                                                                | 1.81 ms: 1.17x slower                                       |
| pprint_pformat             | 1.38 sec                                                               | 1.63 sec: 1.18x slower                                      |
| pyflate                    | 403 ms                                                                 | 478 ms: 1.19x slower                                        |
| raytrace                   | 253 ms                                                                 | 300 ms: 1.19x slower                                        |
| sqlglot_optimize           | 50.7 ms                                                                | 60.3 ms: 1.19x slower                                       |
| 2to3                       | 249 ms                                                                 | 296 ms: 1.19x slower                                        |
| sqlglot_normalize          | 99.8 ms                                                                | 119 ms: 1.19x slower                                        |
| spectral_norm              | 90.6 ms                                                                | 108 ms: 1.19x slower                                        |
| sqlglot_parse              | 1.25 ms                                                                | 1.49 ms: 1.20x slower                                       |
| deltablue                  | 3.02 ms                                                                | 3.62 ms: 1.20x slower                                       |
| deepcopy_reduce            | 2.53 us                                                                | 3.03 us: 1.20x slower                                       |
| telco                      | 7.15 ms                                                                | 8.60 ms: 1.20x slower                                       |
| deepcopy                   | 244 us                                                                 | 294 us: 1.20x slower                                        |
| deepcopy_memo              | 29.2 us                                                                | 35.3 us: 1.21x slower                                       |
| sympy_expand               | 450 ms                                                                 | 545 ms: 1.21x slower                                        |
| logging_simple             | 5.91 us                                                                | 7.16 us: 1.21x slower                                       |
| comprehensions             | 16.0 us                                                                | 19.4 us: 1.21x slower                                       |
| chaos                      | 54.5 ms                                                                | 66.1 ms: 1.21x slower                                       |
| xml_etree_process          | 57.3 ms                                                                | 69.5 ms: 1.21x slower                                       |
| coverage                   | 79.5 ms                                                                | 96.5 ms: 1.21x slower                                       |
| scimark_sor                | 112 ms                                                                 | 136 ms: 1.22x slower                                        |
| genshi_xml                 | 47.4 ms                                                                | 57.8 ms: 1.22x slower                                       |
| thrift                     | 715 us                                                                 | 872 us: 1.22x slower                                        |
| sympy_integrate            | 19.3 ms                                                                | 23.6 ms: 1.22x slower                                       |
| regex_compile              | 123 ms                                                                 | 151 ms: 1.22x slower                                        |
| generators                 | 26.8 ms                                                                | 33.0 ms: 1.23x slower                                       |
| sympy_sum                  | 150 ms                                                                 | 185 ms: 1.24x slower                                        |
| sympy_str                  | 267 ms                                                                 | 331 ms: 1.24x slower                                        |
| logging_format             | 6.60 us                                                                | 8.19 us: 1.24x slower                                       |
| sqlalchemy_declarative     | 126 ms                                                                 | 156 ms: 1.24x slower                                        |
| hexiom                     | 5.70 ms                                                                | 7.15 ms: 1.25x slower                                       |
| richards                   | 41.9 ms                                                                | 52.6 ms: 1.25x slower                                       |
| sqlalchemy_imperative      | 19.0 ms                                                                | 23.8 ms: 1.25x slower                                       |
| shortest_path              | 427 ms                                                                 | 539 ms: 1.26x slower                                        |
| connected_components       | 386 ms                                                                 | 488 ms: 1.26x slower                                        |
| nqueens                    | 74.9 ms                                                                | 94.7 ms: 1.26x slower                                       |
| richards_super             | 47.9 ms                                                                | 61.1 ms: 1.28x slower                                       |
| django_template            | 32.9 ms                                                                | 42.1 ms: 1.28x slower                                       |
| python_startup_no_site     | 7.51 ms                                                                | 9.64 ms: 1.28x slower                                       |
| crypto_pyaes               | 66.2 ms                                                                | 84.9 ms: 1.28x slower                                       |
| typing_runtime_protocols   | 153 us                                                                 | 196 us: 1.28x slower                                        |
| meteor_contest             | 97.1 ms                                                                | 125 ms: 1.29x slower                                        |
| fannkuch                   | 363 ms                                                                 | 471 ms: 1.30x slower                                        |
| genshi_text                | 20.4 ms                                                                | 26.5 ms: 1.30x slower                                       |
| mako                       | 11.5 ms                                                                | 15.6 ms: 1.35x slower                                       |
| scimark_lu                 | 112 ms                                                                 | 153 ms: 1.36x slower                                        |
| scimark_fft                | 331 ms                                                                 | 454 ms: 1.37x slower                                        |
| nbody                      | 87.3 ms                                                                | 120 ms: 1.38x slower                                        |
| scimark_monte_carlo        | 63.4 ms                                                                | 89.1 ms: 1.41x slower                                       |
| scimark_sparse_mat_mult    | 4.26 ms                                                                | 7.38 ms: 1.73x slower                                       |
| bench_thread_pool          | 1.03 ms                                                                | 3.27 ms: 3.18x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.16x slower                                                |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (1) of results/bm-20250227-3.14.0a5+-9ad230b-NOGIL/bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5+-9ad230b.json: html5lib

- Geometric mean (including insignificant results): 1.126x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x