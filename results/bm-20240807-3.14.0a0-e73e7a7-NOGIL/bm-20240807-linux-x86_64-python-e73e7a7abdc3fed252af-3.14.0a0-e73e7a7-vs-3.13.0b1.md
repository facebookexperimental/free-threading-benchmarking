# Results vs. 3.13.0b1

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.34x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 651 ms: 1.47x slower                                                  |
| docutils       | 3.94 sec                                                              | 4.92 sec: 1.25x slower                                                |
| html5lib       | 92.0 ms                                                               | 137 ms: 1.49x slower                                                  |
| tornado_http   | 253 ms                                                                | 319 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.36x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|---------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg          | 1.43 sec                                                              | 1.12 sec: 1.28x faster                                                |
| async_tree_memoization_tg | 692 ms                                                                | 619 ms: 1.12x faster                                                  |
| async_tree_io             | 1.39 sec                                                              | 1.25 sec: 1.11x faster                                                |
| async_tree_none_tg        | 526 ms                                                                | 489 ms: 1.08x faster                                                  |
| async_tree_memoization    | 775 ms                                                                | 724 ms: 1.07x faster                                                  |
| asyncio_websockets        | 728 ms                                                                | 766 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 951 ms: 1.06x slower                                                  |
| async_tree_none           | 523 ms                                                                | 584 ms: 1.12x slower                                                  |
| asyncio_tcp               | 972 ms                                                                | 1.09 sec: 1.12x slower                                                |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.34 sec: 1.18x slower                                                |
| async_generators          | 588 ms                                                                | 747 ms: 1.27x slower                                                  |
| coroutines                | 29.3 ms                                                               | 42.7 ms: 1.46x slower                                                 |
| Geometric mean            | (ref)                                                                 | 1.04x slower                                                          |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 256 ms                                                                | 239 ms: 1.07x faster                                                  |
| float          | 115 ms                                                                | 194 ms: 1.69x slower                                                  |
| nbody          | 126 ms                                                                | 281 ms: 2.24x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.52x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.63 ms                                                               | 4.84 ms: 1.05x slower                                                 |
| regex_compile  | 189 ms                                                                | 296 ms: 1.56x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                          |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.90 us: 1.08x faster                                                 |
| pickle_dict          | 46.5 us                                                               | 43.1 us: 1.08x faster                                                 |
| pickle               | 15.2 us                                                               | 14.5 us: 1.05x faster                                                 |
| json_loads           | 37.9 us                                                               | 41.2 us: 1.09x slower                                                 |
| unpickle_list        | 6.78 us                                                               | 7.70 us: 1.14x slower                                                 |
| json_dumps           | 13.9 ms                                                               | 18.0 ms: 1.29x slower                                                 |
| xml_etree_generate   | 120 ms                                                                | 159 ms: 1.33x slower                                                  |
| tomli_loads          | 2.84 sec                                                              | 4.14 sec: 1.46x slower                                                |
| xml_etree_process    | 82.2 ms                                                               | 127 ms: 1.54x slower                                                  |
| unpickle_pure_python | 285 us                                                                | 544 us: 1.91x slower                                                  |
| pickle_pure_python   | 428 us                                                                | 846 us: 1.98x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.22x slower                                                          |

Benchmark hidden because not significant (3): unpickle, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 19.4 ms: 1.21x slower                                                 |
| python_startup         | 23.5 ms                                                               | 28.9 ms: 1.23x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.22x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 111 ms: 1.55x slower                                                  |
| genshi_text     | 31.6 ms                                                               | 53.4 ms: 1.69x slower                                                 |
| django_template | 46.1 ms                                                               | 79.6 ms: 1.73x slower                                                 |
| mako            | 16.7 ms                                                               | 31.0 ms: 1.86x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.70x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|---------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| telco                     | 229 ms                                                                | 14.0 ms: 16.35x faster                                                |
| gc_traversal              | 5.80 ms                                                               | 4.19 ms: 1.39x faster                                                 |
| create_gc_cycles          | 2.49 ms                                                               | 1.80 ms: 1.38x faster                                                 |
| async_tree_io_tg          | 1.43 sec                                                              | 1.12 sec: 1.28x faster                                                |
| async_tree_memoization_tg | 692 ms                                                                | 619 ms: 1.12x faster                                                  |
| async_tree_io             | 1.39 sec                                                              | 1.25 sec: 1.11x faster                                                |
| pickle_list               | 7.48 us                                                               | 6.90 us: 1.08x faster                                                 |
| pickle_dict               | 46.5 us                                                               | 43.1 us: 1.08x faster                                                 |
| async_tree_none_tg        | 526 ms                                                                | 489 ms: 1.08x faster                                                  |
| async_tree_memoization    | 775 ms                                                                | 724 ms: 1.07x faster                                                  |
| pidigits                  | 256 ms                                                                | 239 ms: 1.07x faster                                                  |
| pickle                    | 15.2 us                                                               | 14.5 us: 1.05x faster                                                 |
| regex_effbot              | 4.63 ms                                                               | 4.84 ms: 1.05x slower                                                 |
| asyncio_websockets        | 728 ms                                                                | 766 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 951 ms: 1.06x slower                                                  |
| json_loads                | 37.9 us                                                               | 41.2 us: 1.09x slower                                                 |
| async_tree_none           | 523 ms                                                                | 584 ms: 1.12x slower                                                  |
| sqlite_synth              | 3.94 us                                                               | 4.42 us: 1.12x slower                                                 |
| asyncio_tcp               | 972 ms                                                                | 1.09 sec: 1.12x slower                                                |
| deepcopy                  | 498 us                                                                | 560 us: 1.12x slower                                                  |
| unpickle_list             | 6.78 us                                                               | 7.70 us: 1.14x slower                                                 |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.34 sec: 1.18x slower                                                |
| json                      | 6.79 ms                                                               | 8.10 ms: 1.19x slower                                                 |
| coverage                  | 121 ms                                                                | 146 ms: 1.21x slower                                                  |
| python_startup_no_site    | 16.0 ms                                                               | 19.4 ms: 1.21x slower                                                 |
| python_startup            | 23.5 ms                                                               | 28.9 ms: 1.23x slower                                                 |
| meteor_contest            | 156 ms                                                                | 192 ms: 1.23x slower                                                  |
| pylint                    | 466 ms                                                                | 579 ms: 1.24x slower                                                  |
| docutils                  | 3.94 sec                                                              | 4.92 sec: 1.25x slower                                                |
| tornado_http              | 253 ms                                                                | 319 ms: 1.26x slower                                                  |
| async_generators          | 588 ms                                                                | 747 ms: 1.27x slower                                                  |
| mdp                       | 4.01 sec                                                              | 5.13 sec: 1.28x slower                                                |
| json_dumps                | 13.9 ms                                                               | 18.0 ms: 1.29x slower                                                 |
| pycparser                 | 1.71 sec                                                              | 2.21 sec: 1.30x slower                                                |
| scimark_sparse_mat_mult   | 6.84 ms                                                               | 8.91 ms: 1.30x slower                                                 |
| deepcopy_memo             | 50.9 us                                                               | 67.1 us: 1.32x slower                                                 |
| deepcopy_reduce           | 4.31 us                                                               | 5.70 us: 1.32x slower                                                 |
| xml_etree_generate        | 120 ms                                                                | 159 ms: 1.33x slower                                                  |
| scimark_fft               | 469 ms                                                                | 624 ms: 1.33x slower                                                  |
| generators                | 40.7 ms                                                               | 55.0 ms: 1.35x slower                                                 |
| fannkuch                  | 535 ms                                                                | 762 ms: 1.42x slower                                                  |
| nqueens                   | 108 ms                                                                | 155 ms: 1.43x slower                                                  |
| richards                  | 68.8 ms                                                               | 99.2 ms: 1.44x slower                                                 |
| coroutines                | 29.3 ms                                                               | 42.7 ms: 1.46x slower                                                 |
| tomli_loads               | 2.84 sec                                                              | 4.14 sec: 1.46x slower                                                |
| 2to3                      | 441 ms                                                                | 651 ms: 1.47x slower                                                  |
| typing_runtime_protocols  | 222 us                                                                | 327 us: 1.48x slower                                                  |
| html5lib                  | 92.0 ms                                                               | 137 ms: 1.49x slower                                                  |
| pyflate                   | 710 ms                                                                | 1.07 sec: 1.50x slower                                                |
| bench_thread_pool         | 3.01 ms                                                               | 4.52 ms: 1.50x slower                                                 |
| sqlglot_normalize         | 150 ms                                                                | 229 ms: 1.52x slower                                                  |
| crypto_pyaes              | 102 ms                                                                | 156 ms: 1.53x slower                                                  |
| thrift                    | 1.09 ms                                                               | 1.67 ms: 1.54x slower                                                 |
| xml_etree_process         | 82.2 ms                                                               | 127 ms: 1.54x slower                                                  |
| genshi_xml                | 71.9 ms                                                               | 111 ms: 1.55x slower                                                  |
| bpe_tokeniser             | 6.53 sec                                                              | 10.1 sec: 1.55x slower                                                |
| sqlglot_optimize          | 77.9 ms                                                               | 121 ms: 1.55x slower                                                  |
| regex_compile             | 189 ms                                                                | 296 ms: 1.56x slower                                                  |
| sympy_integrate           | 28.7 ms                                                               | 44.9 ms: 1.56x slower                                                 |
| spectral_norm             | 151 ms                                                                | 247 ms: 1.64x slower                                                  |
| pprint_pformat            | 2.04 sec                                                              | 3.39 sec: 1.66x slower                                                |
| pprint_safe_repr          | 991 ms                                                                | 1.65 sec: 1.67x slower                                                |
| logging_simple            | 9.16 us                                                               | 15.4 us: 1.68x slower                                                 |
| float                     | 115 ms                                                                | 194 ms: 1.69x slower                                                  |
| genshi_text               | 31.6 ms                                                               | 53.4 ms: 1.69x slower                                                 |
| comprehensions            | 22.6 us                                                               | 38.7 us: 1.71x slower                                                 |
| django_template           | 46.1 ms                                                               | 79.6 ms: 1.73x slower                                                 |
| richards_super            | 73.5 ms                                                               | 127 ms: 1.73x slower                                                  |
| logging_format            | 9.36 us                                                               | 16.4 us: 1.75x slower                                                 |
| scimark_monte_carlo       | 89.0 ms                                                               | 159 ms: 1.79x slower                                                  |
| sympy_str                 | 376 ms                                                                | 675 ms: 1.79x slower                                                  |
| logging_silent            | 137 ns                                                                | 249 ns: 1.82x slower                                                  |
| mako                      | 16.7 ms                                                               | 31.0 ms: 1.86x slower                                                 |
| unpickle_pure_python      | 285 us                                                                | 544 us: 1.91x slower                                                  |
| sqlglot_transpile         | 2.24 ms                                                               | 4.32 ms: 1.93x slower                                                 |
| scimark_sor               | 176 ms                                                                | 340 ms: 1.93x slower                                                  |
| hexiom                    | 8.42 ms                                                               | 16.3 ms: 1.94x slower                                                 |
| sympy_sum                 | 226 ms                                                                | 443 ms: 1.96x slower                                                  |
| sqlglot_parse             | 1.92 ms                                                               | 3.76 ms: 1.96x slower                                                 |
| pickle_pure_python        | 428 us                                                                | 846 us: 1.98x slower                                                  |
| sympy_expand              | 638 ms                                                                | 1.29 sec: 2.01x slower                                                |
| chaos                     | 81.5 ms                                                               | 170 ms: 2.09x slower                                                  |
| scimark_lu                | 150 ms                                                                | 313 ms: 2.09x slower                                                  |
| nbody                     | 126 ms                                                                | 281 ms: 2.24x slower                                                  |
| go                        | 193 ms                                                                | 434 ms: 2.25x slower                                                  |
| raytrace                  | 351 ms                                                                | 801 ms: 2.28x slower                                                  |
| deltablue                 | 4.55 ms                                                               | 11.6 ms: 2.55x slower                                                 |
| unpack_sequence           | 54.6 ns                                                               | 190 ns: 3.48x slower                                                  |
| Geometric mean            | (ref)                                                                 | 1.34x slower                                                          |

Benchmark hidden because not significant (8): bench_mp_pool, regex_v8, async_tree_cpu_io_mixed_tg, unpickle, xml_etree_parse, regex_dna, xml_etree_iterparse, pathlib
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.15x