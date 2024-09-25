# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4606eff
- commit date: 2024-07-23
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 664 ms: 1.50x slower                                  |
| docutils       | 3.94 sec                                                              | 4.86 sec: 1.23x slower                                |
| html5lib       | 92.0 ms                                                               | 157 ms: 1.70x slower                                  |
| tornado_http   | 253 ms                                                                | 320 ms: 1.27x slower                                  |
| Geometric mean | (ref)                                                                 | 1.41x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg          | 1.43 sec                                                              | 1.17 sec: 1.23x faster                                |
| async_tree_io             | 1.39 sec                                                              | 1.22 sec: 1.14x faster                                |
| async_tree_none_tg        | 526 ms                                                                | 493 ms: 1.07x faster                                  |
| async_tree_memoization_tg | 692 ms                                                                | 654 ms: 1.06x faster                                  |
| async_tree_memoization    | 775 ms                                                                | 733 ms: 1.06x faster                                  |
| asyncio_websockets        | 728 ms                                                                | 750 ms: 1.03x slower                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 945 ms: 1.05x slower                                  |
| async_tree_none           | 523 ms                                                                | 593 ms: 1.13x slower                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.27 sec: 1.16x slower                                |
| asyncio_tcp               | 972 ms                                                                | 1.12 sec: 1.16x slower                                |
| async_generators          | 588 ms                                                                | 724 ms: 1.23x slower                                  |
| coroutines                | 29.3 ms                                                               | 45.6 ms: 1.56x slower                                 |
| Geometric mean            | (ref)                                                                 | 1.05x slower                                          |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                                                | 243 ms: 1.05x faster                                  |
| float          | 115 ms                                                                | 200 ms: 1.74x slower                                  |
| nbody          | 126 ms                                                                | 283 ms: 2.25x slower                                  |
| Geometric mean | (ref)                                                                 | 1.55x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 37.1 ms                                                               | 33.7 ms: 1.10x faster                                 |
| regex_effbot   | 4.63 ms                                                               | 4.80 ms: 1.04x slower                                 |
| regex_dna      | 284 ms                                                                | 301 ms: 1.06x slower                                  |
| regex_compile  | 189 ms                                                                | 292 ms: 1.54x slower                                  |
| Geometric mean | (ref)                                                                 | 1.11x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.45 us: 1.16x faster                                 |
| pickle_dict          | 46.5 us                                                               | 42.9 us: 1.08x faster                                 |
| pickle               | 15.2 us                                                               | 14.3 us: 1.07x faster                                 |
| unpickle_list        | 6.78 us                                                               | 7.21 us: 1.06x slower                                 |
| json_loads           | 37.9 us                                                               | 45.2 us: 1.19x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 158 ms: 1.32x slower                                  |
| json_dumps           | 13.9 ms                                                               | 18.9 ms: 1.36x slower                                 |
| tomli_loads          | 2.84 sec                                                              | 4.14 sec: 1.46x slower                                |
| xml_etree_process    | 82.2 ms                                                               | 124 ms: 1.50x slower                                  |
| pickle_pure_python   | 428 us                                                                | 760 us: 1.78x slower                                  |
| unpickle_pure_python | 285 us                                                                | 540 us: 1.89x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.19x slower                                          |

Benchmark hidden because not significant (3): unpickle, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 29.5 ms: 1.25x slower                                 |
| python_startup_no_site | 16.0 ms                                                               | 20.9 ms: 1.31x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.28x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 122 ms: 1.70x slower                                  |
| genshi_text     | 31.6 ms                                                               | 55.7 ms: 1.76x slower                                 |
| django_template | 46.1 ms                                                               | 84.5 ms: 1.83x slower                                 |
| mako            | 16.7 ms                                                               | 31.9 ms: 1.91x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.80x slower                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                     | 229 ms                                                                | 13.4 ms: 17.13x faster                                |
| bench_mp_pool             | 19.7 ms                                                               | 13.3 ms: 1.48x faster                                 |
| create_gc_cycles          | 2.49 ms                                                               | 1.82 ms: 1.36x faster                                 |
| gc_traversal              | 5.80 ms                                                               | 4.60 ms: 1.26x faster                                 |
| async_tree_io_tg          | 1.43 sec                                                              | 1.17 sec: 1.23x faster                                |
| pickle_list               | 7.48 us                                                               | 6.45 us: 1.16x faster                                 |
| async_tree_io             | 1.39 sec                                                              | 1.22 sec: 1.14x faster                                |
| regex_v8                  | 37.1 ms                                                               | 33.7 ms: 1.10x faster                                 |
| pickle_dict               | 46.5 us                                                               | 42.9 us: 1.08x faster                                 |
| pickle                    | 15.2 us                                                               | 14.3 us: 1.07x faster                                 |
| async_tree_none_tg        | 526 ms                                                                | 493 ms: 1.07x faster                                  |
| async_tree_memoization_tg | 692 ms                                                                | 654 ms: 1.06x faster                                  |
| async_tree_memoization    | 775 ms                                                                | 733 ms: 1.06x faster                                  |
| pidigits                  | 256 ms                                                                | 243 ms: 1.05x faster                                  |
| asyncio_websockets        | 728 ms                                                                | 750 ms: 1.03x slower                                  |
| regex_effbot              | 4.63 ms                                                               | 4.80 ms: 1.04x slower                                 |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 945 ms: 1.05x slower                                  |
| regex_dna                 | 284 ms                                                                | 301 ms: 1.06x slower                                  |
| unpickle_list             | 6.78 us                                                               | 7.21 us: 1.06x slower                                 |
| sqlite_synth              | 3.94 us                                                               | 4.23 us: 1.07x slower                                 |
| async_tree_none           | 523 ms                                                                | 593 ms: 1.13x slower                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.27 sec: 1.16x slower                                |
| asyncio_tcp               | 972 ms                                                                | 1.12 sec: 1.16x slower                                |
| deepcopy                  | 498 us                                                                | 594 us: 1.19x slower                                  |
| json_loads                | 37.9 us                                                               | 45.2 us: 1.19x slower                                 |
| async_generators          | 588 ms                                                                | 724 ms: 1.23x slower                                  |
| docutils                  | 3.94 sec                                                              | 4.86 sec: 1.23x slower                                |
| pylint                    | 466 ms                                                                | 582 ms: 1.25x slower                                  |
| python_startup            | 23.5 ms                                                               | 29.5 ms: 1.25x slower                                 |
| coverage                  | 121 ms                                                                | 151 ms: 1.26x slower                                  |
| tornado_http              | 253 ms                                                                | 320 ms: 1.27x slower                                  |
| pycparser                 | 1.71 sec                                                              | 2.16 sec: 1.27x slower                                |
| json                      | 6.79 ms                                                               | 8.61 ms: 1.27x slower                                 |
| meteor_contest            | 156 ms                                                                | 199 ms: 1.27x slower                                  |
| scimark_sparse_mat_mult   | 6.84 ms                                                               | 8.70 ms: 1.27x slower                                 |
| mdp                       | 4.01 sec                                                              | 5.10 sec: 1.27x slower                                |
| python_startup_no_site    | 16.0 ms                                                               | 20.9 ms: 1.31x slower                                 |
| scimark_fft               | 469 ms                                                                | 617 ms: 1.31x slower                                  |
| xml_etree_generate        | 120 ms                                                                | 158 ms: 1.32x slower                                  |
| bench_thread_pool         | 3.01 ms                                                               | 4.01 ms: 1.33x slower                                 |
| generators                | 40.7 ms                                                               | 54.9 ms: 1.35x slower                                 |
| json_dumps                | 13.9 ms                                                               | 18.9 ms: 1.36x slower                                 |
| deepcopy_reduce           | 4.31 us                                                               | 5.85 us: 1.36x slower                                 |
| deepcopy_memo             | 50.9 us                                                               | 69.7 us: 1.37x slower                                 |
| nqueens                   | 108 ms                                                                | 152 ms: 1.40x slower                                  |
| dulwich_log               | 97.5 ms                                                               | 140 ms: 1.43x slower                                  |
| tomli_loads               | 2.84 sec                                                              | 4.14 sec: 1.46x slower                                |
| fannkuch                  | 535 ms                                                                | 783 ms: 1.46x slower                                  |
| xml_etree_process         | 82.2 ms                                                               | 124 ms: 1.50x slower                                  |
| 2to3                      | 441 ms                                                                | 664 ms: 1.50x slower                                  |
| sympy_integrate           | 28.7 ms                                                               | 43.9 ms: 1.53x slower                                 |
| sqlglot_normalize         | 150 ms                                                                | 230 ms: 1.53x slower                                  |
| regex_compile             | 189 ms                                                                | 292 ms: 1.54x slower                                  |
| typing_runtime_protocols  | 222 us                                                                | 342 us: 1.54x slower                                  |
| bpe_tokeniser             | 6.53 sec                                                              | 10.1 sec: 1.55x slower                                |
| crypto_pyaes              | 102 ms                                                                | 157 ms: 1.55x slower                                  |
| coroutines                | 29.3 ms                                                               | 45.6 ms: 1.56x slower                                 |
| pyflate                   | 710 ms                                                                | 1.13 sec: 1.59x slower                                |
| sqlglot_optimize          | 77.9 ms                                                               | 124 ms: 1.59x slower                                  |
| thrift                    | 1.09 ms                                                               | 1.75 ms: 1.61x slower                                 |
| richards                  | 68.8 ms                                                               | 112 ms: 1.62x slower                                  |
| spectral_norm             | 151 ms                                                                | 247 ms: 1.64x slower                                  |
| logging_simple            | 9.16 us                                                               | 15.2 us: 1.66x slower                                 |
| comprehensions            | 22.6 us                                                               | 38.3 us: 1.69x slower                                 |
| genshi_xml                | 71.9 ms                                                               | 122 ms: 1.70x slower                                  |
| html5lib                  | 92.0 ms                                                               | 157 ms: 1.70x slower                                  |
| pprint_safe_repr          | 991 ms                                                                | 1.71 sec: 1.73x slower                                |
| float                     | 115 ms                                                                | 200 ms: 1.74x slower                                  |
| pprint_pformat            | 2.04 sec                                                              | 3.55 sec: 1.74x slower                                |
| genshi_text               | 31.6 ms                                                               | 55.7 ms: 1.76x slower                                 |
| logging_format            | 9.36 us                                                               | 16.6 us: 1.78x slower                                 |
| pickle_pure_python        | 428 us                                                                | 760 us: 1.78x slower                                  |
| logging_silent            | 137 ns                                                                | 246 ns: 1.80x slower                                  |
| richards_super            | 73.5 ms                                                               | 133 ms: 1.81x slower                                  |
| sympy_str                 | 376 ms                                                                | 685 ms: 1.82x slower                                  |
| scimark_monte_carlo       | 89.0 ms                                                               | 163 ms: 1.83x slower                                  |
| django_template           | 46.1 ms                                                               | 84.5 ms: 1.83x slower                                 |
| unpickle_pure_python      | 285 us                                                                | 540 us: 1.89x slower                                  |
| mako                      | 16.7 ms                                                               | 31.9 ms: 1.91x slower                                 |
| scimark_sor               | 176 ms                                                                | 341 ms: 1.93x slower                                  |
| hexiom                    | 8.42 ms                                                               | 16.7 ms: 1.99x slower                                 |
| sympy_expand              | 638 ms                                                                | 1.27 sec: 1.99x slower                                |
| sqlglot_transpile         | 2.24 ms                                                               | 4.58 ms: 2.04x slower                                 |
| sqlglot_parse             | 1.92 ms                                                               | 3.99 ms: 2.08x slower                                 |
| scimark_lu                | 150 ms                                                                | 314 ms: 2.09x slower                                  |
| sympy_sum                 | 226 ms                                                                | 476 ms: 2.10x slower                                  |
| go                        | 193 ms                                                                | 411 ms: 2.12x slower                                  |
| chaos                     | 81.5 ms                                                               | 175 ms: 2.15x slower                                  |
| nbody                     | 126 ms                                                                | 283 ms: 2.25x slower                                  |
| raytrace                  | 351 ms                                                                | 807 ms: 2.30x slower                                  |
| deltablue                 | 4.55 ms                                                               | 11.4 ms: 2.51x slower                                 |
| unpack_sequence           | 54.6 ns                                                               | 200 ns: 3.67x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.35x slower                                          |

Benchmark hidden because not significant (5): unpickle, async_tree_cpu_io_mixed_tg, xml_etree_parse, xml_etree_iterparse, pathlib
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.15x