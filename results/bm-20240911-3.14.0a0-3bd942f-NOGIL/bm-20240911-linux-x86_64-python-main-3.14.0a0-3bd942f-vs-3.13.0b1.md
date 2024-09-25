# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3bd942f
- commit date: 2024-09-11
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 626 ms: 1.42x slower                                  |
| docutils       | 3.94 sec                                                              | 4.76 sec: 1.21x slower                                |
| html5lib       | 92.0 ms                                                               | 141 ms: 1.53x slower                                  |
| tornado_http   | 253 ms                                                                | 352 ms: 1.39x slower                                  |
| Geometric mean | (ref)                                                                 | 1.38x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.43 sec                                                              | 1.13 sec: 1.27x faster                                |
| async_tree_none_tg         | 526 ms                                                                | 495 ms: 1.06x faster                                  |
| async_tree_memoization_tg  | 692 ms                                                                | 653 ms: 1.06x faster                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 829 ms: 1.06x faster                                  |
| async_tree_io              | 1.39 sec                                                              | 1.31 sec: 1.06x faster                                |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 980 ms: 1.09x slower                                  |
| async_tree_none            | 523 ms                                                                | 575 ms: 1.10x slower                                  |
| asyncio_tcp                | 972 ms                                                                | 1.09 sec: 1.12x slower                                |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.27 sec: 1.16x slower                                |
| async_generators           | 588 ms                                                                | 712 ms: 1.21x slower                                  |
| coroutines                 | 29.3 ms                                                               | 45.1 ms: 1.54x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.05x slower                                          |

Benchmark hidden because not significant (2): async_tree_memoization, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                                                | 242 ms: 1.06x faster                                  |
| float          | 115 ms                                                                | 201 ms: 1.74x slower                                  |
| nbody          | 126 ms                                                                | 312 ms: 2.48x slower                                  |
| Geometric mean | (ref)                                                                 | 1.60x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 189 ms                                                                | 290 ms: 1.53x slower                                  |
| Geometric mean | (ref)                                                                 | 1.10x slower                                          |

Benchmark hidden because not significant (3): regex_v8, regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.36 us: 1.18x faster                                 |
| pickle_dict          | 46.5 us                                                               | 43.5 us: 1.07x faster                                 |
| xml_etree_iterparse  | 163 ms                                                                | 175 ms: 1.07x slower                                  |
| xml_etree_parse      | 216 ms                                                                | 235 ms: 1.08x slower                                  |
| unpickle_list        | 6.78 us                                                               | 7.59 us: 1.12x slower                                 |
| json_loads           | 37.9 us                                                               | 42.8 us: 1.13x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 157 ms: 1.31x slower                                  |
| json_dumps           | 13.9 ms                                                               | 18.9 ms: 1.36x slower                                 |
| xml_etree_process    | 82.2 ms                                                               | 121 ms: 1.48x slower                                  |
| tomli_loads          | 2.84 sec                                                              | 4.35 sec: 1.53x slower                                |
| pickle_pure_python   | 428 us                                                                | 804 us: 1.88x slower                                  |
| unpickle_pure_python | 285 us                                                                | 547 us: 1.92x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.22x slower                                          |

Benchmark hidden because not significant (2): pickle, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 30.9 ms: 1.31x slower                                 |
| python_startup_no_site | 16.0 ms                                                               | 21.2 ms: 1.33x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.32x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 116 ms: 1.61x slower                                  |
| django_template | 46.1 ms                                                               | 83.8 ms: 1.82x slower                                 |
| genshi_text     | 31.6 ms                                                               | 58.2 ms: 1.84x slower                                 |
| mako            | 16.7 ms                                                               | 31.2 ms: 1.87x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.78x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                      | 229 ms                                                                | 14.0 ms: 16.35x faster                                |
| create_gc_cycles           | 2.49 ms                                                               | 1.83 ms: 1.36x faster                                 |
| gc_traversal               | 5.80 ms                                                               | 4.51 ms: 1.29x faster                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.13 sec: 1.27x faster                                |
| pickle_list                | 7.48 us                                                               | 6.36 us: 1.18x faster                                 |
| bench_mp_pool              | 19.7 ms                                                               | 17.5 ms: 1.12x faster                                 |
| pickle_dict                | 46.5 us                                                               | 43.5 us: 1.07x faster                                 |
| async_tree_none_tg         | 526 ms                                                                | 495 ms: 1.06x faster                                  |
| async_tree_memoization_tg  | 692 ms                                                                | 653 ms: 1.06x faster                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 829 ms: 1.06x faster                                  |
| async_tree_io              | 1.39 sec                                                              | 1.31 sec: 1.06x faster                                |
| pidigits                   | 256 ms                                                                | 242 ms: 1.06x faster                                  |
| sqlite_synth               | 3.94 us                                                               | 4.19 us: 1.06x slower                                 |
| xml_etree_iterparse        | 163 ms                                                                | 175 ms: 1.07x slower                                  |
| xml_etree_parse            | 216 ms                                                                | 235 ms: 1.08x slower                                  |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 980 ms: 1.09x slower                                  |
| async_tree_none            | 523 ms                                                                | 575 ms: 1.10x slower                                  |
| unpickle_list              | 6.78 us                                                               | 7.59 us: 1.12x slower                                 |
| asyncio_tcp                | 972 ms                                                                | 1.09 sec: 1.12x slower                                |
| json_loads                 | 37.9 us                                                               | 42.8 us: 1.13x slower                                 |
| pathlib                    | 31.8 ms                                                               | 36.6 ms: 1.15x slower                                 |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.27 sec: 1.16x slower                                |
| deepcopy                   | 498 us                                                                | 579 us: 1.16x slower                                  |
| json                       | 6.79 ms                                                               | 7.97 ms: 1.17x slower                                 |
| meteor_contest             | 156 ms                                                                | 186 ms: 1.19x slower                                  |
| docutils                   | 3.94 sec                                                              | 4.76 sec: 1.21x slower                                |
| async_generators           | 588 ms                                                                | 712 ms: 1.21x slower                                  |
| coverage                   | 121 ms                                                                | 147 ms: 1.22x slower                                  |
| scimark_fft                | 469 ms                                                                | 587 ms: 1.25x slower                                  |
| pylint                     | 466 ms                                                                | 593 ms: 1.27x slower                                  |
| mdp                        | 4.01 sec                                                              | 5.11 sec: 1.28x slower                                |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 8.77 ms: 1.28x slower                                 |
| xml_etree_generate         | 120 ms                                                                | 157 ms: 1.31x slower                                  |
| python_startup             | 23.5 ms                                                               | 30.9 ms: 1.31x slower                                 |
| python_startup_no_site     | 16.0 ms                                                               | 21.2 ms: 1.33x slower                                 |
| dulwich_log                | 97.5 ms                                                               | 130 ms: 1.33x slower                                  |
| pycparser                  | 1.71 sec                                                              | 2.28 sec: 1.33x slower                                |
| generators                 | 40.7 ms                                                               | 54.8 ms: 1.35x slower                                 |
| json_dumps                 | 13.9 ms                                                               | 18.9 ms: 1.36x slower                                 |
| deepcopy_reduce            | 4.31 us                                                               | 5.88 us: 1.36x slower                                 |
| tornado_http               | 253 ms                                                                | 352 ms: 1.39x slower                                  |
| bench_thread_pool          | 3.01 ms                                                               | 4.19 ms: 1.39x slower                                 |
| 2to3                       | 441 ms                                                                | 626 ms: 1.42x slower                                  |
| fannkuch                   | 535 ms                                                                | 767 ms: 1.43x slower                                  |
| deepcopy_memo              | 50.9 us                                                               | 73.7 us: 1.45x slower                                 |
| nqueens                    | 108 ms                                                                | 160 ms: 1.47x slower                                  |
| xml_etree_process          | 82.2 ms                                                               | 121 ms: 1.48x slower                                  |
| crypto_pyaes               | 102 ms                                                                | 151 ms: 1.48x slower                                  |
| pyflate                    | 710 ms                                                                | 1.08 sec: 1.52x slower                                |
| thrift                     | 1.09 ms                                                               | 1.65 ms: 1.52x slower                                 |
| sympy_integrate            | 28.7 ms                                                               | 43.8 ms: 1.52x slower                                 |
| richards                   | 68.8 ms                                                               | 105 ms: 1.52x slower                                  |
| regex_compile              | 189 ms                                                                | 290 ms: 1.53x slower                                  |
| html5lib                   | 92.0 ms                                                               | 141 ms: 1.53x slower                                  |
| tomli_loads                | 2.84 sec                                                              | 4.35 sec: 1.53x slower                                |
| bpe_tokeniser              | 6.53 sec                                                              | 10.0 sec: 1.54x slower                                |
| coroutines                 | 29.3 ms                                                               | 45.1 ms: 1.54x slower                                 |
| sqlglot_optimize           | 77.9 ms                                                               | 125 ms: 1.60x slower                                  |
| genshi_xml                 | 71.9 ms                                                               | 116 ms: 1.61x slower                                  |
| sqlglot_normalize          | 150 ms                                                                | 245 ms: 1.63x slower                                  |
| logging_simple             | 9.16 us                                                               | 15.0 us: 1.64x slower                                 |
| typing_runtime_protocols   | 222 us                                                                | 364 us: 1.64x slower                                  |
| spectral_norm              | 151 ms                                                                | 254 ms: 1.68x slower                                  |
| comprehensions             | 22.6 us                                                               | 38.4 us: 1.70x slower                                 |
| pprint_safe_repr           | 991 ms                                                                | 1.69 sec: 1.71x slower                                |
| logging_format             | 9.36 us                                                               | 16.0 us: 1.71x slower                                 |
| pprint_pformat             | 2.04 sec                                                              | 3.52 sec: 1.73x slower                                |
| float                      | 115 ms                                                                | 201 ms: 1.74x slower                                  |
| scimark_monte_carlo        | 89.0 ms                                                               | 157 ms: 1.76x slower                                  |
| richards_super             | 73.5 ms                                                               | 130 ms: 1.77x slower                                  |
| sympy_str                  | 376 ms                                                                | 672 ms: 1.78x slower                                  |
| django_template            | 46.1 ms                                                               | 83.8 ms: 1.82x slower                                 |
| sqlglot_parse              | 1.92 ms                                                               | 3.50 ms: 1.83x slower                                 |
| genshi_text                | 31.6 ms                                                               | 58.2 ms: 1.84x slower                                 |
| mako                       | 16.7 ms                                                               | 31.2 ms: 1.87x slower                                 |
| pickle_pure_python         | 428 us                                                                | 804 us: 1.88x slower                                  |
| hexiom                     | 8.42 ms                                                               | 16.0 ms: 1.90x slower                                 |
| scimark_sor                | 176 ms                                                                | 337 ms: 1.91x slower                                  |
| go                         | 193 ms                                                                | 369 ms: 1.91x slower                                  |
| unpickle_pure_python       | 285 us                                                                | 547 us: 1.92x slower                                  |
| logging_silent             | 137 ns                                                                | 272 ns: 1.99x slower                                  |
| sqlglot_transpile          | 2.24 ms                                                               | 4.53 ms: 2.02x slower                                 |
| sympy_sum                  | 226 ms                                                                | 464 ms: 2.05x slower                                  |
| scimark_lu                 | 150 ms                                                                | 309 ms: 2.06x slower                                  |
| chaos                      | 81.5 ms                                                               | 168 ms: 2.06x slower                                  |
| sympy_expand               | 638 ms                                                                | 1.36 sec: 2.12x slower                                |
| raytrace                   | 351 ms                                                                | 791 ms: 2.25x slower                                  |
| deltablue                  | 4.55 ms                                                               | 10.9 ms: 2.40x slower                                 |
| nbody                      | 126 ms                                                                | 312 ms: 2.48x slower                                  |
| unpack_sequence            | 54.6 ns                                                               | 187 ns: 3.43x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.35x slower                                          |

Benchmark hidden because not significant (7): async_tree_memoization, regex_v8, pickle, regex_effbot, regex_dna, asyncio_websockets, unpickle
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.15x