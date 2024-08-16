# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.31x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 661 ms: 1.50x slower                                  |
| docutils       | 3.94 sec                                                              | 4.69 sec: 1.19x slower                                |
| html5lib       | 92.0 ms                                                               | 135 ms: 1.47x slower                                  |
| tornado_http   | 253 ms                                                                | 320 ms: 1.27x slower                                  |
| Geometric mean | (ref)                                                                 | 1.35x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.43 sec                                                              | 1.15 sec: 1.25x faster                                |
| async_tree_io              | 1.39 sec                                                              | 1.25 sec: 1.12x faster                                |
| async_tree_none_tg         | 526 ms                                                                | 479 ms: 1.10x faster                                  |
| async_tree_memoization_tg  | 692 ms                                                                | 632 ms: 1.10x faster                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 806 ms: 1.09x faster                                  |
| async_tree_memoization     | 775 ms                                                                | 728 ms: 1.07x faster                                  |
| asyncio_tcp                | 972 ms                                                                | 1.05 sec: 1.08x slower                                |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.12 sec: 1.10x slower                                |
| async_tree_none            | 523 ms                                                                | 578 ms: 1.11x slower                                  |
| async_generators           | 588 ms                                                                | 739 ms: 1.26x slower                                  |
| coroutines                 | 29.3 ms                                                               | 40.7 ms: 1.39x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                                                | 241 ms: 1.06x faster                                  |
| float          | 115 ms                                                                | 199 ms: 1.73x slower                                  |
| nbody          | 126 ms                                                                | 284 ms: 2.26x slower                                  |
| Geometric mean | (ref)                                                                 | 1.54x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 189 ms                                                                | 287 ms: 1.51x slower                                  |
| Geometric mean | (ref)                                                                 | 1.10x slower                                          |

Benchmark hidden because not significant (3): regex_v8, regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 40.4 us: 1.15x faster                                 |
| pickle_list          | 7.48 us                                                               | 6.56 us: 1.14x faster                                 |
| xml_etree_iterparse  | 163 ms                                                                | 152 ms: 1.07x faster                                  |
| xml_etree_parse      | 216 ms                                                                | 203 ms: 1.07x faster                                  |
| pickle               | 15.2 us                                                               | 14.4 us: 1.06x faster                                 |
| unpickle_list        | 6.78 us                                                               | 7.37 us: 1.09x slower                                 |
| json_loads           | 37.9 us                                                               | 41.9 us: 1.11x slower                                 |
| json_dumps           | 13.9 ms                                                               | 18.2 ms: 1.31x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 160 ms: 1.33x slower                                  |
| xml_etree_process    | 82.2 ms                                                               | 119 ms: 1.45x slower                                  |
| tomli_loads          | 2.84 sec                                                              | 4.17 sec: 1.47x slower                                |
| unpickle_pure_python | 285 us                                                                | 526 us: 1.84x slower                                  |
| pickle_pure_python   | 428 us                                                                | 792 us: 1.85x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.17x slower                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 27.3 ms: 1.16x slower                                 |
| python_startup_no_site | 16.0 ms                                                               | 18.6 ms: 1.16x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.16x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 117 ms: 1.62x slower                                  |
| genshi_text     | 31.6 ms                                                               | 54.8 ms: 1.73x slower                                 |
| django_template | 46.1 ms                                                               | 80.7 ms: 1.75x slower                                 |
| mako            | 16.7 ms                                                               | 29.7 ms: 1.78x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.72x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                      | 229 ms                                                                | 13.2 ms: 17.38x faster                                |
| bench_mp_pool              | 19.7 ms                                                               | 12.0 ms: 1.64x faster                                 |
| create_gc_cycles           | 2.49 ms                                                               | 1.77 ms: 1.41x faster                                 |
| gc_traversal               | 5.80 ms                                                               | 4.22 ms: 1.37x faster                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.15 sec: 1.25x faster                                |
| pickle_dict                | 46.5 us                                                               | 40.4 us: 1.15x faster                                 |
| pickle_list                | 7.48 us                                                               | 6.56 us: 1.14x faster                                 |
| async_tree_io              | 1.39 sec                                                              | 1.25 sec: 1.12x faster                                |
| async_tree_none_tg         | 526 ms                                                                | 479 ms: 1.10x faster                                  |
| async_tree_memoization_tg  | 692 ms                                                                | 632 ms: 1.10x faster                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 806 ms: 1.09x faster                                  |
| xml_etree_iterparse        | 163 ms                                                                | 152 ms: 1.07x faster                                  |
| xml_etree_parse            | 216 ms                                                                | 203 ms: 1.07x faster                                  |
| async_tree_memoization     | 775 ms                                                                | 728 ms: 1.07x faster                                  |
| pidigits                   | 256 ms                                                                | 241 ms: 1.06x faster                                  |
| pickle                     | 15.2 us                                                               | 14.4 us: 1.06x faster                                 |
| asyncio_tcp                | 972 ms                                                                | 1.05 sec: 1.08x slower                                |
| unpickle_list              | 6.78 us                                                               | 7.37 us: 1.09x slower                                 |
| sqlite_synth               | 3.94 us                                                               | 4.31 us: 1.09x slower                                 |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.12 sec: 1.10x slower                                |
| async_tree_none            | 523 ms                                                                | 578 ms: 1.11x slower                                  |
| json_loads                 | 37.9 us                                                               | 41.9 us: 1.11x slower                                 |
| python_startup             | 23.5 ms                                                               | 27.3 ms: 1.16x slower                                 |
| python_startup_no_site     | 16.0 ms                                                               | 18.6 ms: 1.16x slower                                 |
| json                       | 6.79 ms                                                               | 8.04 ms: 1.18x slower                                 |
| pylint                     | 466 ms                                                                | 554 ms: 1.19x slower                                  |
| docutils                   | 3.94 sec                                                              | 4.69 sec: 1.19x slower                                |
| deepcopy                   | 498 us                                                                | 608 us: 1.22x slower                                  |
| coverage                   | 121 ms                                                                | 149 ms: 1.24x slower                                  |
| bench_thread_pool          | 3.01 ms                                                               | 3.73 ms: 1.24x slower                                 |
| meteor_contest             | 156 ms                                                                | 196 ms: 1.25x slower                                  |
| pycparser                  | 1.71 sec                                                              | 2.15 sec: 1.26x slower                                |
| async_generators           | 588 ms                                                                | 739 ms: 1.26x slower                                  |
| mdp                        | 4.01 sec                                                              | 5.07 sec: 1.27x slower                                |
| tornado_http               | 253 ms                                                                | 320 ms: 1.27x slower                                  |
| generators                 | 40.7 ms                                                               | 52.7 ms: 1.30x slower                                 |
| json_dumps                 | 13.9 ms                                                               | 18.2 ms: 1.31x slower                                 |
| scimark_fft                | 469 ms                                                                | 616 ms: 1.31x slower                                  |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 9.03 ms: 1.32x slower                                 |
| xml_etree_generate         | 120 ms                                                                | 160 ms: 1.33x slower                                  |
| deepcopy_memo              | 50.9 us                                                               | 69.3 us: 1.36x slower                                 |
| coroutines                 | 29.3 ms                                                               | 40.7 ms: 1.39x slower                                 |
| dulwich_log                | 97.5 ms                                                               | 135 ms: 1.39x slower                                  |
| deepcopy_reduce            | 4.31 us                                                               | 6.01 us: 1.40x slower                                 |
| nqueens                    | 108 ms                                                                | 153 ms: 1.41x slower                                  |
| richards                   | 68.8 ms                                                               | 99.0 ms: 1.44x slower                                 |
| xml_etree_process          | 82.2 ms                                                               | 119 ms: 1.45x slower                                  |
| html5lib                   | 92.0 ms                                                               | 135 ms: 1.47x slower                                  |
| tomli_loads                | 2.84 sec                                                              | 4.17 sec: 1.47x slower                                |
| crypto_pyaes               | 102 ms                                                                | 150 ms: 1.47x slower                                  |
| fannkuch                   | 535 ms                                                                | 794 ms: 1.48x slower                                  |
| bpe_tokeniser              | 6.53 sec                                                              | 9.73 sec: 1.49x slower                                |
| 2to3                       | 441 ms                                                                | 661 ms: 1.50x slower                                  |
| sympy_integrate            | 28.7 ms                                                               | 43.4 ms: 1.51x slower                                 |
| regex_compile              | 189 ms                                                                | 287 ms: 1.51x slower                                  |
| typing_runtime_protocols   | 222 us                                                                | 337 us: 1.52x slower                                  |
| pyflate                    | 710 ms                                                                | 1.08 sec: 1.52x slower                                |
| sqlglot_optimize           | 77.9 ms                                                               | 121 ms: 1.55x slower                                  |
| sqlglot_normalize          | 150 ms                                                                | 235 ms: 1.56x slower                                  |
| thrift                     | 1.09 ms                                                               | 1.71 ms: 1.58x slower                                 |
| spectral_norm              | 151 ms                                                                | 245 ms: 1.62x slower                                  |
| genshi_xml                 | 71.9 ms                                                               | 117 ms: 1.62x slower                                  |
| richards_super             | 73.5 ms                                                               | 122 ms: 1.67x slower                                  |
| logging_simple             | 9.16 us                                                               | 15.5 us: 1.69x slower                                 |
| pprint_pformat             | 2.04 sec                                                              | 3.50 sec: 1.72x slower                                |
| pprint_safe_repr           | 991 ms                                                                | 1.71 sec: 1.72x slower                                |
| float                      | 115 ms                                                                | 199 ms: 1.73x slower                                  |
| genshi_text                | 31.6 ms                                                               | 54.8 ms: 1.73x slower                                 |
| django_template            | 46.1 ms                                                               | 80.7 ms: 1.75x slower                                 |
| logging_silent             | 137 ns                                                                | 240 ns: 1.75x slower                                  |
| sympy_str                  | 376 ms                                                                | 664 ms: 1.76x slower                                  |
| mako                       | 16.7 ms                                                               | 29.7 ms: 1.78x slower                                 |
| logging_format             | 9.36 us                                                               | 16.8 us: 1.80x slower                                 |
| unpickle_pure_python       | 285 us                                                                | 526 us: 1.84x slower                                  |
| pickle_pure_python         | 428 us                                                                | 792 us: 1.85x slower                                  |
| scimark_monte_carlo        | 89.0 ms                                                               | 165 ms: 1.85x slower                                  |
| comprehensions             | 22.6 us                                                               | 42.1 us: 1.86x slower                                 |
| scimark_sor                | 176 ms                                                                | 337 ms: 1.91x slower                                  |
| sqlglot_transpile          | 2.24 ms                                                               | 4.33 ms: 1.93x slower                                 |
| hexiom                     | 8.42 ms                                                               | 16.5 ms: 1.95x slower                                 |
| sqlglot_parse              | 1.92 ms                                                               | 3.77 ms: 1.97x slower                                 |
| sympy_expand               | 638 ms                                                                | 1.27 sec: 1.98x slower                                |
| chaos                      | 81.5 ms                                                               | 165 ms: 2.03x slower                                  |
| sympy_sum                  | 226 ms                                                                | 460 ms: 2.03x slower                                  |
| go                         | 193 ms                                                                | 395 ms: 2.05x slower                                  |
| scimark_lu                 | 150 ms                                                                | 326 ms: 2.18x slower                                  |
| raytrace                   | 351 ms                                                                | 784 ms: 2.23x slower                                  |
| nbody                      | 126 ms                                                                | 284 ms: 2.26x slower                                  |
| deltablue                  | 4.55 ms                                                               | 10.8 ms: 2.38x slower                                 |
| unpack_sequence            | 54.6 ns                                                               | 191 ns: 3.49x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.31x slower                                          |

Benchmark hidden because not significant (7): regex_v8, unpickle, asyncio_websockets, regex_effbot, pathlib, regex_dna, async_tree_cpu_io_mixed
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.16x