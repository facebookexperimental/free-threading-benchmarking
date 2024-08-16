# Results vs. 3.12.0b1

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.04x faster
- HPT reliability: 99.93%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.88x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 740 ms                                                                | 501 ms: 1.48x faster                                                  |
| async_tree_memoization_tg  | 935 ms                                                                | 650 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 692 ms                                                                | 485 ms: 1.43x faster                                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.30 sec: 1.39x faster                                                |
| async_tree_io              | 1.79 sec                                                              | 1.29 sec: 1.39x faster                                                |
| async_tree_memoization     | 949 ms                                                                | 705 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 829 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 856 ms: 1.33x faster                                                  |
| async_generators           | 617 ms                                                                | 579 ms: 1.07x faster                                                  |
| coroutines                 | 30.1 ms                                                               | 32.6 ms: 1.08x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.22x faster                                                          |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 127 ms                                                                | 119 ms: 1.06x faster                                                  |
| pidigits       | 255 ms                                                                | 245 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.04x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 287 ms                                                                | 300 ms: 1.05x slower                                                  |
| regex_effbot   | 4.97 ms                                                               | 5.47 ms: 1.10x slower                                                 |
| regex_v8       | 31.1 ms                                                               | 38.1 ms: 1.22x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.08x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.99 sec                                                              | 2.66 sec: 1.12x faster                                                |
| unpickle_pure_python | 319 us                                                                | 295 us: 1.08x faster                                                  |
| unpickle_list        | 7.19 us                                                               | 6.83 us: 1.05x faster                                                 |
| pickle               | 14.8 us                                                               | 15.4 us: 1.04x slower                                                 |
| pickle_list          | 6.40 us                                                               | 6.74 us: 1.05x slower                                                 |
| xml_etree_iterparse  | 157 ms                                                                | 167 ms: 1.06x slower                                                  |
| json_dumps           | 13.6 ms                                                               | 14.5 ms: 1.07x slower                                                 |
| unpickle             | 19.7 us                                                               | 21.7 us: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                          |

Benchmark hidden because not significant (6): xml_etree_generate, pickle_pure_python, xml_etree_parse, pickle_dict, xml_etree_process, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 14.9 ms: 1.09x faster                                                 |
| python_startup         | 21.2 ms                                                               | 23.8 ms: 1.12x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.01x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 17.2 ms                                                               | 18.3 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (3): genshi_xml, django_template, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 740 ms                                                                | 501 ms: 1.48x faster                                                  |
| async_tree_memoization_tg  | 935 ms                                                                | 650 ms: 1.44x faster                                                  |
| deepcopy_memo              | 57.5 us                                                               | 40.2 us: 1.43x faster                                                 |
| async_tree_none_tg         | 692 ms                                                                | 485 ms: 1.43x faster                                                  |
| deepcopy                   | 503 us                                                                | 359 us: 1.40x faster                                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.30 sec: 1.39x faster                                                |
| async_tree_io              | 1.79 sec                                                              | 1.29 sec: 1.39x faster                                                |
| async_tree_memoization     | 949 ms                                                                | 705 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 829 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 856 ms: 1.33x faster                                                  |
| comprehensions             | 29.6 us                                                               | 24.0 us: 1.23x faster                                                 |
| raytrace                   | 418 ms                                                                | 340 ms: 1.23x faster                                                  |
| deepcopy_reduce            | 4.45 us                                                               | 3.63 us: 1.23x faster                                                 |
| logging_simple             | 9.89 us                                                               | 8.46 us: 1.17x faster                                                 |
| logging_format             | 11.8 us                                                               | 10.2 us: 1.16x faster                                                 |
| sympy_str                  | 425 ms                                                                | 372 ms: 1.14x faster                                                  |
| deltablue                  | 5.05 ms                                                               | 4.43 ms: 1.14x faster                                                 |
| sympy_expand               | 689 ms                                                                | 606 ms: 1.14x faster                                                  |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 6.59 ms: 1.13x faster                                                 |
| tomli_loads                | 2.99 sec                                                              | 2.66 sec: 1.12x faster                                                |
| sympy_integrate            | 31.4 ms                                                               | 28.1 ms: 1.12x faster                                                 |
| unpack_sequence            | 68.5 ns                                                               | 61.3 ns: 1.12x faster                                                 |
| generators                 | 46.0 ms                                                               | 41.5 ms: 1.11x faster                                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 89.4 ms: 1.10x faster                                                 |
| python_startup_no_site     | 16.3 ms                                                               | 14.9 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 6.63 sec                                                              | 6.08 sec: 1.09x faster                                                |
| unpickle_pure_python       | 319 us                                                                | 295 us: 1.08x faster                                                  |
| crypto_pyaes               | 112 ms                                                                | 105 ms: 1.07x faster                                                  |
| pathlib                    | 31.7 ms                                                               | 29.7 ms: 1.07x faster                                                 |
| meteor_contest             | 149 ms                                                                | 139 ms: 1.07x faster                                                  |
| async_generators           | 617 ms                                                                | 579 ms: 1.07x faster                                                  |
| float                      | 127 ms                                                                | 119 ms: 1.06x faster                                                  |
| chaos                      | 93.7 ms                                                               | 88.2 ms: 1.06x faster                                                 |
| unpickle_list              | 7.19 us                                                               | 6.83 us: 1.05x faster                                                 |
| scimark_fft                | 499 ms                                                                | 476 ms: 1.05x faster                                                  |
| nqueens                    | 110 ms                                                                | 105 ms: 1.05x faster                                                  |
| pprint_pformat             | 2.03 sec                                                              | 1.94 sec: 1.04x faster                                                |
| hexiom                     | 8.87 ms                                                               | 8.52 ms: 1.04x faster                                                 |
| pidigits                   | 255 ms                                                                | 245 ms: 1.04x faster                                                  |
| pycparser                  | 1.73 sec                                                              | 1.67 sec: 1.04x faster                                                |
| mdp                        | 3.84 sec                                                              | 3.71 sec: 1.04x faster                                                |
| fannkuch                   | 551 ms                                                                | 534 ms: 1.03x faster                                                  |
| pprint_safe_repr           | 970 ms                                                                | 995 ms: 1.03x slower                                                  |
| pyflate                    | 661 ms                                                                | 682 ms: 1.03x slower                                                  |
| pickle                     | 14.8 us                                                               | 15.4 us: 1.04x slower                                                 |
| regex_dna                  | 287 ms                                                                | 300 ms: 1.05x slower                                                  |
| pickle_list                | 6.40 us                                                               | 6.74 us: 1.05x slower                                                 |
| mako                       | 17.2 ms                                                               | 18.3 ms: 1.06x slower                                                 |
| xml_etree_iterparse        | 157 ms                                                                | 167 ms: 1.06x slower                                                  |
| go                         | 185 ms                                                                | 198 ms: 1.07x slower                                                  |
| json_dumps                 | 13.6 ms                                                               | 14.5 ms: 1.07x slower                                                 |
| coroutines                 | 30.1 ms                                                               | 32.6 ms: 1.08x slower                                                 |
| richards                   | 63.4 ms                                                               | 69.2 ms: 1.09x slower                                                 |
| sqlite_synth               | 3.75 us                                                               | 4.10 us: 1.09x slower                                                 |
| typing_runtime_protocols   | 199 us                                                                | 218 us: 1.10x slower                                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 83.9 ms: 1.10x slower                                                 |
| unpickle                   | 19.7 us                                                               | 21.7 us: 1.10x slower                                                 |
| regex_effbot               | 4.97 ms                                                               | 5.47 ms: 1.10x slower                                                 |
| bench_thread_pool          | 3.11 ms                                                               | 3.44 ms: 1.11x slower                                                 |
| richards_super             | 67.9 ms                                                               | 76.3 ms: 1.12x slower                                                 |
| python_startup             | 21.2 ms                                                               | 23.8 ms: 1.12x slower                                                 |
| bench_mp_pool              | 18.4 ms                                                               | 21.4 ms: 1.16x slower                                                 |
| telco                      | 9.71 ms                                                               | 11.5 ms: 1.18x slower                                                 |
| create_gc_cycles           | 2.02 ms                                                               | 2.41 ms: 1.19x slower                                                 |
| coverage                   | 97.6 ms                                                               | 117 ms: 1.20x slower                                                  |
| regex_v8                   | 31.1 ms                                                               | 38.1 ms: 1.22x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.04x faster                                                          |

Benchmark hidden because not significant (30): pylint, xml_etree_generate, nbody, pickle_pure_python, regex_compile, genshi_xml, thrift, asyncio_tcp, html5lib, xml_etree_parse, sqlglot_normalize, sympy_sum, tornado_http, pickle_dict, asyncio_tcp_ssl, django_template, gc_traversal, spectral_norm, scimark_sor, sqlglot_parse, asyncio_websockets, genshi_text, 2to3, json, xml_etree_process, scimark_lu, docutils, logging_silent, json_loads, sqlglot_transpile
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.93% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.88x