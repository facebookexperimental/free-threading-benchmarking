# Results vs. 3.13.0b1

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.34x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 647 ms: 1.47x slower                                                  |
| docutils       | 3.94 sec                                                              | 4.82 sec: 1.22x slower                                                |
| html5lib       | 92.0 ms                                                               | 141 ms: 1.53x slower                                                  |
| tornado_http   | 253 ms                                                                | 342 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.39x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.43 sec                                                              | 1.12 sec: 1.28x faster                                                |
| async_tree_io              | 1.39 sec                                                              | 1.23 sec: 1.13x faster                                                |
| async_tree_memoization_tg  | 692 ms                                                                | 632 ms: 1.09x faster                                                  |
| async_tree_none_tg         | 526 ms                                                                | 482 ms: 1.09x faster                                                  |
| async_tree_memoization     | 775 ms                                                                | 721 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 820 ms: 1.07x faster                                                  |
| asyncio_tcp                | 972 ms                                                                | 1.02 sec: 1.05x slower                                                |
| async_tree_none            | 523 ms                                                                | 566 ms: 1.08x slower                                                  |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.18 sec: 1.12x slower                                                |
| async_generators           | 588 ms                                                                | 723 ms: 1.23x slower                                                  |
| coroutines                 | 29.3 ms                                                               | 39.3 ms: 1.34x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 256 ms                                                                | 242 ms: 1.06x faster                                                  |
| float          | 115 ms                                                                | 193 ms: 1.68x slower                                                  |
| nbody          | 126 ms                                                                | 280 ms: 2.23x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.52x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 37.1 ms                                                               | 35.3 ms: 1.05x faster                                                 |
| regex_effbot   | 4.63 ms                                                               | 4.47 ms: 1.04x faster                                                 |
| regex_dna      | 284 ms                                                                | 295 ms: 1.04x slower                                                  |
| regex_compile  | 189 ms                                                                | 293 ms: 1.54x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.10x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.53 us: 1.15x faster                                                 |
| xml_etree_parse      | 216 ms                                                                | 201 ms: 1.08x faster                                                  |
| pickle_dict          | 46.5 us                                                               | 44.0 us: 1.06x faster                                                 |
| pickle               | 15.2 us                                                               | 14.5 us: 1.05x faster                                                 |
| unpickle_list        | 6.78 us                                                               | 7.76 us: 1.15x slower                                                 |
| json_loads           | 37.9 us                                                               | 43.6 us: 1.15x slower                                                 |
| json_dumps           | 13.9 ms                                                               | 17.8 ms: 1.28x slower                                                 |
| xml_etree_generate   | 120 ms                                                                | 160 ms: 1.34x slower                                                  |
| tomli_loads          | 2.84 sec                                                              | 4.22 sec: 1.49x slower                                                |
| xml_etree_process    | 82.2 ms                                                               | 126 ms: 1.53x slower                                                  |
| pickle_pure_python   | 428 us                                                                | 830 us: 1.94x slower                                                  |
| unpickle_pure_python | 285 us                                                                | 558 us: 1.96x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.21x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 19.5 ms: 1.22x slower                                                 |
| python_startup         | 23.5 ms                                                               | 28.9 ms: 1.23x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.23x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 120 ms: 1.66x slower                                                  |
| genshi_text     | 31.6 ms                                                               | 54.4 ms: 1.72x slower                                                 |
| django_template | 46.1 ms                                                               | 80.6 ms: 1.75x slower                                                 |
| mako            | 16.7 ms                                                               | 29.9 ms: 1.80x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.73x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| telco                      | 229 ms                                                                | 14.1 ms: 16.28x faster                                                |
| bench_mp_pool              | 19.7 ms                                                               | 13.6 ms: 1.44x faster                                                 |
| gc_traversal               | 5.80 ms                                                               | 4.28 ms: 1.36x faster                                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.12 sec: 1.28x faster                                                |
| create_gc_cycles           | 2.49 ms                                                               | 1.95 ms: 1.27x faster                                                 |
| pickle_list                | 7.48 us                                                               | 6.53 us: 1.15x faster                                                 |
| async_tree_io              | 1.39 sec                                                              | 1.23 sec: 1.13x faster                                                |
| async_tree_memoization_tg  | 692 ms                                                                | 632 ms: 1.09x faster                                                  |
| async_tree_none_tg         | 526 ms                                                                | 482 ms: 1.09x faster                                                  |
| xml_etree_parse            | 216 ms                                                                | 201 ms: 1.08x faster                                                  |
| async_tree_memoization     | 775 ms                                                                | 721 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 820 ms: 1.07x faster                                                  |
| pidigits                   | 256 ms                                                                | 242 ms: 1.06x faster                                                  |
| pickle_dict                | 46.5 us                                                               | 44.0 us: 1.06x faster                                                 |
| regex_v8                   | 37.1 ms                                                               | 35.3 ms: 1.05x faster                                                 |
| pickle                     | 15.2 us                                                               | 14.5 us: 1.05x faster                                                 |
| regex_effbot               | 4.63 ms                                                               | 4.47 ms: 1.04x faster                                                 |
| regex_dna                  | 284 ms                                                                | 295 ms: 1.04x slower                                                  |
| asyncio_tcp                | 972 ms                                                                | 1.02 sec: 1.05x slower                                                |
| async_tree_none            | 523 ms                                                                | 566 ms: 1.08x slower                                                  |
| sqlite_synth               | 3.94 us                                                               | 4.28 us: 1.09x slower                                                 |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.18 sec: 1.12x slower                                                |
| json                       | 6.79 ms                                                               | 7.69 ms: 1.13x slower                                                 |
| unpickle_list              | 6.78 us                                                               | 7.76 us: 1.15x slower                                                 |
| json_loads                 | 37.9 us                                                               | 43.6 us: 1.15x slower                                                 |
| coverage                   | 121 ms                                                                | 141 ms: 1.17x slower                                                  |
| deepcopy                   | 498 us                                                                | 600 us: 1.20x slower                                                  |
| pylint                     | 466 ms                                                                | 562 ms: 1.21x slower                                                  |
| python_startup_no_site     | 16.0 ms                                                               | 19.5 ms: 1.22x slower                                                 |
| docutils                   | 3.94 sec                                                              | 4.82 sec: 1.22x slower                                                |
| async_generators           | 588 ms                                                                | 723 ms: 1.23x slower                                                  |
| python_startup             | 23.5 ms                                                               | 28.9 ms: 1.23x slower                                                 |
| mdp                        | 4.01 sec                                                              | 5.02 sec: 1.25x slower                                                |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 8.68 ms: 1.27x slower                                                 |
| pycparser                  | 1.71 sec                                                              | 2.18 sec: 1.27x slower                                                |
| json_dumps                 | 13.9 ms                                                               | 17.8 ms: 1.28x slower                                                 |
| meteor_contest             | 156 ms                                                                | 208 ms: 1.33x slower                                                  |
| deepcopy_reduce            | 4.31 us                                                               | 5.73 us: 1.33x slower                                                 |
| xml_etree_generate         | 120 ms                                                                | 160 ms: 1.34x slower                                                  |
| coroutines                 | 29.3 ms                                                               | 39.3 ms: 1.34x slower                                                 |
| generators                 | 40.7 ms                                                               | 54.8 ms: 1.35x slower                                                 |
| tornado_http               | 253 ms                                                                | 342 ms: 1.35x slower                                                  |
| deepcopy_memo              | 50.9 us                                                               | 69.1 us: 1.36x slower                                                 |
| scimark_fft                | 469 ms                                                                | 641 ms: 1.37x slower                                                  |
| bench_thread_pool          | 3.01 ms                                                               | 4.27 ms: 1.42x slower                                                 |
| fannkuch                   | 535 ms                                                                | 772 ms: 1.44x slower                                                  |
| 2to3                       | 441 ms                                                                | 647 ms: 1.47x slower                                                  |
| tomli_loads                | 2.84 sec                                                              | 4.22 sec: 1.49x slower                                                |
| sympy_integrate            | 28.7 ms                                                               | 42.8 ms: 1.49x slower                                                 |
| nqueens                    | 108 ms                                                                | 162 ms: 1.49x slower                                                  |
| pyflate                    | 710 ms                                                                | 1.07 sec: 1.51x slower                                                |
| bpe_tokeniser              | 6.53 sec                                                              | 9.90 sec: 1.52x slower                                                |
| html5lib                   | 92.0 ms                                                               | 141 ms: 1.53x slower                                                  |
| xml_etree_process          | 82.2 ms                                                               | 126 ms: 1.53x slower                                                  |
| regex_compile              | 189 ms                                                                | 293 ms: 1.54x slower                                                  |
| crypto_pyaes               | 102 ms                                                                | 159 ms: 1.56x slower                                                  |
| thrift                     | 1.09 ms                                                               | 1.70 ms: 1.57x slower                                                 |
| spectral_norm              | 151 ms                                                                | 242 ms: 1.61x slower                                                  |
| richards                   | 68.8 ms                                                               | 111 ms: 1.62x slower                                                  |
| typing_runtime_protocols   | 222 us                                                                | 362 us: 1.63x slower                                                  |
| sqlglot_normalize          | 150 ms                                                                | 246 ms: 1.64x slower                                                  |
| genshi_xml                 | 71.9 ms                                                               | 120 ms: 1.66x slower                                                  |
| float                      | 115 ms                                                                | 193 ms: 1.68x slower                                                  |
| comprehensions             | 22.6 us                                                               | 38.3 us: 1.69x slower                                                 |
| sqlglot_optimize           | 77.9 ms                                                               | 133 ms: 1.71x slower                                                  |
| richards_super             | 73.5 ms                                                               | 125 ms: 1.71x slower                                                  |
| pprint_pformat             | 2.04 sec                                                              | 3.48 sec: 1.71x slower                                                |
| genshi_text                | 31.6 ms                                                               | 54.4 ms: 1.72x slower                                                 |
| logging_simple             | 9.16 us                                                               | 15.9 us: 1.74x slower                                                 |
| pprint_safe_repr           | 991 ms                                                                | 1.73 sec: 1.75x slower                                                |
| django_template            | 46.1 ms                                                               | 80.6 ms: 1.75x slower                                                 |
| sympy_str                  | 376 ms                                                                | 663 ms: 1.76x slower                                                  |
| mako                       | 16.7 ms                                                               | 29.9 ms: 1.80x slower                                                 |
| logging_format             | 9.36 us                                                               | 17.6 us: 1.88x slower                                                 |
| logging_silent             | 137 ns                                                                | 259 ns: 1.90x slower                                                  |
| scimark_monte_carlo        | 89.0 ms                                                               | 171 ms: 1.92x slower                                                  |
| pickle_pure_python         | 428 us                                                                | 830 us: 1.94x slower                                                  |
| unpickle_pure_python       | 285 us                                                                | 558 us: 1.96x slower                                                  |
| sqlglot_parse              | 1.92 ms                                                               | 3.76 ms: 1.96x slower                                                 |
| sympy_expand               | 638 ms                                                                | 1.27 sec: 1.99x slower                                                |
| scimark_sor                | 176 ms                                                                | 351 ms: 1.99x slower                                                  |
| chaos                      | 81.5 ms                                                               | 163 ms: 2.00x slower                                                  |
| sqlglot_transpile          | 2.24 ms                                                               | 4.53 ms: 2.02x slower                                                 |
| hexiom                     | 8.42 ms                                                               | 17.4 ms: 2.07x slower                                                 |
| scimark_lu                 | 150 ms                                                                | 313 ms: 2.09x slower                                                  |
| go                         | 193 ms                                                                | 406 ms: 2.10x slower                                                  |
| sympy_sum                  | 226 ms                                                                | 493 ms: 2.18x slower                                                  |
| nbody                      | 126 ms                                                                | 280 ms: 2.23x slower                                                  |
| raytrace                   | 351 ms                                                                | 806 ms: 2.29x slower                                                  |
| deltablue                  | 4.55 ms                                                               | 11.7 ms: 2.56x slower                                                 |
| unpack_sequence            | 54.6 ns                                                               | 201 ns: 3.68x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.34x slower                                                          |

Benchmark hidden because not significant (5): xml_etree_iterparse, unpickle, asyncio_websockets, async_tree_cpu_io_mixed, pathlib
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.16x