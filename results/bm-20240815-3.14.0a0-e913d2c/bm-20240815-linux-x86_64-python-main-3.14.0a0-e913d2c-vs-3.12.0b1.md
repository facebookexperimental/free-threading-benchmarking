# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e913d2c
- commit date: 2024-08-15
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.88x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 422 ms: 1.05x faster                                  |
| tornado_http   | 262 ms                                                                | 241 ms: 1.09x faster                                  |
| Geometric mean | (ref)                                                                 | 1.04x faster                                          |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none_tg         | 692 ms                                                                | 466 ms: 1.49x faster                                  |
| async_tree_none            | 740 ms                                                                | 508 ms: 1.46x faster                                  |
| async_tree_memoization_tg  | 935 ms                                                                | 650 ms: 1.44x faster                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.27 sec: 1.42x faster                                |
| async_tree_memoization     | 949 ms                                                                | 670 ms: 1.42x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.29 sec: 1.39x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 857 ms: 1.32x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 847 ms: 1.30x faster                                  |
| async_generators           | 617 ms                                                                | 574 ms: 1.07x faster                                  |
| asyncio_websockets         | 766 ms                                                                | 734 ms: 1.04x faster                                  |
| coroutines                 | 30.1 ms                                                               | 31.3 ms: 1.04x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.24x faster                                          |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| nbody          | 125 ms                                                                | 116 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                                 | 1.04x faster                                          |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 197 ms                                                                | 175 ms: 1.12x faster                                  |
| regex_effbot   | 4.97 ms                                                               | 5.30 ms: 1.07x slower                                 |
| regex_v8       | 31.1 ms                                                               | 35.4 ms: 1.14x slower                                 |
| Geometric mean | (ref)                                                                 | 1.02x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle_pure_python | 319 us                                                                | 275 us: 1.16x faster                                  |
| tomli_loads          | 2.99 sec                                                              | 2.73 sec: 1.10x faster                                |
| xml_etree_generate   | 128 ms                                                                | 121 ms: 1.06x faster                                  |
| xml_etree_iterparse  | 157 ms                                                                | 166 ms: 1.05x slower                                  |
| pickle_list          | 6.40 us                                                               | 6.78 us: 1.06x slower                                 |
| pickle               | 14.8 us                                                               | 15.7 us: 1.06x slower                                 |
| json_dumps           | 13.6 ms                                                               | 15.7 ms: 1.16x slower                                 |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (7): pickle_pure_python, xml_etree_parse, xml_etree_process, pickle_dict, json_loads, unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 15.4 ms: 1.06x faster                                 |
| python_startup         | 21.2 ms                                                               | 22.6 ms: 1.06x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                          |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): django_template, genshi_xml, mako, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none_tg         | 692 ms                                                                | 466 ms: 1.49x faster                                  |
| async_tree_none            | 740 ms                                                                | 508 ms: 1.46x faster                                  |
| deepcopy_memo              | 57.5 us                                                               | 39.8 us: 1.44x faster                                 |
| async_tree_memoization_tg  | 935 ms                                                                | 650 ms: 1.44x faster                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.27 sec: 1.42x faster                                |
| async_tree_memoization     | 949 ms                                                                | 670 ms: 1.42x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.29 sec: 1.39x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 857 ms: 1.32x faster                                  |
| comprehensions             | 29.6 us                                                               | 22.4 us: 1.32x faster                                 |
| deepcopy                   | 503 us                                                                | 383 us: 1.31x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 847 ms: 1.30x faster                                  |
| raytrace                   | 418 ms                                                                | 328 ms: 1.28x faster                                  |
| logging_format             | 11.8 us                                                               | 9.52 us: 1.24x faster                                 |
| logging_simple             | 9.89 us                                                               | 8.33 us: 1.19x faster                                 |
| deepcopy_reduce            | 4.45 us                                                               | 3.83 us: 1.16x faster                                 |
| unpickle_pure_python       | 319 us                                                                | 275 us: 1.16x faster                                  |
| sympy_str                  | 425 ms                                                                | 370 ms: 1.15x faster                                  |
| sympy_integrate            | 31.4 ms                                                               | 27.3 ms: 1.15x faster                                 |
| chaos                      | 93.7 ms                                                               | 81.7 ms: 1.15x faster                                 |
| deltablue                  | 5.05 ms                                                               | 4.42 ms: 1.14x faster                                 |
| pathlib                    | 31.7 ms                                                               | 28.0 ms: 1.13x faster                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 6.60 ms: 1.13x faster                                 |
| generators                 | 46.0 ms                                                               | 41.0 ms: 1.12x faster                                 |
| regex_compile              | 197 ms                                                                | 175 ms: 1.12x faster                                  |
| scimark_monte_carlo        | 98.5 ms                                                               | 88.7 ms: 1.11x faster                                 |
| sympy_expand               | 689 ms                                                                | 622 ms: 1.11x faster                                  |
| tomli_loads                | 2.99 sec                                                              | 2.73 sec: 1.10x faster                                |
| tornado_http               | 262 ms                                                                | 241 ms: 1.09x faster                                  |
| nbody                      | 125 ms                                                                | 116 ms: 1.07x faster                                  |
| async_generators           | 617 ms                                                                | 574 ms: 1.07x faster                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 71.7 ms: 1.07x faster                                 |
| xml_etree_generate         | 128 ms                                                                | 121 ms: 1.06x faster                                  |
| crypto_pyaes               | 112 ms                                                                | 106 ms: 1.06x faster                                  |
| python_startup_no_site     | 16.3 ms                                                               | 15.4 ms: 1.06x faster                                 |
| 2to3                       | 444 ms                                                                | 422 ms: 1.05x faster                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 6.31 sec: 1.05x faster                                |
| sqlglot_parse              | 1.89 ms                                                               | 1.81 ms: 1.05x faster                                 |
| asyncio_websockets         | 766 ms                                                                | 734 ms: 1.04x faster                                  |
| hexiom                     | 8.87 ms                                                               | 8.52 ms: 1.04x faster                                 |
| pycparser                  | 1.73 sec                                                              | 1.67 sec: 1.04x faster                                |
| mdp                        | 3.84 sec                                                              | 3.71 sec: 1.04x faster                                |
| fannkuch                   | 551 ms                                                                | 532 ms: 1.04x faster                                  |
| pprint_pformat             | 2.03 sec                                                              | 1.96 sec: 1.03x faster                                |
| coroutines                 | 30.1 ms                                                               | 31.3 ms: 1.04x slower                                 |
| richards_super             | 67.9 ms                                                               | 71.2 ms: 1.05x slower                                 |
| xml_etree_iterparse        | 157 ms                                                                | 166 ms: 1.05x slower                                  |
| nqueens                    | 110 ms                                                                | 116 ms: 1.06x slower                                  |
| go                         | 185 ms                                                                | 196 ms: 1.06x slower                                  |
| pickle_list                | 6.40 us                                                               | 6.78 us: 1.06x slower                                 |
| pickle                     | 14.8 us                                                               | 15.7 us: 1.06x slower                                 |
| python_startup             | 21.2 ms                                                               | 22.6 ms: 1.06x slower                                 |
| regex_effbot               | 4.97 ms                                                               | 5.30 ms: 1.07x slower                                 |
| bench_mp_pool              | 18.4 ms                                                               | 19.8 ms: 1.08x slower                                 |
| json                       | 6.68 ms                                                               | 7.54 ms: 1.13x slower                                 |
| regex_v8                   | 31.1 ms                                                               | 35.4 ms: 1.14x slower                                 |
| bench_thread_pool          | 3.11 ms                                                               | 3.58 ms: 1.15x slower                                 |
| telco                      | 9.71 ms                                                               | 11.2 ms: 1.15x slower                                 |
| json_dumps                 | 13.6 ms                                                               | 15.7 ms: 1.16x slower                                 |
| typing_runtime_protocols   | 199 us                                                                | 233 us: 1.17x slower                                  |
| coverage                   | 97.6 ms                                                               | 117 ms: 1.20x slower                                  |
| create_gc_cycles           | 2.02 ms                                                               | 2.51 ms: 1.24x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                          |

Benchmark hidden because not significant (35): float, pylint, pickle_pure_python, django_template, unpack_sequence, genshi_xml, sqlglot_transpile, html5lib, spectral_norm, scimark_lu, scimark_sor, pprint_safe_repr, mako, xml_etree_parse, docutils, sqlglot_normalize, pidigits, logging_silent, richards, asyncio_tcp, sympy_sum, xml_etree_process, meteor_contest, asyncio_tcp_ssl, sqlite_synth, genshi_text, gc_traversal, thrift, regex_dna, pyflate, scimark_fft, pickle_dict, json_loads, unpickle, unpickle_list
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.88x