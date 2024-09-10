# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d343f97
- commit date: 2024-09-06
- overall geometric mean: 1.03x faster
- HPT reliability: 97.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.89x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| html5lib       | 95.8 ms                                                               | 89.1 ms: 1.07x faster                                 |
| Geometric mean | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (3): 2to3, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 740 ms                                                                | 502 ms: 1.47x faster                                  |
| async_tree_memoization_tg  | 935 ms                                                                | 667 ms: 1.40x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 686 ms: 1.38x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 519 ms: 1.33x faster                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.39 sec: 1.30x faster                                |
| async_tree_io              | 1.79 sec                                                              | 1.39 sec: 1.28x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 888 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 887 ms: 1.24x faster                                  |
| async_generators           | 617 ms                                                                | 586 ms: 1.05x faster                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 2.99 sec: 1.07x slower                                |
| Geometric mean             | (ref)                                                                 | 1.19x faster                                          |

Benchmark hidden because not significant (3): coroutines, asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 127 ms                                                                | 120 ms: 1.06x faster                                  |
| pidigits       | 255 ms                                                                | 247 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                                 | 1.04x faster                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 287 ms                                                                | 297 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (3): regex_compile, regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle_pure_python | 319 us                                                                | 294 us: 1.08x faster                                  |
| tomli_loads          | 2.99 sec                                                              | 2.84 sec: 1.05x faster                                |
| pickle_dict          | 46.5 us                                                               | 49.2 us: 1.06x slower                                 |
| json_dumps           | 13.6 ms                                                               | 14.4 ms: 1.06x slower                                 |
| xml_etree_iterparse  | 157 ms                                                                | 170 ms: 1.08x slower                                  |
| pickle               | 14.8 us                                                               | 16.6 us: 1.12x slower                                 |
| json_loads           | 36.6 us                                                               | 41.2 us: 1.13x slower                                 |
| pickle_list          | 6.40 us                                                               | 7.57 us: 1.18x slower                                 |
| Geometric mean       | (ref)                                                                 | 1.03x slower                                          |

Benchmark hidden because not significant (6): xml_etree_process, xml_etree_generate, unpickle, xml_etree_parse, unpickle_list, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 17.8 ms: 1.10x slower                                 |
| python_startup         | 21.2 ms                                                               | 25.6 ms: 1.20x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.15x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text    | 31.9 ms                                                               | 34.1 ms: 1.07x slower                                 |
| mako           | 17.2 ms                                                               | 19.0 ms: 1.10x slower                                 |
| Geometric mean | (ref)                                                                 | 1.05x slower                                          |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| deepcopy                   | 503 us                                                                | 341 us: 1.48x faster                                  |
| async_tree_none            | 740 ms                                                                | 502 ms: 1.47x faster                                  |
| deepcopy_memo              | 57.5 us                                                               | 39.8 us: 1.45x faster                                 |
| async_tree_memoization_tg  | 935 ms                                                                | 667 ms: 1.40x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 686 ms: 1.38x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 519 ms: 1.33x faster                                  |
| async_tree_io_tg           | 1.80 sec                                                              | 1.39 sec: 1.30x faster                                |
| comprehensions             | 29.6 us                                                               | 23.0 us: 1.29x faster                                 |
| async_tree_io              | 1.79 sec                                                              | 1.39 sec: 1.28x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 888 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 887 ms: 1.24x faster                                  |
| deepcopy_reduce            | 4.45 us                                                               | 3.61 us: 1.23x faster                                 |
| crypto_pyaes               | 112 ms                                                                | 93.8 ms: 1.19x faster                                 |
| raytrace                   | 418 ms                                                                | 361 ms: 1.16x faster                                  |
| sympy_str                  | 425 ms                                                                | 373 ms: 1.14x faster                                  |
| chaos                      | 93.7 ms                                                               | 82.8 ms: 1.13x faster                                 |
| dulwich_log                | 114 ms                                                                | 101 ms: 1.13x faster                                  |
| logging_simple             | 9.89 us                                                               | 8.80 us: 1.12x faster                                 |
| sympy_expand               | 689 ms                                                                | 623 ms: 1.11x faster                                  |
| deltablue                  | 5.05 ms                                                               | 4.57 ms: 1.11x faster                                 |
| generators                 | 46.0 ms                                                               | 41.7 ms: 1.10x faster                                 |
| logging_format             | 11.8 us                                                               | 10.7 us: 1.10x faster                                 |
| unpack_sequence            | 68.5 ns                                                               | 62.2 ns: 1.10x faster                                 |
| go                         | 185 ms                                                                | 171 ms: 1.09x faster                                  |
| unpickle_pure_python       | 319 us                                                                | 294 us: 1.08x faster                                  |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 6.93 ms: 1.08x faster                                 |
| thrift                     | 1.17 ms                                                               | 1.09 ms: 1.08x faster                                 |
| html5lib                   | 95.8 ms                                                               | 89.1 ms: 1.07x faster                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 91.7 ms: 1.07x faster                                 |
| pathlib                    | 31.7 ms                                                               | 30.0 ms: 1.06x faster                                 |
| float                      | 127 ms                                                                | 120 ms: 1.06x faster                                  |
| sympy_integrate            | 31.4 ms                                                               | 29.8 ms: 1.05x faster                                 |
| async_generators           | 617 ms                                                                | 586 ms: 1.05x faster                                  |
| tomli_loads                | 2.99 sec                                                              | 2.84 sec: 1.05x faster                                |
| pycparser                  | 1.73 sec                                                              | 1.67 sec: 1.04x faster                                |
| pidigits                   | 255 ms                                                                | 247 ms: 1.03x faster                                  |
| regex_dna                  | 287 ms                                                                | 297 ms: 1.04x slower                                  |
| pprint_safe_repr           | 970 ms                                                                | 1.01 sec: 1.04x slower                                |
| pyflate                    | 661 ms                                                                | 690 ms: 1.04x slower                                  |
| pickle_dict                | 46.5 us                                                               | 49.2 us: 1.06x slower                                 |
| json_dumps                 | 13.6 ms                                                               | 14.4 ms: 1.06x slower                                 |
| mdp                        | 3.84 sec                                                              | 4.09 sec: 1.06x slower                                |
| genshi_text                | 31.9 ms                                                               | 34.1 ms: 1.07x slower                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 2.99 sec: 1.07x slower                                |
| sqlite_synth               | 3.75 us                                                               | 4.02 us: 1.07x slower                                 |
| sqlglot_parse              | 1.89 ms                                                               | 2.03 ms: 1.07x slower                                 |
| xml_etree_iterparse        | 157 ms                                                                | 170 ms: 1.08x slower                                  |
| logging_silent             | 135 ns                                                                | 146 ns: 1.08x slower                                  |
| richards_super             | 67.9 ms                                                               | 73.7 ms: 1.09x slower                                 |
| json                       | 6.68 ms                                                               | 7.28 ms: 1.09x slower                                 |
| python_startup_no_site     | 16.3 ms                                                               | 17.8 ms: 1.10x slower                                 |
| mako                       | 17.2 ms                                                               | 19.0 ms: 1.10x slower                                 |
| typing_runtime_protocols   | 199 us                                                                | 221 us: 1.11x slower                                  |
| pickle                     | 14.8 us                                                               | 16.6 us: 1.12x slower                                 |
| json_loads                 | 36.6 us                                                               | 41.2 us: 1.13x slower                                 |
| gc_traversal               | 5.61 ms                                                               | 6.35 ms: 1.13x slower                                 |
| pickle_list                | 6.40 us                                                               | 7.57 us: 1.18x slower                                 |
| coverage                   | 97.6 ms                                                               | 117 ms: 1.20x slower                                  |
| python_startup             | 21.2 ms                                                               | 25.6 ms: 1.20x slower                                 |
| telco                      | 9.71 ms                                                               | 11.9 ms: 1.22x slower                                 |
| bench_thread_pool          | 3.11 ms                                                               | 3.86 ms: 1.24x slower                                 |
| bench_mp_pool              | 18.4 ms                                                               | 22.8 ms: 1.24x slower                                 |
| create_gc_cycles           | 2.02 ms                                                               | 2.70 ms: 1.34x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.03x faster                                          |

Benchmark hidden because not significant (34): xml_etree_process, sqlglot_transpile, hexiom, sympy_sum, xml_etree_generate, pprint_pformat, regex_compile, bpe_tokeniser, nbody, sqlglot_optimize, sqlglot_normalize, richards, django_template, regex_effbot, scimark_fft, fannkuch, 2to3, pylint, unpickle, scimark_lu, docutils, spectral_norm, xml_etree_parse, scimark_sor, unpickle_list, coroutines, meteor_contest, pickle_pure_python, asyncio_websockets, tornado_http, regex_v8, genshi_xml, asyncio_tcp, nqueens
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 97.07% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.89x