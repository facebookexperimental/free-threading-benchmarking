# Results vs. 3.13.0rc2

- fork: python
- ref: v3.12.6
- machine: linux-x86_64
- commit hash: a4a2d2b
- commit date: 2024-09-06
- overall geometric mean: 1.04x slower
- HPT reliability: 99.79%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| tornado_http   | 251 ms                                                       | 266 ms: 1.06x slower                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                           |

Benchmark hidden because not significant (4): 2to3, chameleon, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| async_generators           | 567 ms                                                       | 589 ms: 1.04x slower                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 1.08 sec: 1.21x slower                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 1.10 sec: 1.29x slower                                 |
| async_tree_none            | 572 ms                                                       | 741 ms: 1.30x slower                                   |
| async_tree_io              | 1.39 sec                                                     | 1.85 sec: 1.33x slower                                 |
| async_tree_memoization     | 709 ms                                                       | 977 ms: 1.38x slower                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 1.93 sec: 1.38x slower                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 930 ms: 1.39x slower                                   |
| async_tree_none_tg         | 504 ms                                                       | 704 ms: 1.40x slower                                   |
| Geometric mean             | (ref)                                                        | 1.19x slower                                           |

Benchmark hidden because not significant (4): coroutines, asyncio_tcp, asyncio_websockets, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| float          | 116 ms                                                       | 123 ms: 1.06x slower                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                           |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 5.13 ms: 1.08x slower                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                           |

Benchmark hidden because not significant (3): regex_dna, regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| tomli_loads    | 2.78 sec                                                     | 2.88 sec: 1.04x slower                                 |
| pickle         | 15.1 us                                                      | 16.4 us: 1.08x slower                                  |
| json_loads     | 34.3 us                                                      | 37.9 us: 1.10x slower                                  |
| pickle_dict    | 47.2 us                                                      | 52.7 us: 1.12x slower                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                           |

Benchmark hidden because not significant (10): xml_etree_iterparse, xml_etree_process, json_dumps, pickle_list, unpickle_list, unpickle_pure_python, unpickle, xml_etree_generate, xml_etree_parse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 23.7 ms: 1.06x slower                                  |
| python_startup_no_site | 15.3 ms                                                      | 17.6 ms: 1.15x slower                                  |
| Geometric mean         | (ref)                                                        | 1.10x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml     | 72.1 ms                                                      | 67.6 ms: 1.07x faster                                  |
| genshi_text    | 31.7 ms                                                      | 30.2 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                           |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| telco                      | 12.2 ms                                                      | 9.59 ms: 1.27x faster                                  |
| create_gc_cycles           | 2.41 ms                                                      | 1.94 ms: 1.24x faster                                  |
| unpack_sequence            | 74.3 ns                                                      | 60.2 ns: 1.23x faster                                  |
| coverage                   | 107 ms                                                       | 95.4 ms: 1.13x faster                                  |
| go                         | 191 ms                                                       | 172 ms: 1.11x faster                                   |
| richards                   | 65.5 ms                                                      | 60.3 ms: 1.09x faster                                  |
| scimark_sor                | 179 ms                                                       | 167 ms: 1.07x faster                                   |
| genshi_xml                 | 72.1 ms                                                      | 67.6 ms: 1.07x faster                                  |
| deepcopy                   | 498 us                                                       | 468 us: 1.06x faster                                   |
| genshi_text                | 31.7 ms                                                      | 30.2 ms: 1.05x faster                                  |
| deltablue                  | 4.44 ms                                                      | 4.27 ms: 1.04x faster                                  |
| tomli_loads                | 2.78 sec                                                     | 2.88 sec: 1.04x slower                                 |
| async_generators           | 567 ms                                                       | 589 ms: 1.04x slower                                   |
| scimark_lu                 | 146 ms                                                       | 152 ms: 1.04x slower                                   |
| mdp                        | 3.80 sec                                                     | 3.97 sec: 1.05x slower                                 |
| deepcopy_memo              | 50.1 us                                                      | 52.4 us: 1.05x slower                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 6.59 sec: 1.05x slower                                 |
| json                       | 6.51 ms                                                      | 6.85 ms: 1.05x slower                                  |
| sympy_sum                  | 210 ms                                                       | 222 ms: 1.06x slower                                   |
| scimark_fft                | 473 ms                                                       | 500 ms: 1.06x slower                                   |
| pathlib                    | 29.9 ms                                                      | 31.6 ms: 1.06x slower                                  |
| python_startup             | 22.4 ms                                                      | 23.7 ms: 1.06x slower                                  |
| tornado_http               | 251 ms                                                       | 266 ms: 1.06x slower                                   |
| float                      | 116 ms                                                       | 123 ms: 1.06x slower                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 96.4 ms: 1.06x slower                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 2.34 ms: 1.06x slower                                  |
| dulwich_log                | 93.7 ms                                                      | 100 ms: 1.07x slower                                   |
| crypto_pyaes               | 100 ms                                                       | 107 ms: 1.07x slower                                   |
| logging_silent             | 130 ns                                                       | 139 ns: 1.07x slower                                   |
| pickle                     | 15.1 us                                                      | 16.4 us: 1.08x slower                                  |
| regex_effbot               | 4.74 ms                                                      | 5.13 ms: 1.08x slower                                  |
| pyflate                    | 664 ms                                                       | 727 ms: 1.10x slower                                   |
| logging_simple             | 8.56 us                                                      | 9.45 us: 1.10x slower                                  |
| json_loads                 | 34.3 us                                                      | 37.9 us: 1.10x slower                                  |
| bench_mp_pool              | 18.7 ms                                                      | 20.7 ms: 1.11x slower                                  |
| pickle_dict                | 47.2 us                                                      | 52.7 us: 1.12x slower                                  |
| sqlglot_normalize          | 140 ms                                                       | 157 ms: 1.12x slower                                   |
| pycparser                  | 1.57 sec                                                     | 1.79 sec: 1.14x slower                                 |
| python_startup_no_site     | 15.3 ms                                                      | 17.6 ms: 1.15x slower                                  |
| raytrace                   | 344 ms                                                       | 408 ms: 1.18x slower                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.48 ms: 1.21x slower                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 1.08 sec: 1.21x slower                                 |
| comprehensions             | 22.2 us                                                      | 27.1 us: 1.22x slower                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 1.10 sec: 1.29x slower                                 |
| async_tree_none            | 572 ms                                                       | 741 ms: 1.30x slower                                   |
| async_tree_io              | 1.39 sec                                                     | 1.85 sec: 1.33x slower                                 |
| async_tree_memoization     | 709 ms                                                       | 977 ms: 1.38x slower                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 1.93 sec: 1.38x slower                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 930 ms: 1.39x slower                                   |
| async_tree_none_tg         | 504 ms                                                       | 704 ms: 1.40x slower                                   |
| Geometric mean             | (ref)                                                        | 1.04x slower                                           |

Benchmark hidden because not significant (52): gunicorn, xml_etree_iterparse, coroutines, html5lib, thrift, sympy_expand, sqlite_synth, asyncio_tcp, flaskblogging, xml_etree_process, meteor_contest, asyncio_websockets, pprint_safe_repr, aiohttp, sympy_integrate, deepcopy_reduce, mako, regex_dna, fannkuch, pylint, dask, regex_v8, scimark_sparse_mat_mult, spectral_norm, richards_super, typing_runtime_protocols, pidigits, docutils, chameleon, nbody, asyncio_tcp_ssl, json_dumps, django_template, chaos, sympy_str, pickle_list, sqlglot_optimize, sqlglot_parse, pprint_pformat, hexiom, unpickle_list, regex_compile, 2to3, generators, gc_traversal, unpickle_pure_python, unpickle, logging_format, xml_etree_generate, xml_etree_parse, nqueens, pickle_pure_python
Ignored benchmarks (3) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.79% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x