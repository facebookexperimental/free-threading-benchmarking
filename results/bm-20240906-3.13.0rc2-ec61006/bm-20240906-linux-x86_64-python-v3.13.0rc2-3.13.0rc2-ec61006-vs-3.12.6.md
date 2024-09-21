# Results vs. 3.12.6

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.04x faster
- HPT reliability: 99.79%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| tornado_http   | 266 ms                                                 | 251 ms: 1.06x faster                                         |
| Geometric mean | (ref)                                                  | 1.01x faster                                                 |

Benchmark hidden because not significant (4): 2to3, chameleon, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none_tg         | 704 ms                                                 | 504 ms: 1.40x faster                                         |
| async_tree_memoization_tg  | 930 ms                                                 | 670 ms: 1.39x faster                                         |
| async_tree_io_tg           | 1.93 sec                                               | 1.40 sec: 1.38x faster                                       |
| async_tree_memoization     | 977 ms                                                 | 709 ms: 1.38x faster                                         |
| async_tree_io              | 1.85 sec                                               | 1.39 sec: 1.33x faster                                       |
| async_tree_none            | 741 ms                                                 | 572 ms: 1.30x faster                                         |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 852 ms: 1.29x faster                                         |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 889 ms: 1.21x faster                                         |
| async_generators           | 589 ms                                                 | 567 ms: 1.04x faster                                         |
| Geometric mean             | (ref)                                                  | 1.19x faster                                                 |

Benchmark hidden because not significant (4): asyncio_tcp_ssl, asyncio_websockets, asyncio_tcp, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 123 ms                                                 | 116 ms: 1.06x faster                                         |
| Geometric mean | (ref)                                                  | 1.02x faster                                                 |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.74 ms: 1.08x faster                                        |
| Geometric mean | (ref)                                                  | 1.02x faster                                                 |

Benchmark hidden because not significant (3): regex_compile, regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| pickle_dict    | 52.7 us                                                | 47.2 us: 1.12x faster                                        |
| json_loads     | 37.9 us                                                | 34.3 us: 1.10x faster                                        |
| pickle         | 16.4 us                                                | 15.1 us: 1.08x faster                                        |
| tomli_loads    | 2.88 sec                                               | 2.78 sec: 1.04x faster                                       |
| Geometric mean | (ref)                                                  | 1.04x faster                                                 |

Benchmark hidden because not significant (10): pickle_pure_python, xml_etree_parse, xml_etree_generate, unpickle, unpickle_pure_python, unpickle_list, pickle_list, json_dumps, xml_etree_process, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.3 ms: 1.15x faster                                        |
| python_startup         | 23.7 ms                                                | 22.4 ms: 1.06x faster                                        |
| Geometric mean         | (ref)                                                  | 1.10x faster                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 31.7 ms: 1.05x slower                                        |
| genshi_xml     | 67.6 ms                                                | 72.1 ms: 1.07x slower                                        |
| Geometric mean | (ref)                                                  | 1.03x slower                                                 |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none_tg         | 704 ms                                                 | 504 ms: 1.40x faster                                         |
| async_tree_memoization_tg  | 930 ms                                                 | 670 ms: 1.39x faster                                         |
| async_tree_io_tg           | 1.93 sec                                               | 1.40 sec: 1.38x faster                                       |
| async_tree_memoization     | 977 ms                                                 | 709 ms: 1.38x faster                                         |
| async_tree_io              | 1.85 sec                                               | 1.39 sec: 1.33x faster                                       |
| async_tree_none            | 741 ms                                                 | 572 ms: 1.30x faster                                         |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 852 ms: 1.29x faster                                         |
| comprehensions             | 27.1 us                                                | 22.2 us: 1.22x faster                                        |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 889 ms: 1.21x faster                                         |
| bench_thread_pool          | 3.48 ms                                                | 2.89 ms: 1.21x faster                                        |
| raytrace                   | 408 ms                                                 | 344 ms: 1.18x faster                                         |
| python_startup_no_site     | 17.6 ms                                                | 15.3 ms: 1.15x faster                                        |
| pycparser                  | 1.79 sec                                               | 1.57 sec: 1.14x faster                                       |
| sqlglot_normalize          | 157 ms                                                 | 140 ms: 1.12x faster                                         |
| pickle_dict                | 52.7 us                                                | 47.2 us: 1.12x faster                                        |
| bench_mp_pool              | 20.7 ms                                                | 18.7 ms: 1.11x faster                                        |
| json_loads                 | 37.9 us                                                | 34.3 us: 1.10x faster                                        |
| logging_simple             | 9.45 us                                                | 8.56 us: 1.10x faster                                        |
| pyflate                    | 727 ms                                                 | 664 ms: 1.10x faster                                         |
| regex_effbot               | 5.13 ms                                                | 4.74 ms: 1.08x faster                                        |
| pickle                     | 16.4 us                                                | 15.1 us: 1.08x faster                                        |
| logging_silent             | 139 ns                                                 | 130 ns: 1.07x faster                                         |
| crypto_pyaes               | 107 ms                                                 | 100 ms: 1.07x faster                                         |
| dulwich_log                | 100 ms                                                 | 93.7 ms: 1.07x faster                                        |
| sqlglot_transpile          | 2.34 ms                                                | 2.20 ms: 1.06x faster                                        |
| scimark_monte_carlo        | 96.4 ms                                                | 90.6 ms: 1.06x faster                                        |
| float                      | 123 ms                                                 | 116 ms: 1.06x faster                                         |
| tornado_http               | 266 ms                                                 | 251 ms: 1.06x faster                                         |
| python_startup             | 23.7 ms                                                | 22.4 ms: 1.06x faster                                        |
| pathlib                    | 31.6 ms                                                | 29.9 ms: 1.06x faster                                        |
| scimark_fft                | 500 ms                                                 | 473 ms: 1.06x faster                                         |
| sympy_sum                  | 222 ms                                                 | 210 ms: 1.06x faster                                         |
| json                       | 6.85 ms                                                | 6.51 ms: 1.05x faster                                        |
| bpe_tokeniser              | 6.59 sec                                               | 6.28 sec: 1.05x faster                                       |
| deepcopy_memo              | 52.4 us                                                | 50.1 us: 1.05x faster                                        |
| mdp                        | 3.97 sec                                               | 3.80 sec: 1.05x faster                                       |
| scimark_lu                 | 152 ms                                                 | 146 ms: 1.04x faster                                         |
| async_generators           | 589 ms                                                 | 567 ms: 1.04x faster                                         |
| tomli_loads                | 2.88 sec                                               | 2.78 sec: 1.04x faster                                       |
| deltablue                  | 4.27 ms                                                | 4.44 ms: 1.04x slower                                        |
| genshi_text                | 30.2 ms                                                | 31.7 ms: 1.05x slower                                        |
| deepcopy                   | 468 us                                                 | 498 us: 1.06x slower                                         |
| genshi_xml                 | 67.6 ms                                                | 72.1 ms: 1.07x slower                                        |
| scimark_sor                | 167 ms                                                 | 179 ms: 1.07x slower                                         |
| richards                   | 60.3 ms                                                | 65.5 ms: 1.09x slower                                        |
| go                         | 172 ms                                                 | 191 ms: 1.11x slower                                         |
| coverage                   | 95.4 ms                                                | 107 ms: 1.13x slower                                         |
| unpack_sequence            | 60.2 ns                                                | 74.3 ns: 1.23x slower                                        |
| create_gc_cycles           | 1.94 ms                                                | 2.41 ms: 1.24x slower                                        |
| telco                      | 9.59 ms                                                | 12.2 ms: 1.27x slower                                        |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                 |

Benchmark hidden because not significant (52): pickle_pure_python, nqueens, xml_etree_parse, xml_etree_generate, logging_format, unpickle, unpickle_pure_python, gc_traversal, generators, 2to3, regex_compile, unpickle_list, hexiom, pprint_pformat, sqlglot_parse, sqlglot_optimize, pickle_list, sympy_str, chaos, django_template, json_dumps, asyncio_tcp_ssl, nbody, chameleon, docutils, pidigits, typing_runtime_protocols, richards_super, spectral_norm, scimark_sparse_mat_mult, regex_v8, dask, pylint, fannkuch, regex_dna, mako, deepcopy_reduce, sympy_integrate, aiohttp, pprint_safe_repr, asyncio_websockets, meteor_contest, xml_etree_process, flaskblogging, asyncio_tcp, sqlite_synth, sympy_expand, thrift, html5lib, coroutines, xml_etree_iterparse, gunicorn
Ignored benchmarks (3) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.79% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x