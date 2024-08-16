# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4767a6e
- commit date: 2024-08-06
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 2.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 666 ms: 1.50x slower                                  |
| docutils       | 4.06 sec                                                              | 5.00 sec: 1.23x slower                                |
| html5lib       | 95.8 ms                                                               | 162 ms: 1.69x slower                                  |
| tornado_http   | 262 ms                                                                | 337 ms: 1.28x slower                                  |
| Geometric mean | (ref)                                                                 | 1.41x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.14 sec: 1.58x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 634 ms: 1.47x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.24 sec: 1.44x faster                                |
| async_tree_none_tg         | 692 ms                                                                | 483 ms: 1.43x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 744 ms: 1.28x faster                                  |
| async_tree_none            | 740 ms                                                                | 607 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 909 ms: 1.21x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 961 ms: 1.18x faster                                  |
| asyncio_websockets         | 766 ms                                                                | 737 ms: 1.04x faster                                  |
| asyncio_tcp                | 958 ms                                                                | 1.11 sec: 1.16x slower                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.33 sec: 1.19x slower                                |
| async_generators           | 617 ms                                                                | 740 ms: 1.20x slower                                  |
| coroutines                 | 30.1 ms                                                               | 43.8 ms: 1.45x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.12x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 255 ms                                                                | 267 ms: 1.05x slower                                  |
| float          | 127 ms                                                                | 190 ms: 1.50x slower                                  |
| nbody          | 125 ms                                                                | 309 ms: 2.48x slower                                  |
| Geometric mean | (ref)                                                                 | 1.57x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 287 ms                                                                | 304 ms: 1.06x slower                                  |
| regex_v8       | 31.1 ms                                                               | 36.9 ms: 1.19x slower                                 |
| regex_compile  | 197 ms                                                                | 288 ms: 1.46x slower                                  |
| Geometric mean | (ref)                                                                 | 1.16x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 42.8 us: 1.09x faster                                 |
| pickle               | 14.8 us                                                               | 14.1 us: 1.05x faster                                 |
| xml_etree_iterparse  | 157 ms                                                                | 168 ms: 1.07x slower                                  |
| json_loads           | 36.6 us                                                               | 45.4 us: 1.24x slower                                 |
| unpickle             | 19.7 us                                                               | 24.7 us: 1.25x slower                                 |
| xml_etree_generate   | 128 ms                                                                | 162 ms: 1.26x slower                                  |
| json_dumps           | 13.6 ms                                                               | 18.6 ms: 1.37x slower                                 |
| tomli_loads          | 2.99 sec                                                              | 4.21 sec: 1.41x slower                                |
| xml_etree_process    | 85.7 ms                                                               | 132 ms: 1.54x slower                                  |
| unpickle_pure_python | 319 us                                                                | 537 us: 1.68x slower                                  |
| pickle_pure_python   | 447 us                                                                | 764 us: 1.71x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.22x slower                                          |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 19.2 ms: 1.18x slower                                 |
| python_startup         | 21.2 ms                                                               | 29.3 ms: 1.38x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.28x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 123 ms: 1.67x slower                                  |
| django_template | 48.6 ms                                                               | 81.9 ms: 1.69x slower                                 |
| mako            | 17.2 ms                                                               | 30.3 ms: 1.76x slower                                 |
| genshi_text     | 31.9 ms                                                               | 56.5 ms: 1.77x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.72x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.14 sec: 1.58x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 634 ms: 1.47x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.24 sec: 1.44x faster                                |
| async_tree_none_tg         | 692 ms                                                                | 483 ms: 1.43x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 744 ms: 1.28x faster                                  |
| async_tree_none            | 740 ms                                                                | 607 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 909 ms: 1.21x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 961 ms: 1.18x faster                                  |
| bench_mp_pool              | 18.4 ms                                                               | 16.0 ms: 1.15x faster                                 |
| gc_traversal               | 5.61 ms                                                               | 5.03 ms: 1.11x faster                                 |
| pickle_dict                | 46.5 us                                                               | 42.8 us: 1.09x faster                                 |
| pickle                     | 14.8 us                                                               | 14.1 us: 1.05x faster                                 |
| asyncio_websockets         | 766 ms                                                                | 737 ms: 1.04x faster                                  |
| pidigits                   | 255 ms                                                                | 267 ms: 1.05x slower                                  |
| pathlib                    | 31.7 ms                                                               | 33.6 ms: 1.06x slower                                 |
| regex_dna                  | 287 ms                                                                | 304 ms: 1.06x slower                                  |
| xml_etree_iterparse        | 157 ms                                                                | 168 ms: 1.07x slower                                  |
| sqlite_synth               | 3.75 us                                                               | 4.22 us: 1.13x slower                                 |
| asyncio_tcp                | 958 ms                                                                | 1.11 sec: 1.16x slower                                |
| generators                 | 46.0 ms                                                               | 53.8 ms: 1.17x slower                                 |
| python_startup_no_site     | 16.3 ms                                                               | 19.2 ms: 1.18x slower                                 |
| pylint                     | 501 ms                                                                | 591 ms: 1.18x slower                                  |
| regex_v8                   | 31.1 ms                                                               | 36.9 ms: 1.19x slower                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.33 sec: 1.19x slower                                |
| deepcopy                   | 503 us                                                                | 602 us: 1.20x slower                                  |
| async_generators           | 617 ms                                                                | 740 ms: 1.20x slower                                  |
| docutils                   | 4.06 sec                                                              | 5.00 sec: 1.23x slower                                |
| json_loads                 | 36.6 us                                                               | 45.4 us: 1.24x slower                                 |
| unpickle                   | 19.7 us                                                               | 24.7 us: 1.25x slower                                 |
| deepcopy_memo              | 57.5 us                                                               | 72.1 us: 1.26x slower                                 |
| xml_etree_generate         | 128 ms                                                                | 162 ms: 1.26x slower                                  |
| tornado_http               | 262 ms                                                                | 337 ms: 1.28x slower                                  |
| pycparser                  | 1.73 sec                                                              | 2.23 sec: 1.29x slower                                |
| mdp                        | 3.84 sec                                                              | 5.00 sec: 1.30x slower                                |
| scimark_fft                | 499 ms                                                                | 651 ms: 1.30x slower                                  |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 9.98 ms: 1.34x slower                                 |
| json                       | 6.68 ms                                                               | 8.93 ms: 1.34x slower                                 |
| deepcopy_reduce            | 4.45 us                                                               | 5.96 us: 1.34x slower                                 |
| json_dumps                 | 13.6 ms                                                               | 18.6 ms: 1.37x slower                                 |
| crypto_pyaes               | 112 ms                                                                | 154 ms: 1.38x slower                                  |
| python_startup             | 21.2 ms                                                               | 29.3 ms: 1.38x slower                                 |
| sympy_integrate            | 31.4 ms                                                               | 44.2 ms: 1.41x slower                                 |
| tomli_loads                | 2.99 sec                                                              | 4.21 sec: 1.41x slower                                |
| comprehensions             | 29.6 us                                                               | 41.9 us: 1.42x slower                                 |
| meteor_contest             | 149 ms                                                                | 212 ms: 1.42x slower                                  |
| bench_thread_pool          | 3.11 ms                                                               | 4.44 ms: 1.43x slower                                 |
| coroutines                 | 30.1 ms                                                               | 43.8 ms: 1.45x slower                                 |
| regex_compile              | 197 ms                                                                | 288 ms: 1.46x slower                                  |
| fannkuch                   | 551 ms                                                                | 806 ms: 1.46x slower                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 9.70 sec: 1.46x slower                                |
| nqueens                    | 110 ms                                                                | 161 ms: 1.46x slower                                  |
| 2to3                       | 444 ms                                                                | 666 ms: 1.50x slower                                  |
| float                      | 127 ms                                                                | 190 ms: 1.50x slower                                  |
| telco                      | 9.71 ms                                                               | 14.8 ms: 1.52x slower                                 |
| thrift                     | 1.17 ms                                                               | 1.78 ms: 1.52x slower                                 |
| logging_simple             | 9.89 us                                                               | 15.1 us: 1.52x slower                                 |
| xml_etree_process          | 85.7 ms                                                               | 132 ms: 1.54x slower                                  |
| spectral_norm              | 158 ms                                                                | 247 ms: 1.57x slower                                  |
| logging_format             | 11.8 us                                                               | 18.8 us: 1.59x slower                                 |
| sqlglot_optimize           | 76.5 ms                                                               | 122 ms: 1.59x slower                                  |
| sqlglot_normalize          | 148 ms                                                                | 237 ms: 1.60x slower                                  |
| coverage                   | 97.6 ms                                                               | 157 ms: 1.61x slower                                  |
| sympy_str                  | 425 ms                                                                | 698 ms: 1.64x slower                                  |
| pyflate                    | 661 ms                                                                | 1.10 sec: 1.67x slower                                |
| genshi_xml                 | 73.6 ms                                                               | 123 ms: 1.67x slower                                  |
| unpickle_pure_python       | 319 us                                                                | 537 us: 1.68x slower                                  |
| html5lib                   | 95.8 ms                                                               | 162 ms: 1.69x slower                                  |
| django_template            | 48.6 ms                                                               | 81.9 ms: 1.69x slower                                 |
| pprint_pformat             | 2.03 sec                                                              | 3.44 sec: 1.70x slower                                |
| scimark_monte_carlo        | 98.5 ms                                                               | 168 ms: 1.70x slower                                  |
| pprint_safe_repr           | 970 ms                                                                | 1.65 sec: 1.71x slower                                |
| pickle_pure_python         | 447 us                                                                | 764 us: 1.71x slower                                  |
| mako                       | 17.2 ms                                                               | 30.3 ms: 1.76x slower                                 |
| genshi_text                | 31.9 ms                                                               | 56.5 ms: 1.77x slower                                 |
| hexiom                     | 8.87 ms                                                               | 16.2 ms: 1.82x slower                                 |
| richards                   | 63.4 ms                                                               | 116 ms: 1.83x slower                                  |
| richards_super             | 67.9 ms                                                               | 127 ms: 1.87x slower                                  |
| sympy_expand               | 689 ms                                                                | 1.30 sec: 1.88x slower                                |
| chaos                      | 93.7 ms                                                               | 179 ms: 1.91x slower                                  |
| raytrace                   | 418 ms                                                                | 800 ms: 1.91x slower                                  |
| typing_runtime_protocols   | 199 us                                                                | 383 us: 1.92x slower                                  |
| logging_silent             | 135 ns                                                                | 267 ns: 1.97x slower                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.79 ms: 2.00x slower                                 |
| scimark_sor                | 171 ms                                                                | 347 ms: 2.03x slower                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.65 ms: 2.04x slower                                 |
| sympy_sum                  | 229 ms                                                                | 470 ms: 2.05x slower                                  |
| scimark_lu                 | 155 ms                                                                | 336 ms: 2.17x slower                                  |
| deltablue                  | 5.05 ms                                                               | 11.9 ms: 2.35x slower                                 |
| go                         | 185 ms                                                                | 457 ms: 2.47x slower                                  |
| nbody                      | 125 ms                                                                | 309 ms: 2.48x slower                                  |
| unpack_sequence            | 68.5 ns                                                               | 217 ns: 3.16x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.37x slower                                          |

Benchmark hidden because not significant (5): xml_etree_parse, create_gc_cycles, regex_effbot, pickle_list, unpickle_list
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 2.23x