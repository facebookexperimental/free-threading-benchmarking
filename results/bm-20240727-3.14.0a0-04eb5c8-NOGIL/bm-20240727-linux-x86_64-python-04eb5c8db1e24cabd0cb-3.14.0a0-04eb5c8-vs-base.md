# Results vs. base

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.44x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240727-3.14.0a0-04eb5c8/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json | results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 425 ms                                                                                                          | 647 ms: 1.52x slower                                                                                                  |
| docutils       | 3.95 sec                                                                                                        | 4.82 sec: 1.22x slower                                                                                                |
| html5lib       | 93.1 ms                                                                                                         | 141 ms: 1.51x slower                                                                                                  |
| tornado_http   | 228 ms                                                                                                          | 342 ms: 1.50x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.43x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20240727-3.14.0a0-04eb5c8/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json | results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json |
|---------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg          | 1.22 sec                                                                                                        | 1.12 sec: 1.10x faster                                                                                                |
| async_tree_none_tg        | 451 ms                                                                                                          | 482 ms: 1.07x slower                                                                                                  |
| async_tree_memoization_tg | 591 ms                                                                                                          | 632 ms: 1.07x slower                                                                                                  |
| async_tree_none           | 499 ms                                                                                                          | 566 ms: 1.13x slower                                                                                                  |
| async_tree_cpu_io_mixed   | 794 ms                                                                                                          | 913 ms: 1.15x slower                                                                                                  |
| async_tree_memoization    | 626 ms                                                                                                          | 721 ms: 1.15x slower                                                                                                  |
| Geometric mean            | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmark hidden because not significant (2): async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240727-3.14.0a0-04eb5c8/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json | results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 112 ms                                                                                                          | 193 ms: 1.72x slower                                                                                                  |
| nbody          | 118 ms                                                                                                          | 280 ms: 2.37x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.60x slower                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240727-3.14.0a0-04eb5c8/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json | results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 4.78 ms                                                                                                         | 4.47 ms: 1.07x faster                                                                                                 |
| regex_dna      | 282 ms                                                                                                          | 295 ms: 1.04x slower                                                                                                  |
| regex_compile  | 174 ms                                                                                                          | 293 ms: 1.68x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.13x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240727-3.14.0a0-04eb5c8/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json | results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 230 ms                                                                                                          | 201 ms: 1.14x faster                                                                                                  |
| pickle               | 15.6 us                                                                                                         | 14.5 us: 1.07x faster                                                                                                 |
| pickle_dict          | 46.8 us                                                                                                         | 44.0 us: 1.06x faster                                                                                                 |
| unpickle_list        | 7.22 us                                                                                                         | 7.76 us: 1.08x slower                                                                                                 |
| unpickle             | 19.8 us                                                                                                         | 22.0 us: 1.11x slower                                                                                                 |
| json_dumps           | 15.5 ms                                                                                                         | 17.8 ms: 1.15x slower                                                                                                 |
| json_loads           | 37.1 us                                                                                                         | 43.6 us: 1.17x slower                                                                                                 |
| xml_etree_generate   | 117 ms                                                                                                          | 160 ms: 1.37x slower                                                                                                  |
| xml_etree_process    | 81.3 ms                                                                                                         | 126 ms: 1.55x slower                                                                                                  |
| tomli_loads          | 2.66 sec                                                                                                        | 4.22 sec: 1.59x slower                                                                                                |
| unpickle_pure_python | 306 us                                                                                                          | 558 us: 1.83x slower                                                                                                  |
| pickle_pure_python   | 431 us                                                                                                          | 830 us: 1.92x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                           | 1.21x slower                                                                                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240727-3.14.0a0-04eb5c8/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json | results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 15.0 ms                                                                                                         | 19.5 ms: 1.30x slower                                                                                                 |
| python_startup         | 22.1 ms                                                                                                         | 28.9 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.30x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240727-3.14.0a0-04eb5c8/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json | results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 73.3 ms                                                                                                         | 120 ms: 1.63x slower                                                                                                  |
| genshi_text     | 30.2 ms                                                                                                         | 54.4 ms: 1.80x slower                                                                                                 |
| mako            | 16.3 ms                                                                                                         | 29.9 ms: 1.83x slower                                                                                                 |
| django_template | 44.0 ms                                                                                                         | 80.6 ms: 1.83x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.77x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                 | results/bm-20240727-3.14.0a0-04eb5c8/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json | results/bm-20240727-3.14.0a0-04eb5c8-NOGIL/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json |
|---------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool             | 19.0 ms                                                                                                         | 13.6 ms: 1.39x faster                                                                                                 |
| gc_traversal              | 5.48 ms                                                                                                         | 4.28 ms: 1.28x faster                                                                                                 |
| create_gc_cycles          | 2.32 ms                                                                                                         | 1.95 ms: 1.19x faster                                                                                                 |
| xml_etree_parse           | 230 ms                                                                                                          | 201 ms: 1.14x faster                                                                                                  |
| async_tree_io_tg          | 1.22 sec                                                                                                        | 1.12 sec: 1.10x faster                                                                                                |
| pickle                    | 15.6 us                                                                                                         | 14.5 us: 1.07x faster                                                                                                 |
| regex_effbot              | 4.78 ms                                                                                                         | 4.47 ms: 1.07x faster                                                                                                 |
| pickle_dict               | 46.8 us                                                                                                         | 44.0 us: 1.06x faster                                                                                                 |
| regex_dna                 | 282 ms                                                                                                          | 295 ms: 1.04x slower                                                                                                  |
| async_tree_none_tg        | 451 ms                                                                                                          | 482 ms: 1.07x slower                                                                                                  |
| async_tree_memoization_tg | 591 ms                                                                                                          | 632 ms: 1.07x slower                                                                                                  |
| unpickle_list             | 7.22 us                                                                                                         | 7.76 us: 1.08x slower                                                                                                 |
| asyncio_tcp               | 928 ms                                                                                                          | 1.02 sec: 1.10x slower                                                                                                |
| unpickle                  | 19.8 us                                                                                                         | 22.0 us: 1.11x slower                                                                                                 |
| async_tree_none           | 499 ms                                                                                                          | 566 ms: 1.13x slower                                                                                                  |
| json                      | 6.72 ms                                                                                                         | 7.69 ms: 1.15x slower                                                                                                 |
| json_dumps                | 15.5 ms                                                                                                         | 17.8 ms: 1.15x slower                                                                                                 |
| async_tree_cpu_io_mixed   | 794 ms                                                                                                          | 913 ms: 1.15x slower                                                                                                  |
| async_tree_memoization    | 626 ms                                                                                                          | 721 ms: 1.15x slower                                                                                                  |
| asyncio_tcp_ssl           | 2.74 sec                                                                                                        | 3.18 sec: 1.16x slower                                                                                                |
| json_loads                | 37.1 us                                                                                                         | 43.6 us: 1.17x slower                                                                                                 |
| pylint                    | 477 ms                                                                                                          | 562 ms: 1.18x slower                                                                                                  |
| coverage                  | 118 ms                                                                                                          | 141 ms: 1.20x slower                                                                                                  |
| docutils                  | 3.95 sec                                                                                                        | 4.82 sec: 1.22x slower                                                                                                |
| coroutines                | 31.6 ms                                                                                                         | 39.3 ms: 1.24x slower                                                                                                 |
| async_generators          | 580 ms                                                                                                          | 723 ms: 1.25x slower                                                                                                  |
| pathlib                   | 26.6 ms                                                                                                         | 33.2 ms: 1.25x slower                                                                                                 |
| telco                     | 10.9 ms                                                                                                         | 14.1 ms: 1.29x slower                                                                                                 |
| python_startup_no_site    | 15.0 ms                                                                                                         | 19.5 ms: 1.30x slower                                                                                                 |
| python_startup            | 22.1 ms                                                                                                         | 28.9 ms: 1.31x slower                                                                                                 |
| pycparser                 | 1.63 sec                                                                                                        | 2.18 sec: 1.33x slower                                                                                                |
| scimark_fft               | 471 ms                                                                                                          | 641 ms: 1.36x slower                                                                                                  |
| xml_etree_generate        | 117 ms                                                                                                          | 160 ms: 1.37x slower                                                                                                  |
| nqueens                   | 117 ms                                                                                                          | 162 ms: 1.38x slower                                                                                                  |
| mdp                       | 3.64 sec                                                                                                        | 5.02 sec: 1.38x slower                                                                                                |
| generators                | 39.3 ms                                                                                                         | 54.8 ms: 1.40x slower                                                                                                 |
| bench_thread_pool         | 2.97 ms                                                                                                         | 4.27 ms: 1.44x slower                                                                                                 |
| fannkuch                  | 536 ms                                                                                                          | 772 ms: 1.44x slower                                                                                                  |
| scimark_sparse_mat_mult   | 5.99 ms                                                                                                         | 8.68 ms: 1.45x slower                                                                                                 |
| tornado_http              | 228 ms                                                                                                          | 342 ms: 1.50x slower                                                                                                  |
| meteor_contest            | 138 ms                                                                                                          | 208 ms: 1.50x slower                                                                                                  |
| html5lib                  | 93.1 ms                                                                                                         | 141 ms: 1.51x slower                                                                                                  |
| 2to3                      | 425 ms                                                                                                          | 647 ms: 1.52x slower                                                                                                  |
| sympy_integrate           | 28.1 ms                                                                                                         | 42.8 ms: 1.52x slower                                                                                                 |
| thrift                    | 1.10 ms                                                                                                         | 1.70 ms: 1.54x slower                                                                                                 |
| typing_runtime_protocols  | 234 us                                                                                                          | 362 us: 1.54x slower                                                                                                  |
| xml_etree_process         | 81.3 ms                                                                                                         | 126 ms: 1.55x slower                                                                                                  |
| deepcopy_reduce           | 3.64 us                                                                                                         | 5.73 us: 1.58x slower                                                                                                 |
| tomli_loads               | 2.66 sec                                                                                                        | 4.22 sec: 1.59x slower                                                                                                |
| crypto_pyaes              | 99.9 ms                                                                                                         | 159 ms: 1.59x slower                                                                                                  |
| spectral_norm             | 150 ms                                                                                                          | 242 ms: 1.61x slower                                                                                                  |
| deepcopy                  | 372 us                                                                                                          | 600 us: 1.61x slower                                                                                                  |
| bpe_tokeniser             | 6.13 sec                                                                                                        | 9.90 sec: 1.62x slower                                                                                                |
| pyflate                   | 657 ms                                                                                                          | 1.07 sec: 1.63x slower                                                                                                |
| genshi_xml                | 73.3 ms                                                                                                         | 120 ms: 1.63x slower                                                                                                  |
| regex_compile             | 174 ms                                                                                                          | 293 ms: 1.68x slower                                                                                                  |
| sqlglot_normalize         | 144 ms                                                                                                          | 246 ms: 1.71x slower                                                                                                  |
| sqlglot_optimize          | 77.5 ms                                                                                                         | 133 ms: 1.72x slower                                                                                                  |
| float                     | 112 ms                                                                                                          | 193 ms: 1.72x slower                                                                                                  |
| richards                  | 63.4 ms                                                                                                         | 111 ms: 1.76x slower                                                                                                  |
| pprint_safe_repr          | 972 ms                                                                                                          | 1.73 sec: 1.78x slower                                                                                                |
| pprint_pformat            | 1.94 sec                                                                                                        | 3.48 sec: 1.79x slower                                                                                                |
| genshi_text               | 30.2 ms                                                                                                         | 54.4 ms: 1.80x slower                                                                                                 |
| deepcopy_memo             | 38.4 us                                                                                                         | 69.1 us: 1.80x slower                                                                                                 |
| unpickle_pure_python      | 306 us                                                                                                          | 558 us: 1.83x slower                                                                                                  |
| mako                      | 16.3 ms                                                                                                         | 29.9 ms: 1.83x slower                                                                                                 |
| comprehensions            | 20.9 us                                                                                                         | 38.3 us: 1.83x slower                                                                                                 |
| django_template           | 44.0 ms                                                                                                         | 80.6 ms: 1.83x slower                                                                                                 |
| richards_super            | 66.2 ms                                                                                                         | 125 ms: 1.90x slower                                                                                                  |
| sympy_str                 | 345 ms                                                                                                          | 663 ms: 1.92x slower                                                                                                  |
| pickle_pure_python        | 431 us                                                                                                          | 830 us: 1.92x slower                                                                                                  |
| scimark_monte_carlo       | 87.1 ms                                                                                                         | 171 ms: 1.96x slower                                                                                                  |
| logging_format            | 8.93 us                                                                                                         | 17.6 us: 1.98x slower                                                                                                 |
| logging_simple            | 7.95 us                                                                                                         | 15.9 us: 2.00x slower                                                                                                 |
| scimark_lu                | 155 ms                                                                                                          | 313 ms: 2.02x slower                                                                                                  |
| logging_silent            | 128 ns                                                                                                          | 259 ns: 2.03x slower                                                                                                  |
| hexiom                    | 8.49 ms                                                                                                         | 17.4 ms: 2.05x slower                                                                                                 |
| chaos                     | 79.1 ms                                                                                                         | 163 ms: 2.06x slower                                                                                                  |
| scimark_sor               | 168 ms                                                                                                          | 351 ms: 2.09x slower                                                                                                  |
| sqlglot_transpile         | 2.12 ms                                                                                                         | 4.53 ms: 2.14x slower                                                                                                 |
| sympy_expand              | 591 ms                                                                                                          | 1.27 sec: 2.14x slower                                                                                                |
| go                        | 188 ms                                                                                                          | 406 ms: 2.16x slower                                                                                                  |
| sqlglot_parse             | 1.69 ms                                                                                                         | 3.76 ms: 2.22x slower                                                                                                 |
| nbody                     | 118 ms                                                                                                          | 280 ms: 2.37x slower                                                                                                  |
| sympy_sum                 | 207 ms                                                                                                          | 493 ms: 2.38x slower                                                                                                  |
| raytrace                  | 338 ms                                                                                                          | 806 ms: 2.39x slower                                                                                                  |
| deltablue                 | 4.11 ms                                                                                                         | 11.7 ms: 2.84x slower                                                                                                 |
| unpack_sequence           | 67.4 ns                                                                                                         | 201 ns: 2.98x slower                                                                                                  |
| Geometric mean            | (ref)                                                                                                           | 1.44x slower                                                                                                          |

Benchmark hidden because not significant (8): async_tree_io, asyncio_websockets, regex_v8, pidigits, xml_etree_iterparse, async_tree_cpu_io_mixed_tg, pickle_list, sqlite_synth
Ignored benchmarks (1) of results/bm-20240727-3.14.0a0-04eb5c8/bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8.json: dask

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.35x
- 99% likely to have a slowdown of 1.30x

# Memory
- memory change: 1.14x