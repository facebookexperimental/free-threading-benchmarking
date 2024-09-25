# Results vs. 3.12.5+

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.04x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| html5lib       | 100 ms                                               | 92.6 ms: 1.08x faster                                        |
| Geometric mean | (ref)                                                | 1.04x faster                                                 |

Benchmark hidden because not significant (4): 2to3, chameleon, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none_tg         | 726 ms                                               | 504 ms: 1.44x faster                                         |
| async_tree_none            | 820 ms                                               | 572 ms: 1.43x faster                                         |
| async_tree_memoization     | 975 ms                                               | 709 ms: 1.37x faster                                         |
| async_tree_memoization_tg  | 912 ms                                               | 670 ms: 1.36x faster                                         |
| async_tree_io              | 1.86 sec                                             | 1.39 sec: 1.34x faster                                       |
| async_tree_io_tg           | 1.87 sec                                             | 1.40 sec: 1.33x faster                                       |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 852 ms: 1.31x faster                                         |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 889 ms: 1.28x faster                                         |
| async_generators           | 615 ms                                               | 567 ms: 1.08x faster                                         |
| Geometric mean             | (ref)                                                | 1.22x faster                                                 |

Benchmark hidden because not significant (4): asyncio_tcp, asyncio_tcp_ssl, coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| float          | 124 ms                                               | 116 ms: 1.07x faster                                         |
| Geometric mean | (ref)                                                | 1.03x faster                                                 |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.74 ms: 1.06x faster                                        |
| regex_dna      | 268 ms                                               | 282 ms: 1.05x slower                                         |
| regex_v8       | 29.9 ms                                              | 32.8 ms: 1.10x slower                                        |
| Geometric mean | (ref)                                                | 1.01x slower                                                 |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_generate   | 138 ms                                               | 122 ms: 1.12x faster                                         |
| xml_etree_parse      | 244 ms                                               | 231 ms: 1.05x faster                                         |
| pickle               | 15.9 us                                              | 15.1 us: 1.05x faster                                        |
| json_loads           | 35.9 us                                              | 34.3 us: 1.05x faster                                        |
| unpickle_pure_python | 304 us                                               | 290 us: 1.05x faster                                         |
| tomli_loads          | 2.86 sec                                             | 2.78 sec: 1.03x faster                                       |
| pickle_dict          | 45.5 us                                              | 47.2 us: 1.04x slower                                        |
| Geometric mean       | (ref)                                                | 1.03x faster                                                 |

Benchmark hidden because not significant (7): unpickle, pickle_pure_python, unpickle_list, pickle_list, json_dumps, xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 15.3 ms: 1.06x faster                                        |
| Geometric mean         | (ref)                                                | 1.04x faster                                                 |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text    | 30.3 ms                                              | 31.7 ms: 1.04x slower                                        |
| Geometric mean | (ref)                                                | 1.01x slower                                                 |

Benchmark hidden because not significant (3): django_template, mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none_tg         | 726 ms                                               | 504 ms: 1.44x faster                                         |
| async_tree_none            | 820 ms                                               | 572 ms: 1.43x faster                                         |
| async_tree_memoization     | 975 ms                                               | 709 ms: 1.37x faster                                         |
| async_tree_memoization_tg  | 912 ms                                               | 670 ms: 1.36x faster                                         |
| async_tree_io              | 1.86 sec                                             | 1.39 sec: 1.34x faster                                       |
| async_tree_io_tg           | 1.87 sec                                             | 1.40 sec: 1.33x faster                                       |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 852 ms: 1.31x faster                                         |
| comprehensions             | 28.6 us                                              | 22.2 us: 1.29x faster                                        |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 889 ms: 1.28x faster                                         |
| bench_thread_pool          | 3.42 ms                                              | 2.89 ms: 1.19x faster                                        |
| raytrace                   | 405 ms                                               | 344 ms: 1.17x faster                                         |
| bench_mp_pool              | 21.2 ms                                              | 18.7 ms: 1.14x faster                                        |
| logging_simple             | 9.68 us                                              | 8.56 us: 1.13x faster                                        |
| gc_traversal               | 6.42 ms                                              | 5.70 ms: 1.13x faster                                        |
| xml_etree_generate         | 138 ms                                               | 122 ms: 1.12x faster                                         |
| generators                 | 44.7 ms                                              | 40.0 ms: 1.12x faster                                        |
| dulwich_log                | 104 ms                                               | 93.7 ms: 1.11x faster                                        |
| chaos                      | 92.1 ms                                              | 83.6 ms: 1.10x faster                                        |
| json                       | 7.14 ms                                              | 6.51 ms: 1.10x faster                                        |
| crypto_pyaes               | 110 ms                                               | 100 ms: 1.09x faster                                         |
| async_generators           | 615 ms                                               | 567 ms: 1.08x faster                                         |
| html5lib                   | 100 ms                                               | 92.6 ms: 1.08x faster                                        |
| bpe_tokeniser              | 6.76 sec                                             | 6.28 sec: 1.08x faster                                       |
| float                      | 124 ms                                               | 116 ms: 1.07x faster                                         |
| sqlglot_optimize           | 80.2 ms                                              | 74.7 ms: 1.07x faster                                        |
| logging_silent             | 139 ns                                               | 130 ns: 1.07x faster                                         |
| scimark_monte_carlo        | 96.8 ms                                              | 90.6 ms: 1.07x faster                                        |
| pycparser                  | 1.68 sec                                             | 1.57 sec: 1.07x faster                                       |
| regex_effbot               | 5.02 ms                                              | 4.74 ms: 1.06x faster                                        |
| scimark_lu                 | 155 ms                                               | 146 ms: 1.06x faster                                         |
| python_startup_no_site     | 16.2 ms                                              | 15.3 ms: 1.06x faster                                        |
| pathlib                    | 31.6 ms                                              | 29.9 ms: 1.06x faster                                        |
| sqlglot_transpile          | 2.32 ms                                              | 2.20 ms: 1.06x faster                                        |
| sqlglot_parse              | 1.85 ms                                              | 1.76 ms: 1.06x faster                                        |
| xml_etree_parse            | 244 ms                                               | 231 ms: 1.05x faster                                         |
| pickle                     | 15.9 us                                              | 15.1 us: 1.05x faster                                        |
| json_loads                 | 35.9 us                                              | 34.3 us: 1.05x faster                                        |
| unpickle_pure_python       | 304 us                                               | 290 us: 1.05x faster                                         |
| tomli_loads                | 2.86 sec                                             | 2.78 sec: 1.03x faster                                       |
| pprint_pformat             | 1.99 sec                                             | 1.94 sec: 1.02x faster                                       |
| pickle_dict                | 45.5 us                                              | 47.2 us: 1.04x slower                                        |
| fannkuch                   | 525 ms                                               | 547 ms: 1.04x slower                                         |
| genshi_text                | 30.3 ms                                              | 31.7 ms: 1.04x slower                                        |
| scimark_sor                | 170 ms                                               | 179 ms: 1.05x slower                                         |
| regex_dna                  | 268 ms                                               | 282 ms: 1.05x slower                                         |
| richards_super             | 69.7 ms                                              | 73.2 ms: 1.05x slower                                        |
| sqlite_synth               | 3.77 us                                              | 3.99 us: 1.06x slower                                        |
| regex_v8                   | 29.9 ms                                              | 32.8 ms: 1.10x slower                                        |
| flaskblogging              | 6.97 ms                                              | 7.68 ms: 1.10x slower                                        |
| go                         | 173 ms                                               | 191 ms: 1.10x slower                                         |
| coverage                   | 96.9 ms                                              | 107 ms: 1.11x slower                                         |
| spectral_norm              | 136 ms                                               | 157 ms: 1.15x slower                                         |
| create_gc_cycles           | 2.00 ms                                              | 2.41 ms: 1.21x slower                                        |
| telco                      | 9.53 ms                                              | 12.2 ms: 1.28x slower                                        |
| Geometric mean             | (ref)                                                | 1.04x faster                                                 |

Benchmark hidden because not significant (48): unpickle, pickle_pure_python, asyncio_tcp, tornado_http, dask, sympy_sum, logging_format, nqueens, chameleon, sqlglot_normalize, scimark_sparse_mat_mult, django_template, 2to3, unpickle_list, regex_compile, pylint, pidigits, pickle_list, deepcopy_reduce, deepcopy_memo, scimark_fft, asyncio_tcp_ssl, python_startup, mako, docutils, hexiom, aiohttp, gunicorn, thrift, deltablue, sympy_str, pyflate, typing_runtime_protocols, json_dumps, mdp, coroutines, pprint_safe_repr, sympy_expand, nbody, asyncio_websockets, deepcopy, xml_etree_iterparse, meteor_contest, xml_etree_process, richards, genshi_xml, sympy_integrate, unpack_sequence
Ignored benchmarks (3) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x