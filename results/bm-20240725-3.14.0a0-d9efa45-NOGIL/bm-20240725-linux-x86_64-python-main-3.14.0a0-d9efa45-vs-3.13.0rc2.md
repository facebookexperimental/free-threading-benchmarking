# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d9efa45
- commit date: 2024-07-25
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 690 ms: 1.55x slower                                  |
| docutils       | 4.01 sec                                                     | 5.03 sec: 1.25x slower                                |
| html5lib       | 92.6 ms                                                      | 138 ms: 1.49x slower                                  |
| tornado_http   | 251 ms                                                       | 358 ms: 1.43x slower                                  |
| Geometric mean | (ref)                                                        | 1.42x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|---------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg          | 1.40 sec                                                     | 1.19 sec: 1.17x faster                                |
| async_tree_io             | 1.39 sec                                                     | 1.28 sec: 1.09x faster                                |
| async_tree_none_tg        | 504 ms                                                       | 471 ms: 1.07x faster                                  |
| async_tree_memoization_tg | 670 ms                                                       | 641 ms: 1.05x faster                                  |
| async_tree_memoization    | 709 ms                                                       | 744 ms: 1.05x slower                                  |
| async_tree_none           | 572 ms                                                       | 600 ms: 1.05x slower                                  |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 975 ms: 1.10x slower                                  |
| asyncio_tcp               | 948 ms                                                       | 1.10 sec: 1.16x slower                                |
| asyncio_tcp_ssl           | 2.77 sec                                                     | 3.42 sec: 1.23x slower                                |
| async_generators          | 567 ms                                                       | 741 ms: 1.31x slower                                  |
| coroutines                | 30.9 ms                                                      | 42.7 ms: 1.39x slower                                 |
| Geometric mean            | (ref)                                                        | 1.06x slower                                          |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 116 ms                                                       | 201 ms: 1.74x slower                                  |
| nbody          | 119 ms                                                       | 291 ms: 2.45x slower                                  |
| Geometric mean | (ref)                                                        | 1.61x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 36.8 ms: 1.12x slower                                 |
| regex_compile  | 182 ms                                                       | 292 ms: 1.61x slower                                  |
| Geometric mean | (ref)                                                        | 1.17x slower                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                       | 213 ms: 1.08x faster                                  |
| pickle_dict          | 47.2 us                                                      | 44.3 us: 1.06x faster                                 |
| pickle_list          | 6.86 us                                                      | 6.46 us: 1.06x faster                                 |
| pickle               | 15.1 us                                                      | 14.4 us: 1.05x faster                                 |
| unpickle_list        | 6.68 us                                                      | 6.83 us: 1.02x slower                                 |
| unpickle             | 20.5 us                                                      | 22.0 us: 1.07x slower                                 |
| json_loads           | 34.3 us                                                      | 44.5 us: 1.30x slower                                 |
| json_dumps           | 14.1 ms                                                      | 18.3 ms: 1.30x slower                                 |
| xml_etree_generate   | 122 ms                                                       | 163 ms: 1.33x slower                                  |
| tomli_loads          | 2.78 sec                                                     | 4.33 sec: 1.56x slower                                |
| xml_etree_process    | 85.9 ms                                                      | 137 ms: 1.60x slower                                  |
| pickle_pure_python   | 416 us                                                       | 768 us: 1.84x slower                                  |
| unpickle_pure_python | 290 us                                                       | 573 us: 1.97x slower                                  |
| Geometric mean       | (ref)                                                        | 1.23x slower                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                 |
| python_startup         | 22.4 ms                                                      | 29.3 ms: 1.31x slower                                 |
| Geometric mean         | (ref)                                                        | 1.30x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 117 ms: 1.62x slower                                  |
| genshi_text     | 31.7 ms                                                      | 57.9 ms: 1.83x slower                                 |
| django_template | 44.3 ms                                                      | 81.6 ms: 1.84x slower                                 |
| mako            | 15.9 ms                                                      | 29.5 ms: 1.85x slower                                 |
| Geometric mean  | (ref)                                                        | 1.78x slower                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|---------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| create_gc_cycles          | 2.41 ms                                                      | 1.87 ms: 1.29x faster                                 |
| gc_traversal              | 5.70 ms                                                      | 4.66 ms: 1.22x faster                                 |
| bench_mp_pool             | 18.7 ms                                                      | 15.8 ms: 1.19x faster                                 |
| async_tree_io_tg          | 1.40 sec                                                     | 1.19 sec: 1.17x faster                                |
| async_tree_io             | 1.39 sec                                                     | 1.28 sec: 1.09x faster                                |
| xml_etree_parse           | 231 ms                                                       | 213 ms: 1.08x faster                                  |
| async_tree_none_tg        | 504 ms                                                       | 471 ms: 1.07x faster                                  |
| pickle_dict               | 47.2 us                                                      | 44.3 us: 1.06x faster                                 |
| pickle_list               | 6.86 us                                                      | 6.46 us: 1.06x faster                                 |
| pickle                    | 15.1 us                                                      | 14.4 us: 1.05x faster                                 |
| async_tree_memoization_tg | 670 ms                                                       | 641 ms: 1.05x faster                                  |
| unpickle_list             | 6.68 us                                                      | 6.83 us: 1.02x slower                                 |
| async_tree_memoization    | 709 ms                                                       | 744 ms: 1.05x slower                                  |
| async_tree_none           | 572 ms                                                       | 600 ms: 1.05x slower                                  |
| sqlite_synth              | 3.99 us                                                      | 4.23 us: 1.06x slower                                 |
| unpickle                  | 20.5 us                                                      | 22.0 us: 1.07x slower                                 |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 975 ms: 1.10x slower                                  |
| regex_v8                  | 32.8 ms                                                      | 36.8 ms: 1.12x slower                                 |
| telco                     | 12.2 ms                                                      | 13.8 ms: 1.14x slower                                 |
| deepcopy                  | 498 us                                                       | 566 us: 1.14x slower                                  |
| asyncio_tcp               | 948 ms                                                       | 1.10 sec: 1.16x slower                                |
| pathlib                   | 29.9 ms                                                      | 35.5 ms: 1.19x slower                                 |
| asyncio_tcp_ssl           | 2.77 sec                                                     | 3.42 sec: 1.23x slower                                |
| docutils                  | 4.01 sec                                                     | 5.03 sec: 1.25x slower                                |
| pylint                    | 470 ms                                                       | 595 ms: 1.27x slower                                  |
| json_loads                | 34.3 us                                                      | 44.5 us: 1.30x slower                                 |
| python_startup_no_site    | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                 |
| json_dumps                | 14.1 ms                                                      | 18.3 ms: 1.30x slower                                 |
| json                      | 6.51 ms                                                      | 8.50 ms: 1.30x slower                                 |
| async_generators          | 567 ms                                                       | 741 ms: 1.31x slower                                  |
| python_startup            | 22.4 ms                                                      | 29.3 ms: 1.31x slower                                 |
| scimark_fft               | 473 ms                                                       | 621 ms: 1.31x slower                                  |
| xml_etree_generate        | 122 ms                                                       | 163 ms: 1.33x slower                                  |
| scimark_sparse_mat_mult   | 6.76 ms                                                      | 9.05 ms: 1.34x slower                                 |
| mdp                       | 3.80 sec                                                     | 5.12 sec: 1.35x slower                                |
| nqueens                   | 112 ms                                                       | 151 ms: 1.35x slower                                  |
| deepcopy_memo             | 50.1 us                                                      | 67.8 us: 1.35x slower                                 |
| meteor_contest            | 150 ms                                                       | 206 ms: 1.37x slower                                  |
| bench_thread_pool         | 2.89 ms                                                      | 3.97 ms: 1.38x slower                                 |
| coroutines                | 30.9 ms                                                      | 42.7 ms: 1.39x slower                                 |
| coverage                  | 107 ms                                                       | 149 ms: 1.39x slower                                  |
| pycparser                 | 1.57 sec                                                     | 2.21 sec: 1.41x slower                                |
| tornado_http              | 251 ms                                                       | 358 ms: 1.43x slower                                  |
| generators                | 40.0 ms                                                      | 57.4 ms: 1.44x slower                                 |
| sympy_integrate           | 30.2 ms                                                      | 44.3 ms: 1.46x slower                                 |
| fannkuch                  | 547 ms                                                       | 802 ms: 1.47x slower                                  |
| deepcopy_reduce           | 4.10 us                                                      | 6.02 us: 1.47x slower                                 |
| html5lib                  | 92.6 ms                                                      | 138 ms: 1.49x slower                                  |
| crypto_pyaes              | 100 ms                                                       | 149 ms: 1.49x slower                                  |
| 2to3                      | 445 ms                                                       | 690 ms: 1.55x slower                                  |
| spectral_norm             | 157 ms                                                       | 244 ms: 1.56x slower                                  |
| tomli_loads               | 2.78 sec                                                     | 4.33 sec: 1.56x slower                                |
| bpe_tokeniser             | 6.28 sec                                                     | 9.93 sec: 1.58x slower                                |
| richards                  | 65.5 ms                                                      | 105 ms: 1.60x slower                                  |
| xml_etree_process         | 85.9 ms                                                      | 137 ms: 1.60x slower                                  |
| regex_compile             | 182 ms                                                       | 292 ms: 1.61x slower                                  |
| thrift                    | 1.10 ms                                                      | 1.77 ms: 1.61x slower                                 |
| genshi_xml                | 72.1 ms                                                      | 117 ms: 1.62x slower                                  |
| sqlglot_optimize          | 74.7 ms                                                      | 123 ms: 1.64x slower                                  |
| pyflate                   | 664 ms                                                       | 1.09 sec: 1.65x slower                                |
| sqlglot_normalize         | 140 ms                                                       | 233 ms: 1.67x slower                                  |
| typing_runtime_protocols  | 226 us                                                       | 377 us: 1.67x slower                                  |
| float                     | 116 ms                                                       | 201 ms: 1.74x slower                                  |
| pprint_safe_repr          | 987 ms                                                       | 1.74 sec: 1.76x slower                                |
| comprehensions            | 22.2 us                                                      | 39.2 us: 1.76x slower                                 |
| richards_super            | 73.2 ms                                                      | 134 ms: 1.83x slower                                  |
| genshi_text               | 31.7 ms                                                      | 57.9 ms: 1.83x slower                                 |
| django_template           | 44.3 ms                                                      | 81.6 ms: 1.84x slower                                 |
| pickle_pure_python        | 416 us                                                       | 768 us: 1.84x slower                                  |
| mako                      | 15.9 ms                                                      | 29.5 ms: 1.85x slower                                 |
| logging_simple            | 8.56 us                                                      | 15.9 us: 1.85x slower                                 |
| pprint_pformat            | 1.94 sec                                                     | 3.60 sec: 1.85x slower                                |
| scimark_monte_carlo       | 90.6 ms                                                      | 168 ms: 1.86x slower                                  |
| sympy_str                 | 379 ms                                                       | 713 ms: 1.88x slower                                  |
| scimark_sor               | 179 ms                                                       | 342 ms: 1.92x slower                                  |
| logging_format            | 9.24 us                                                      | 18.2 us: 1.97x slower                                 |
| unpickle_pure_python      | 290 us                                                       | 573 us: 1.97x slower                                  |
| logging_silent            | 130 ns                                                       | 259 ns: 1.99x slower                                  |
| hexiom                    | 8.11 ms                                                      | 16.3 ms: 2.02x slower                                 |
| chaos                     | 83.6 ms                                                      | 175 ms: 2.09x slower                                  |
| sqlglot_transpile         | 2.20 ms                                                      | 4.65 ms: 2.12x slower                                 |
| go                        | 191 ms                                                       | 405 ms: 2.12x slower                                  |
| sympy_expand              | 601 ms                                                       | 1.29 sec: 2.16x slower                                |
| sqlglot_parse             | 1.76 ms                                                      | 3.81 ms: 2.17x slower                                 |
| scimark_lu                | 146 ms                                                       | 323 ms: 2.21x slower                                  |
| sympy_sum                 | 210 ms                                                       | 487 ms: 2.32x slower                                  |
| raytrace                  | 344 ms                                                       | 805 ms: 2.34x slower                                  |
| nbody                     | 119 ms                                                       | 291 ms: 2.45x slower                                  |
| unpack_sequence           | 74.3 ns                                                      | 190 ns: 2.56x slower                                  |
| deltablue                 | 4.44 ms                                                      | 12.1 ms: 2.73x slower                                 |
| Geometric mean            | (ref)                                                        | 1.42x slower                                          |

Benchmark hidden because not significant (6): pidigits, async_tree_cpu_io_mixed_tg, asyncio_websockets, xml_etree_iterparse, regex_effbot, regex_dna
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.16x