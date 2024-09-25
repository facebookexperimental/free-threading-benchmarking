# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4767a6e
- commit date: 2024-08-06
- overall geometric mean: 1.44x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 666 ms: 1.50x slower                                  |
| docutils       | 4.01 sec                                                     | 5.00 sec: 1.25x slower                                |
| html5lib       | 92.6 ms                                                      | 162 ms: 1.74x slower                                  |
| tornado_http   | 251 ms                                                       | 337 ms: 1.34x slower                                  |
| Geometric mean | (ref)                                                        | 1.45x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.14 sec: 1.23x faster                                |
| async_tree_io              | 1.39 sec                                                     | 1.24 sec: 1.12x faster                                |
| async_tree_memoization_tg  | 670 ms                                                       | 634 ms: 1.06x faster                                  |
| async_tree_none_tg         | 504 ms                                                       | 483 ms: 1.04x faster                                  |
| asyncio_websockets         | 766 ms                                                       | 737 ms: 1.04x faster                                  |
| async_tree_memoization     | 709 ms                                                       | 744 ms: 1.05x slower                                  |
| async_tree_none            | 572 ms                                                       | 607 ms: 1.06x slower                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 909 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 961 ms: 1.08x slower                                  |
| asyncio_tcp                | 948 ms                                                       | 1.11 sec: 1.17x slower                                |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.33 sec: 1.20x slower                                |
| async_generators           | 567 ms                                                       | 740 ms: 1.31x slower                                  |
| coroutines                 | 30.9 ms                                                      | 43.8 ms: 1.42x slower                                 |
| Geometric mean             | (ref)                                                        | 1.06x slower                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 251 ms                                                       | 267 ms: 1.06x slower                                  |
| float          | 116 ms                                                       | 190 ms: 1.64x slower                                  |
| nbody          | 119 ms                                                       | 309 ms: 2.60x slower                                  |
| Geometric mean | (ref)                                                        | 1.66x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.97 ms: 1.05x slower                                 |
| regex_dna      | 282 ms                                                       | 304 ms: 1.08x slower                                  |
| regex_v8       | 32.8 ms                                                      | 36.9 ms: 1.13x slower                                 |
| regex_compile  | 182 ms                                                       | 288 ms: 1.58x slower                                  |
| Geometric mean | (ref)                                                        | 1.19x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 47.2 us                                                      | 42.8 us: 1.10x faster                                 |
| pickle               | 15.1 us                                                      | 14.1 us: 1.07x faster                                 |
| pickle_list          | 6.86 us                                                      | 6.56 us: 1.05x faster                                 |
| unpickle_list        | 6.68 us                                                      | 7.55 us: 1.13x slower                                 |
| unpickle             | 20.5 us                                                      | 24.7 us: 1.20x slower                                 |
| json_dumps           | 14.1 ms                                                      | 18.6 ms: 1.32x slower                                 |
| xml_etree_generate   | 122 ms                                                       | 162 ms: 1.32x slower                                  |
| json_loads           | 34.3 us                                                      | 45.4 us: 1.33x slower                                 |
| tomli_loads          | 2.78 sec                                                     | 4.21 sec: 1.52x slower                                |
| xml_etree_process    | 85.9 ms                                                      | 132 ms: 1.54x slower                                  |
| pickle_pure_python   | 416 us                                                       | 764 us: 1.83x slower                                  |
| unpickle_pure_python | 290 us                                                       | 537 us: 1.85x slower                                  |
| Geometric mean       | (ref)                                                        | 1.23x slower                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.2 ms: 1.25x slower                                 |
| python_startup         | 22.4 ms                                                      | 29.3 ms: 1.31x slower                                 |
| Geometric mean         | (ref)                                                        | 1.28x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 123 ms: 1.70x slower                                  |
| genshi_text     | 31.7 ms                                                      | 56.5 ms: 1.78x slower                                 |
| django_template | 44.3 ms                                                      | 81.9 ms: 1.85x slower                                 |
| mako            | 15.9 ms                                                      | 30.3 ms: 1.90x slower                                 |
| Geometric mean  | (ref)                                                        | 1.81x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.14 sec: 1.23x faster                                |
| create_gc_cycles           | 2.41 ms                                                      | 1.99 ms: 1.21x faster                                 |
| bench_mp_pool              | 18.7 ms                                                      | 16.0 ms: 1.17x faster                                 |
| gc_traversal               | 5.70 ms                                                      | 5.03 ms: 1.13x faster                                 |
| async_tree_io              | 1.39 sec                                                     | 1.24 sec: 1.12x faster                                |
| pickle_dict                | 47.2 us                                                      | 42.8 us: 1.10x faster                                 |
| pickle                     | 15.1 us                                                      | 14.1 us: 1.07x faster                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 634 ms: 1.06x faster                                  |
| pickle_list                | 6.86 us                                                      | 6.56 us: 1.05x faster                                 |
| async_tree_none_tg         | 504 ms                                                       | 483 ms: 1.04x faster                                  |
| asyncio_websockets         | 766 ms                                                       | 737 ms: 1.04x faster                                  |
| regex_effbot               | 4.74 ms                                                      | 4.97 ms: 1.05x slower                                 |
| async_tree_memoization     | 709 ms                                                       | 744 ms: 1.05x slower                                  |
| sqlite_synth               | 3.99 us                                                      | 4.22 us: 1.06x slower                                 |
| async_tree_none            | 572 ms                                                       | 607 ms: 1.06x slower                                  |
| pidigits                   | 251 ms                                                       | 267 ms: 1.06x slower                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 909 ms: 1.07x slower                                  |
| regex_dna                  | 282 ms                                                       | 304 ms: 1.08x slower                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 961 ms: 1.08x slower                                  |
| pathlib                    | 29.9 ms                                                      | 33.6 ms: 1.12x slower                                 |
| regex_v8                   | 32.8 ms                                                      | 36.9 ms: 1.13x slower                                 |
| unpickle_list              | 6.68 us                                                      | 7.55 us: 1.13x slower                                 |
| asyncio_tcp                | 948 ms                                                       | 1.11 sec: 1.17x slower                                |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.33 sec: 1.20x slower                                |
| unpickle                   | 20.5 us                                                      | 24.7 us: 1.20x slower                                 |
| deepcopy                   | 498 us                                                       | 602 us: 1.21x slower                                  |
| telco                      | 12.2 ms                                                      | 14.8 ms: 1.21x slower                                 |
| docutils                   | 4.01 sec                                                     | 5.00 sec: 1.25x slower                                |
| python_startup_no_site     | 15.3 ms                                                      | 19.2 ms: 1.25x slower                                 |
| pylint                     | 470 ms                                                       | 591 ms: 1.26x slower                                  |
| async_generators           | 567 ms                                                       | 740 ms: 1.31x slower                                  |
| python_startup             | 22.4 ms                                                      | 29.3 ms: 1.31x slower                                 |
| mdp                        | 3.80 sec                                                     | 5.00 sec: 1.32x slower                                |
| json_dumps                 | 14.1 ms                                                      | 18.6 ms: 1.32x slower                                 |
| xml_etree_generate         | 122 ms                                                       | 162 ms: 1.32x slower                                  |
| json_loads                 | 34.3 us                                                      | 45.4 us: 1.33x slower                                 |
| tornado_http               | 251 ms                                                       | 337 ms: 1.34x slower                                  |
| generators                 | 40.0 ms                                                      | 53.8 ms: 1.34x slower                                 |
| json                       | 6.51 ms                                                      | 8.93 ms: 1.37x slower                                 |
| scimark_fft                | 473 ms                                                       | 651 ms: 1.38x slower                                  |
| meteor_contest             | 150 ms                                                       | 212 ms: 1.41x slower                                  |
| coroutines                 | 30.9 ms                                                      | 43.8 ms: 1.42x slower                                 |
| pycparser                  | 1.57 sec                                                     | 2.23 sec: 1.42x slower                                |
| deepcopy_memo              | 50.1 us                                                      | 72.1 us: 1.44x slower                                 |
| nqueens                    | 112 ms                                                       | 161 ms: 1.44x slower                                  |
| deepcopy_reduce            | 4.10 us                                                      | 5.96 us: 1.46x slower                                 |
| sympy_integrate            | 30.2 ms                                                      | 44.2 ms: 1.46x slower                                 |
| coverage                   | 107 ms                                                       | 157 ms: 1.47x slower                                  |
| fannkuch                   | 547 ms                                                       | 806 ms: 1.47x slower                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 9.98 ms: 1.48x slower                                 |
| 2to3                       | 445 ms                                                       | 666 ms: 1.50x slower                                  |
| tomli_loads                | 2.78 sec                                                     | 4.21 sec: 1.52x slower                                |
| crypto_pyaes               | 100 ms                                                       | 154 ms: 1.53x slower                                  |
| xml_etree_process          | 85.9 ms                                                      | 132 ms: 1.54x slower                                  |
| bench_thread_pool          | 2.89 ms                                                      | 4.44 ms: 1.54x slower                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 9.70 sec: 1.54x slower                                |
| spectral_norm              | 157 ms                                                       | 247 ms: 1.58x slower                                  |
| regex_compile              | 182 ms                                                       | 288 ms: 1.58x slower                                  |
| thrift                     | 1.10 ms                                                      | 1.78 ms: 1.62x slower                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 122 ms: 1.63x slower                                  |
| float                      | 116 ms                                                       | 190 ms: 1.64x slower                                  |
| pyflate                    | 664 ms                                                       | 1.10 sec: 1.66x slower                                |
| pprint_safe_repr           | 987 ms                                                       | 1.65 sec: 1.68x slower                                |
| sqlglot_normalize          | 140 ms                                                       | 237 ms: 1.70x slower                                  |
| typing_runtime_protocols   | 226 us                                                       | 383 us: 1.70x slower                                  |
| genshi_xml                 | 72.1 ms                                                      | 123 ms: 1.70x slower                                  |
| richards_super             | 73.2 ms                                                      | 127 ms: 1.73x slower                                  |
| html5lib                   | 92.6 ms                                                      | 162 ms: 1.74x slower                                  |
| logging_simple             | 8.56 us                                                      | 15.1 us: 1.76x slower                                 |
| pprint_pformat             | 1.94 sec                                                     | 3.44 sec: 1.77x slower                                |
| richards                   | 65.5 ms                                                      | 116 ms: 1.77x slower                                  |
| genshi_text                | 31.7 ms                                                      | 56.5 ms: 1.78x slower                                 |
| pickle_pure_python         | 416 us                                                       | 764 us: 1.83x slower                                  |
| sympy_str                  | 379 ms                                                       | 698 ms: 1.84x slower                                  |
| django_template            | 44.3 ms                                                      | 81.9 ms: 1.85x slower                                 |
| unpickle_pure_python       | 290 us                                                       | 537 us: 1.85x slower                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 168 ms: 1.85x slower                                  |
| comprehensions             | 22.2 us                                                      | 41.9 us: 1.88x slower                                 |
| mako                       | 15.9 ms                                                      | 30.3 ms: 1.90x slower                                 |
| scimark_sor                | 179 ms                                                       | 347 ms: 1.95x slower                                  |
| hexiom                     | 8.11 ms                                                      | 16.2 ms: 1.99x slower                                 |
| logging_format             | 9.24 us                                                      | 18.8 us: 2.03x slower                                 |
| logging_silent             | 130 ns                                                       | 267 ns: 2.05x slower                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 4.65 ms: 2.12x slower                                 |
| chaos                      | 83.6 ms                                                      | 179 ms: 2.14x slower                                  |
| sqlglot_parse              | 1.76 ms                                                      | 3.79 ms: 2.16x slower                                 |
| sympy_expand               | 601 ms                                                       | 1.30 sec: 2.16x slower                                |
| sympy_sum                  | 210 ms                                                       | 470 ms: 2.24x slower                                  |
| scimark_lu                 | 146 ms                                                       | 336 ms: 2.29x slower                                  |
| raytrace                   | 344 ms                                                       | 800 ms: 2.32x slower                                  |
| go                         | 191 ms                                                       | 457 ms: 2.39x slower                                  |
| nbody                      | 119 ms                                                       | 309 ms: 2.60x slower                                  |
| deltablue                  | 4.44 ms                                                      | 11.9 ms: 2.67x slower                                 |
| unpack_sequence            | 74.3 ns                                                      | 217 ns: 2.91x slower                                  |
| Geometric mean             | (ref)                                                        | 1.44x slower                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.14x