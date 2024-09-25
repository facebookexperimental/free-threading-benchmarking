# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4767a6e
- commit date: 2024-08-06
- overall geometric mean: 1.38x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 666 ms: 1.51x slower                                  |
| docutils       | 3.94 sec                                                              | 5.00 sec: 1.27x slower                                |
| html5lib       | 92.0 ms                                                               | 162 ms: 1.76x slower                                  |
| tornado_http   | 253 ms                                                                | 337 ms: 1.33x slower                                  |
| Geometric mean | (ref)                                                                 | 1.46x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg          | 1.43 sec                                                              | 1.14 sec: 1.26x faster                                |
| async_tree_io             | 1.39 sec                                                              | 1.24 sec: 1.12x faster                                |
| async_tree_memoization_tg | 692 ms                                                                | 634 ms: 1.09x faster                                  |
| async_tree_none_tg        | 526 ms                                                                | 483 ms: 1.09x faster                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 961 ms: 1.07x slower                                  |
| asyncio_tcp               | 972 ms                                                                | 1.11 sec: 1.14x slower                                |
| async_tree_none           | 523 ms                                                                | 607 ms: 1.16x slower                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.33 sec: 1.18x slower                                |
| async_generators          | 588 ms                                                                | 740 ms: 1.26x slower                                  |
| coroutines                | 29.3 ms                                                               | 43.8 ms: 1.49x slower                                 |
| Geometric mean            | (ref)                                                                 | 1.05x slower                                          |

Benchmark hidden because not significant (3): async_tree_memoization, asyncio_websockets, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                                                | 267 ms: 1.04x slower                                  |
| float          | 115 ms                                                                | 190 ms: 1.65x slower                                  |
| nbody          | 126 ms                                                                | 309 ms: 2.46x slower                                  |
| Geometric mean | (ref)                                                                 | 1.62x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.63 ms                                                               | 4.97 ms: 1.07x slower                                 |
| regex_dna      | 284 ms                                                                | 304 ms: 1.07x slower                                  |
| regex_compile  | 189 ms                                                                | 288 ms: 1.52x slower                                  |
| Geometric mean | (ref)                                                                 | 1.15x slower                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.56 us: 1.14x faster                                 |
| pickle_dict          | 46.5 us                                                               | 42.8 us: 1.08x faster                                 |
| pickle               | 15.2 us                                                               | 14.1 us: 1.08x faster                                 |
| unpickle             | 22.2 us                                                               | 24.7 us: 1.11x slower                                 |
| unpickle_list        | 6.78 us                                                               | 7.55 us: 1.11x slower                                 |
| json_loads           | 37.9 us                                                               | 45.4 us: 1.20x slower                                 |
| json_dumps           | 13.9 ms                                                               | 18.6 ms: 1.34x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 162 ms: 1.35x slower                                  |
| tomli_loads          | 2.84 sec                                                              | 4.21 sec: 1.48x slower                                |
| xml_etree_process    | 82.2 ms                                                               | 132 ms: 1.60x slower                                  |
| pickle_pure_python   | 428 us                                                                | 764 us: 1.79x slower                                  |
| unpickle_pure_python | 285 us                                                                | 537 us: 1.88x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.22x slower                                          |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 19.2 ms: 1.20x slower                                 |
| python_startup         | 23.5 ms                                                               | 29.3 ms: 1.25x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.22x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 123 ms: 1.71x slower                                  |
| django_template | 46.1 ms                                                               | 81.9 ms: 1.78x slower                                 |
| genshi_text     | 31.6 ms                                                               | 56.5 ms: 1.79x slower                                 |
| mako            | 16.7 ms                                                               | 30.3 ms: 1.82x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.77x slower                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                     | 229 ms                                                                | 14.8 ms: 15.53x faster                                |
| async_tree_io_tg          | 1.43 sec                                                              | 1.14 sec: 1.26x faster                                |
| create_gc_cycles          | 2.49 ms                                                               | 1.99 ms: 1.25x faster                                 |
| bench_mp_pool             | 19.7 ms                                                               | 16.0 ms: 1.23x faster                                 |
| gc_traversal              | 5.80 ms                                                               | 5.03 ms: 1.15x faster                                 |
| pickle_list               | 7.48 us                                                               | 6.56 us: 1.14x faster                                 |
| async_tree_io             | 1.39 sec                                                              | 1.24 sec: 1.12x faster                                |
| async_tree_memoization_tg | 692 ms                                                                | 634 ms: 1.09x faster                                  |
| async_tree_none_tg        | 526 ms                                                                | 483 ms: 1.09x faster                                  |
| pickle_dict               | 46.5 us                                                               | 42.8 us: 1.08x faster                                 |
| pickle                    | 15.2 us                                                               | 14.1 us: 1.08x faster                                 |
| pidigits                  | 256 ms                                                                | 267 ms: 1.04x slower                                  |
| pathlib                   | 31.8 ms                                                               | 33.6 ms: 1.06x slower                                 |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 961 ms: 1.07x slower                                  |
| regex_effbot              | 4.63 ms                                                               | 4.97 ms: 1.07x slower                                 |
| sqlite_synth              | 3.94 us                                                               | 4.22 us: 1.07x slower                                 |
| regex_dna                 | 284 ms                                                                | 304 ms: 1.07x slower                                  |
| unpickle                  | 22.2 us                                                               | 24.7 us: 1.11x slower                                 |
| unpickle_list             | 6.78 us                                                               | 7.55 us: 1.11x slower                                 |
| asyncio_tcp               | 972 ms                                                                | 1.11 sec: 1.14x slower                                |
| async_tree_none           | 523 ms                                                                | 607 ms: 1.16x slower                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.33 sec: 1.18x slower                                |
| python_startup_no_site    | 16.0 ms                                                               | 19.2 ms: 1.20x slower                                 |
| json_loads                | 37.9 us                                                               | 45.4 us: 1.20x slower                                 |
| deepcopy                  | 498 us                                                                | 602 us: 1.21x slower                                  |
| python_startup            | 23.5 ms                                                               | 29.3 ms: 1.25x slower                                 |
| mdp                       | 4.01 sec                                                              | 5.00 sec: 1.25x slower                                |
| async_generators          | 588 ms                                                                | 740 ms: 1.26x slower                                  |
| pylint                    | 466 ms                                                                | 591 ms: 1.27x slower                                  |
| docutils                  | 3.94 sec                                                              | 5.00 sec: 1.27x slower                                |
| pycparser                 | 1.71 sec                                                              | 2.23 sec: 1.30x slower                                |
| coverage                  | 121 ms                                                                | 157 ms: 1.31x slower                                  |
| json                      | 6.79 ms                                                               | 8.93 ms: 1.31x slower                                 |
| generators                | 40.7 ms                                                               | 53.8 ms: 1.32x slower                                 |
| tornado_http              | 253 ms                                                                | 337 ms: 1.33x slower                                  |
| json_dumps                | 13.9 ms                                                               | 18.6 ms: 1.34x slower                                 |
| xml_etree_generate        | 120 ms                                                                | 162 ms: 1.35x slower                                  |
| meteor_contest            | 156 ms                                                                | 212 ms: 1.35x slower                                  |
| deepcopy_reduce           | 4.31 us                                                               | 5.96 us: 1.38x slower                                 |
| scimark_fft               | 469 ms                                                                | 651 ms: 1.39x slower                                  |
| deepcopy_memo             | 50.9 us                                                               | 72.1 us: 1.42x slower                                 |
| scimark_sparse_mat_mult   | 6.84 ms                                                               | 9.98 ms: 1.46x slower                                 |
| bench_thread_pool         | 3.01 ms                                                               | 4.44 ms: 1.47x slower                                 |
| tomli_loads               | 2.84 sec                                                              | 4.21 sec: 1.48x slower                                |
| bpe_tokeniser             | 6.53 sec                                                              | 9.70 sec: 1.48x slower                                |
| nqueens                   | 108 ms                                                                | 161 ms: 1.49x slower                                  |
| coroutines                | 29.3 ms                                                               | 43.8 ms: 1.49x slower                                 |
| fannkuch                  | 535 ms                                                                | 806 ms: 1.51x slower                                  |
| 2to3                      | 441 ms                                                                | 666 ms: 1.51x slower                                  |
| crypto_pyaes              | 102 ms                                                                | 154 ms: 1.51x slower                                  |
| regex_compile             | 189 ms                                                                | 288 ms: 1.52x slower                                  |
| sympy_integrate           | 28.7 ms                                                               | 44.2 ms: 1.54x slower                                 |
| pyflate                   | 710 ms                                                                | 1.10 sec: 1.55x slower                                |
| sqlglot_optimize          | 77.9 ms                                                               | 122 ms: 1.56x slower                                  |
| sqlglot_normalize         | 150 ms                                                                | 237 ms: 1.58x slower                                  |
| xml_etree_process         | 82.2 ms                                                               | 132 ms: 1.60x slower                                  |
| spectral_norm             | 151 ms                                                                | 247 ms: 1.64x slower                                  |
| thrift                    | 1.09 ms                                                               | 1.78 ms: 1.64x slower                                 |
| logging_simple            | 9.16 us                                                               | 15.1 us: 1.65x slower                                 |
| float                     | 115 ms                                                                | 190 ms: 1.65x slower                                  |
| pprint_safe_repr          | 991 ms                                                                | 1.65 sec: 1.67x slower                                |
| richards                  | 68.8 ms                                                               | 116 ms: 1.69x slower                                  |
| pprint_pformat            | 2.04 sec                                                              | 3.44 sec: 1.69x slower                                |
| genshi_xml                | 71.9 ms                                                               | 123 ms: 1.71x slower                                  |
| richards_super            | 73.5 ms                                                               | 127 ms: 1.73x slower                                  |
| typing_runtime_protocols  | 222 us                                                                | 383 us: 1.73x slower                                  |
| html5lib                  | 92.0 ms                                                               | 162 ms: 1.76x slower                                  |
| django_template           | 46.1 ms                                                               | 81.9 ms: 1.78x slower                                 |
| genshi_text               | 31.6 ms                                                               | 56.5 ms: 1.79x slower                                 |
| pickle_pure_python        | 428 us                                                                | 764 us: 1.79x slower                                  |
| mako                      | 16.7 ms                                                               | 30.3 ms: 1.82x slower                                 |
| comprehensions            | 22.6 us                                                               | 41.9 us: 1.85x slower                                 |
| sympy_str                 | 376 ms                                                                | 698 ms: 1.85x slower                                  |
| unpickle_pure_python      | 285 us                                                                | 537 us: 1.88x slower                                  |
| scimark_monte_carlo       | 89.0 ms                                                               | 168 ms: 1.89x slower                                  |
| hexiom                    | 8.42 ms                                                               | 16.2 ms: 1.92x slower                                 |
| logging_silent            | 137 ns                                                                | 267 ns: 1.95x slower                                  |
| scimark_sor               | 176 ms                                                                | 347 ms: 1.97x slower                                  |
| sqlglot_parse             | 1.92 ms                                                               | 3.79 ms: 1.97x slower                                 |
| logging_format            | 9.36 us                                                               | 18.8 us: 2.01x slower                                 |
| sympy_expand              | 638 ms                                                                | 1.30 sec: 2.03x slower                                |
| sqlglot_transpile         | 2.24 ms                                                               | 4.65 ms: 2.07x slower                                 |
| sympy_sum                 | 226 ms                                                                | 470 ms: 2.08x slower                                  |
| chaos                     | 81.5 ms                                                               | 179 ms: 2.19x slower                                  |
| scimark_lu                | 150 ms                                                                | 336 ms: 2.24x slower                                  |
| raytrace                  | 351 ms                                                                | 800 ms: 2.28x slower                                  |
| go                        | 193 ms                                                                | 457 ms: 2.36x slower                                  |
| nbody                     | 126 ms                                                                | 309 ms: 2.46x slower                                  |
| deltablue                 | 4.55 ms                                                               | 11.9 ms: 2.61x slower                                 |
| unpack_sequence           | 54.6 ns                                                               | 217 ns: 3.97x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.38x slower                                          |

Benchmark hidden because not significant (6): async_tree_memoization, regex_v8, asyncio_websockets, xml_etree_parse, xml_etree_iterparse, async_tree_cpu_io_mixed_tg
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.15x