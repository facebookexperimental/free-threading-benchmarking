# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d9efa45
- commit date: 2024-07-25
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 690 ms: 1.56x slower                                  |
| docutils       | 3.94 sec                                                              | 5.03 sec: 1.28x slower                                |
| html5lib       | 92.0 ms                                                               | 138 ms: 1.50x slower                                  |
| tornado_http   | 253 ms                                                                | 358 ms: 1.42x slower                                  |
| Geometric mean | (ref)                                                                 | 1.43x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.43 sec                                                              | 1.19 sec: 1.20x faster                                |
| async_tree_none_tg         | 526 ms                                                                | 471 ms: 1.12x faster                                  |
| async_tree_io              | 1.39 sec                                                              | 1.28 sec: 1.09x faster                                |
| async_tree_memoization_tg  | 692 ms                                                                | 641 ms: 1.08x faster                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 843 ms: 1.04x faster                                  |
| asyncio_websockets         | 728 ms                                                                | 760 ms: 1.04x slower                                  |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 975 ms: 1.09x slower                                  |
| asyncio_tcp                | 972 ms                                                                | 1.10 sec: 1.13x slower                                |
| async_tree_none            | 523 ms                                                                | 600 ms: 1.15x slower                                  |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.42 sec: 1.21x slower                                |
| async_generators           | 588 ms                                                                | 741 ms: 1.26x slower                                  |
| coroutines                 | 29.3 ms                                                               | 42.7 ms: 1.46x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.05x slower                                          |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                                                | 246 ms: 1.04x faster                                  |
| float          | 115 ms                                                                | 201 ms: 1.75x slower                                  |
| nbody          | 126 ms                                                                | 291 ms: 2.31x slower                                  |
| Geometric mean | (ref)                                                                 | 1.57x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 189 ms                                                                | 292 ms: 1.54x slower                                  |
| Geometric mean | (ref)                                                                 | 1.13x slower                                          |

Benchmark hidden because not significant (3): regex_v8, regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.46 us: 1.16x faster                                 |
| pickle               | 15.2 us                                                               | 14.4 us: 1.06x faster                                 |
| xml_etree_iterparse  | 163 ms                                                                | 177 ms: 1.09x slower                                  |
| json_loads           | 37.9 us                                                               | 44.5 us: 1.17x slower                                 |
| json_dumps           | 13.9 ms                                                               | 18.3 ms: 1.32x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 163 ms: 1.36x slower                                  |
| tomli_loads          | 2.84 sec                                                              | 4.33 sec: 1.52x slower                                |
| xml_etree_process    | 82.2 ms                                                               | 137 ms: 1.67x slower                                  |
| pickle_pure_python   | 428 us                                                                | 768 us: 1.80x slower                                  |
| unpickle_pure_python | 285 us                                                                | 573 us: 2.01x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.22x slower                                          |

Benchmark hidden because not significant (4): pickle_dict, xml_etree_parse, unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 19.9 ms: 1.24x slower                                 |
| python_startup         | 23.5 ms                                                               | 29.3 ms: 1.25x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.24x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 117 ms: 1.63x slower                                  |
| django_template | 46.1 ms                                                               | 81.6 ms: 1.77x slower                                 |
| mako            | 16.7 ms                                                               | 29.5 ms: 1.77x slower                                 |
| genshi_text     | 31.6 ms                                                               | 57.9 ms: 1.83x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.75x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                      | 229 ms                                                                | 13.8 ms: 16.57x faster                                |
| create_gc_cycles           | 2.49 ms                                                               | 1.87 ms: 1.33x faster                                 |
| bench_mp_pool              | 19.7 ms                                                               | 15.8 ms: 1.25x faster                                 |
| gc_traversal               | 5.80 ms                                                               | 4.66 ms: 1.24x faster                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.19 sec: 1.20x faster                                |
| pickle_list                | 7.48 us                                                               | 6.46 us: 1.16x faster                                 |
| async_tree_none_tg         | 526 ms                                                                | 471 ms: 1.12x faster                                  |
| async_tree_io              | 1.39 sec                                                              | 1.28 sec: 1.09x faster                                |
| async_tree_memoization_tg  | 692 ms                                                                | 641 ms: 1.08x faster                                  |
| pickle                     | 15.2 us                                                               | 14.4 us: 1.06x faster                                 |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 843 ms: 1.04x faster                                  |
| pidigits                   | 256 ms                                                                | 246 ms: 1.04x faster                                  |
| asyncio_websockets         | 728 ms                                                                | 760 ms: 1.04x slower                                  |
| sqlite_synth               | 3.94 us                                                               | 4.23 us: 1.08x slower                                 |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 975 ms: 1.09x slower                                  |
| xml_etree_iterparse        | 163 ms                                                                | 177 ms: 1.09x slower                                  |
| pathlib                    | 31.8 ms                                                               | 35.5 ms: 1.12x slower                                 |
| asyncio_tcp                | 972 ms                                                                | 1.10 sec: 1.13x slower                                |
| deepcopy                   | 498 us                                                                | 566 us: 1.14x slower                                  |
| async_tree_none            | 523 ms                                                                | 600 ms: 1.15x slower                                  |
| json_loads                 | 37.9 us                                                               | 44.5 us: 1.17x slower                                 |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.42 sec: 1.21x slower                                |
| coverage                   | 121 ms                                                                | 149 ms: 1.24x slower                                  |
| python_startup_no_site     | 16.0 ms                                                               | 19.9 ms: 1.24x slower                                 |
| python_startup             | 23.5 ms                                                               | 29.3 ms: 1.25x slower                                 |
| json                       | 6.79 ms                                                               | 8.50 ms: 1.25x slower                                 |
| async_generators           | 588 ms                                                                | 741 ms: 1.26x slower                                  |
| docutils                   | 3.94 sec                                                              | 5.03 sec: 1.28x slower                                |
| pylint                     | 466 ms                                                                | 595 ms: 1.28x slower                                  |
| mdp                        | 4.01 sec                                                              | 5.12 sec: 1.28x slower                                |
| pycparser                  | 1.71 sec                                                              | 2.21 sec: 1.29x slower                                |
| meteor_contest             | 156 ms                                                                | 206 ms: 1.32x slower                                  |
| json_dumps                 | 13.9 ms                                                               | 18.3 ms: 1.32x slower                                 |
| bench_thread_pool          | 3.01 ms                                                               | 3.97 ms: 1.32x slower                                 |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 9.05 ms: 1.32x slower                                 |
| scimark_fft                | 469 ms                                                                | 621 ms: 1.32x slower                                  |
| deepcopy_memo              | 50.9 us                                                               | 67.8 us: 1.33x slower                                 |
| xml_etree_generate         | 120 ms                                                                | 163 ms: 1.36x slower                                  |
| nqueens                    | 108 ms                                                                | 151 ms: 1.39x slower                                  |
| deepcopy_reduce            | 4.31 us                                                               | 6.02 us: 1.40x slower                                 |
| generators                 | 40.7 ms                                                               | 57.4 ms: 1.41x slower                                 |
| tornado_http               | 253 ms                                                                | 358 ms: 1.42x slower                                  |
| coroutines                 | 29.3 ms                                                               | 42.7 ms: 1.46x slower                                 |
| crypto_pyaes               | 102 ms                                                                | 149 ms: 1.46x slower                                  |
| html5lib                   | 92.0 ms                                                               | 138 ms: 1.50x slower                                  |
| fannkuch                   | 535 ms                                                                | 802 ms: 1.50x slower                                  |
| richards                   | 68.8 ms                                                               | 105 ms: 1.52x slower                                  |
| bpe_tokeniser              | 6.53 sec                                                              | 9.93 sec: 1.52x slower                                |
| tomli_loads                | 2.84 sec                                                              | 4.33 sec: 1.52x slower                                |
| sympy_integrate            | 28.7 ms                                                               | 44.3 ms: 1.54x slower                                 |
| pyflate                    | 710 ms                                                                | 1.09 sec: 1.54x slower                                |
| regex_compile              | 189 ms                                                                | 292 ms: 1.54x slower                                  |
| sqlglot_normalize          | 150 ms                                                                | 233 ms: 1.55x slower                                  |
| 2to3                       | 441 ms                                                                | 690 ms: 1.56x slower                                  |
| sqlglot_optimize           | 77.9 ms                                                               | 123 ms: 1.58x slower                                  |
| spectral_norm              | 151 ms                                                                | 244 ms: 1.61x slower                                  |
| genshi_xml                 | 71.9 ms                                                               | 117 ms: 1.63x slower                                  |
| thrift                     | 1.09 ms                                                               | 1.77 ms: 1.63x slower                                 |
| xml_etree_process          | 82.2 ms                                                               | 137 ms: 1.67x slower                                  |
| typing_runtime_protocols   | 222 us                                                                | 377 us: 1.70x slower                                  |
| logging_simple             | 9.16 us                                                               | 15.9 us: 1.73x slower                                 |
| comprehensions             | 22.6 us                                                               | 39.2 us: 1.73x slower                                 |
| float                      | 115 ms                                                                | 201 ms: 1.75x slower                                  |
| pprint_safe_repr           | 991 ms                                                                | 1.74 sec: 1.75x slower                                |
| django_template            | 46.1 ms                                                               | 81.6 ms: 1.77x slower                                 |
| pprint_pformat             | 2.04 sec                                                              | 3.60 sec: 1.77x slower                                |
| mako                       | 16.7 ms                                                               | 29.5 ms: 1.77x slower                                 |
| pickle_pure_python         | 428 us                                                                | 768 us: 1.80x slower                                  |
| richards_super             | 73.5 ms                                                               | 134 ms: 1.82x slower                                  |
| genshi_text                | 31.6 ms                                                               | 57.9 ms: 1.83x slower                                 |
| logging_silent             | 137 ns                                                                | 259 ns: 1.89x slower                                  |
| scimark_monte_carlo        | 89.0 ms                                                               | 168 ms: 1.89x slower                                  |
| sympy_str                  | 376 ms                                                                | 713 ms: 1.89x slower                                  |
| hexiom                     | 8.42 ms                                                               | 16.3 ms: 1.94x slower                                 |
| scimark_sor                | 176 ms                                                                | 342 ms: 1.94x slower                                  |
| logging_format             | 9.36 us                                                               | 18.2 us: 1.95x slower                                 |
| sqlglot_parse              | 1.92 ms                                                               | 3.81 ms: 1.99x slower                                 |
| unpickle_pure_python       | 285 us                                                                | 573 us: 2.01x slower                                  |
| sympy_expand               | 638 ms                                                                | 1.29 sec: 2.03x slower                                |
| sqlglot_transpile          | 2.24 ms                                                               | 4.65 ms: 2.07x slower                                 |
| go                         | 193 ms                                                                | 405 ms: 2.10x slower                                  |
| chaos                      | 81.5 ms                                                               | 175 ms: 2.14x slower                                  |
| sympy_sum                  | 226 ms                                                                | 487 ms: 2.15x slower                                  |
| scimark_lu                 | 150 ms                                                                | 323 ms: 2.16x slower                                  |
| raytrace                   | 351 ms                                                                | 805 ms: 2.29x slower                                  |
| nbody                      | 126 ms                                                                | 291 ms: 2.31x slower                                  |
| deltablue                  | 4.55 ms                                                               | 12.1 ms: 2.66x slower                                 |
| unpack_sequence            | 54.6 ns                                                               | 190 ns: 3.49x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.36x slower                                          |

Benchmark hidden because not significant (8): pickle_dict, async_tree_memoization, xml_etree_parse, unpickle, regex_v8, unpickle_list, regex_dna, regex_effbot
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.16x