# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 8145ebe
- commit date: 2024-09-12
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 669 ms: 1.52x slower                                  |
| docutils       | 3.94 sec                                                              | 4.89 sec: 1.24x slower                                |
| html5lib       | 92.0 ms                                                               | 133 ms: 1.45x slower                                  |
| tornado_http   | 253 ms                                                                | 374 ms: 1.48x slower                                  |
| Geometric mean | (ref)                                                                 | 1.42x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg          | 1.43 sec                                                              | 1.17 sec: 1.23x faster                                |
| async_tree_io             | 1.39 sec                                                              | 1.24 sec: 1.12x faster                                |
| async_tree_memoization_tg | 692 ms                                                                | 651 ms: 1.06x faster                                  |
| async_tree_none_tg        | 526 ms                                                                | 497 ms: 1.06x faster                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 948 ms: 1.06x slower                                  |
| asyncio_websockets        | 728 ms                                                                | 802 ms: 1.10x slower                                  |
| asyncio_tcp               | 972 ms                                                                | 1.10 sec: 1.13x slower                                |
| async_tree_none           | 523 ms                                                                | 609 ms: 1.17x slower                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.36 sec: 1.19x slower                                |
| async_generators          | 588 ms                                                                | 742 ms: 1.26x slower                                  |
| coroutines                | 29.3 ms                                                               | 44.4 ms: 1.51x slower                                 |
| Geometric mean            | (ref)                                                                 | 1.06x slower                                          |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                                                | 247 ms: 1.03x faster                                  |
| float          | 115 ms                                                                | 196 ms: 1.70x slower                                  |
| nbody          | 126 ms                                                                | 281 ms: 2.24x slower                                  |
| Geometric mean | (ref)                                                                 | 1.55x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.63 ms                                                               | 4.42 ms: 1.05x faster                                 |
| regex_compile  | 189 ms                                                                | 288 ms: 1.52x slower                                  |
| Geometric mean | (ref)                                                                 | 1.10x slower                                          |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.85 us: 1.09x faster                                 |
| xml_etree_iterparse  | 163 ms                                                                | 175 ms: 1.08x slower                                  |
| json_loads           | 37.9 us                                                               | 41.7 us: 1.10x slower                                 |
| unpickle_list        | 6.78 us                                                               | 7.64 us: 1.13x slower                                 |
| json_dumps           | 13.9 ms                                                               | 17.8 ms: 1.28x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 170 ms: 1.42x slower                                  |
| tomli_loads          | 2.84 sec                                                              | 4.34 sec: 1.53x slower                                |
| xml_etree_process    | 82.2 ms                                                               | 126 ms: 1.53x slower                                  |
| unpickle_pure_python | 285 us                                                                | 516 us: 1.81x slower                                  |
| pickle_pure_python   | 428 us                                                                | 847 us: 1.98x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.23x slower                                          |

Benchmark hidden because not significant (4): pickle_dict, pickle, unpickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 21.3 ms: 1.33x slower                                 |
| python_startup         | 23.5 ms                                                               | 32.2 ms: 1.37x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.35x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 118 ms: 1.64x slower                                  |
| django_template | 46.1 ms                                                               | 85.0 ms: 1.84x slower                                 |
| mako            | 16.7 ms                                                               | 31.6 ms: 1.90x slower                                 |
| genshi_text     | 31.6 ms                                                               | 60.8 ms: 1.92x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.82x slower                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                     | 229 ms                                                                | 13.9 ms: 16.49x faster                                |
| async_tree_io_tg          | 1.43 sec                                                              | 1.17 sec: 1.23x faster                                |
| create_gc_cycles          | 2.49 ms                                                               | 2.04 ms: 1.22x faster                                 |
| gc_traversal              | 5.80 ms                                                               | 4.89 ms: 1.19x faster                                 |
| async_tree_io             | 1.39 sec                                                              | 1.24 sec: 1.12x faster                                |
| pickle_list               | 7.48 us                                                               | 6.85 us: 1.09x faster                                 |
| async_tree_memoization_tg | 692 ms                                                                | 651 ms: 1.06x faster                                  |
| async_tree_none_tg        | 526 ms                                                                | 497 ms: 1.06x faster                                  |
| regex_effbot              | 4.63 ms                                                               | 4.42 ms: 1.05x faster                                 |
| pidigits                  | 256 ms                                                                | 247 ms: 1.03x faster                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 948 ms: 1.06x slower                                  |
| xml_etree_iterparse       | 163 ms                                                                | 175 ms: 1.08x slower                                  |
| asyncio_websockets        | 728 ms                                                                | 802 ms: 1.10x slower                                  |
| json_loads                | 37.9 us                                                               | 41.7 us: 1.10x slower                                 |
| pathlib                   | 31.8 ms                                                               | 35.3 ms: 1.11x slower                                 |
| sqlite_synth              | 3.94 us                                                               | 4.43 us: 1.12x slower                                 |
| unpickle_list             | 6.78 us                                                               | 7.64 us: 1.13x slower                                 |
| asyncio_tcp               | 972 ms                                                                | 1.10 sec: 1.13x slower                                |
| deepcopy                  | 498 us                                                                | 581 us: 1.17x slower                                  |
| async_tree_none           | 523 ms                                                                | 609 ms: 1.17x slower                                  |
| json                      | 6.79 ms                                                               | 8.00 ms: 1.18x slower                                 |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.36 sec: 1.19x slower                                |
| docutils                  | 3.94 sec                                                              | 4.89 sec: 1.24x slower                                |
| async_generators          | 588 ms                                                                | 742 ms: 1.26x slower                                  |
| json_dumps                | 13.9 ms                                                               | 17.8 ms: 1.28x slower                                 |
| coverage                  | 121 ms                                                                | 156 ms: 1.29x slower                                  |
| generators                | 40.7 ms                                                               | 52.8 ms: 1.30x slower                                 |
| mdp                       | 4.01 sec                                                              | 5.21 sec: 1.30x slower                                |
| scimark_sparse_mat_mult   | 6.84 ms                                                               | 8.92 ms: 1.30x slower                                 |
| pylint                    | 466 ms                                                                | 610 ms: 1.31x slower                                  |
| pycparser                 | 1.71 sec                                                              | 2.24 sec: 1.31x slower                                |
| meteor_contest            | 156 ms                                                                | 208 ms: 1.33x slower                                  |
| python_startup_no_site    | 16.0 ms                                                               | 21.3 ms: 1.33x slower                                 |
| scimark_fft               | 469 ms                                                                | 631 ms: 1.34x slower                                  |
| deepcopy_memo             | 50.9 us                                                               | 68.8 us: 1.35x slower                                 |
| python_startup            | 23.5 ms                                                               | 32.2 ms: 1.37x slower                                 |
| deepcopy_reduce           | 4.31 us                                                               | 5.91 us: 1.37x slower                                 |
| xml_etree_generate        | 120 ms                                                                | 170 ms: 1.42x slower                                  |
| fannkuch                  | 535 ms                                                                | 767 ms: 1.43x slower                                  |
| nqueens                   | 108 ms                                                                | 155 ms: 1.43x slower                                  |
| html5lib                  | 92.0 ms                                                               | 133 ms: 1.45x slower                                  |
| pyflate                   | 710 ms                                                                | 1.04 sec: 1.46x slower                                |
| tornado_http              | 253 ms                                                                | 374 ms: 1.48x slower                                  |
| crypto_pyaes              | 102 ms                                                                | 151 ms: 1.48x slower                                  |
| typing_runtime_protocols  | 222 us                                                                | 334 us: 1.51x slower                                  |
| sqlglot_optimize          | 77.9 ms                                                               | 117 ms: 1.51x slower                                  |
| coroutines                | 29.3 ms                                                               | 44.4 ms: 1.51x slower                                 |
| 2to3                      | 441 ms                                                                | 669 ms: 1.52x slower                                  |
| regex_compile             | 189 ms                                                                | 288 ms: 1.52x slower                                  |
| tomli_loads               | 2.84 sec                                                              | 4.34 sec: 1.53x slower                                |
| xml_etree_process         | 82.2 ms                                                               | 126 ms: 1.53x slower                                  |
| bpe_tokeniser             | 6.53 sec                                                              | 10.2 sec: 1.57x slower                                |
| richards                  | 68.8 ms                                                               | 108 ms: 1.57x slower                                  |
| thrift                    | 1.09 ms                                                               | 1.71 ms: 1.57x slower                                 |
| bench_thread_pool         | 3.01 ms                                                               | 4.74 ms: 1.58x slower                                 |
| sympy_integrate           | 28.7 ms                                                               | 46.3 ms: 1.61x slower                                 |
| spectral_norm             | 151 ms                                                                | 245 ms: 1.62x slower                                  |
| dulwich_log               | 97.5 ms                                                               | 159 ms: 1.63x slower                                  |
| genshi_xml                | 71.9 ms                                                               | 118 ms: 1.64x slower                                  |
| comprehensions            | 22.6 us                                                               | 37.2 us: 1.64x slower                                 |
| logging_simple            | 9.16 us                                                               | 15.2 us: 1.66x slower                                 |
| sqlglot_normalize         | 150 ms                                                                | 250 ms: 1.66x slower                                  |
| richards_super            | 73.5 ms                                                               | 123 ms: 1.68x slower                                  |
| pprint_safe_repr          | 991 ms                                                                | 1.69 sec: 1.70x slower                                |
| float                     | 115 ms                                                                | 196 ms: 1.70x slower                                  |
| pprint_pformat            | 2.04 sec                                                              | 3.52 sec: 1.73x slower                                |
| logging_format            | 9.36 us                                                               | 16.3 us: 1.74x slower                                 |
| unpickle_pure_python      | 285 us                                                                | 516 us: 1.81x slower                                  |
| sympy_str                 | 376 ms                                                                | 687 ms: 1.82x slower                                  |
| django_template           | 46.1 ms                                                               | 85.0 ms: 1.84x slower                                 |
| go                        | 193 ms                                                                | 361 ms: 1.87x slower                                  |
| scimark_monte_carlo       | 89.0 ms                                                               | 166 ms: 1.87x slower                                  |
| logging_silent            | 137 ns                                                                | 256 ns: 1.87x slower                                  |
| mako                      | 16.7 ms                                                               | 31.6 ms: 1.90x slower                                 |
| hexiom                    | 8.42 ms                                                               | 16.0 ms: 1.90x slower                                 |
| genshi_text               | 31.6 ms                                                               | 60.8 ms: 1.92x slower                                 |
| scimark_sor               | 176 ms                                                                | 345 ms: 1.96x slower                                  |
| chaos                     | 81.5 ms                                                               | 159 ms: 1.96x slower                                  |
| sqlglot_transpile         | 2.24 ms                                                               | 4.40 ms: 1.96x slower                                 |
| pickle_pure_python        | 428 us                                                                | 847 us: 1.98x slower                                  |
| sqlglot_parse             | 1.92 ms                                                               | 3.90 ms: 2.03x slower                                 |
| scimark_lu                | 150 ms                                                                | 307 ms: 2.05x slower                                  |
| sympy_expand              | 638 ms                                                                | 1.33 sec: 2.08x slower                                |
| sympy_sum                 | 226 ms                                                                | 491 ms: 2.17x slower                                  |
| raytrace                  | 351 ms                                                                | 766 ms: 2.18x slower                                  |
| nbody                     | 126 ms                                                                | 281 ms: 2.24x slower                                  |
| deltablue                 | 4.55 ms                                                               | 11.6 ms: 2.56x slower                                 |
| unpack_sequence           | 54.6 ns                                                               | 201 ns: 3.68x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.36x slower                                          |

Benchmark hidden because not significant (9): bench_mp_pool, async_tree_cpu_io_mixed_tg, async_tree_memoization, pickle_dict, pickle, regex_dna, regex_v8, unpickle, xml_etree_parse
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.15x