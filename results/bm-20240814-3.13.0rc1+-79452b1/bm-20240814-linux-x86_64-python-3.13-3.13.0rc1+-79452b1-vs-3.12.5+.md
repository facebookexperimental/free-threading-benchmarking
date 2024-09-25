# Results vs. 3.12.5+

- fork: python
- ref: 3.13
- machine: linux-x86_64
- commit hash: 79452b1
- commit date: 2024-08-14
- overall geometric mean: 1.03x faster
- HPT reliability: 99.87%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (5): 2to3, chameleon, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------------------|:----------------------------------------------------:|:-------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 576 ms: 1.42x faster                                    |
| async_tree_none_tg         | 726 ms                                               | 521 ms: 1.39x faster                                    |
| async_tree_memoization_tg  | 912 ms                                               | 672 ms: 1.36x faster                                    |
| async_tree_io              | 1.86 sec                                             | 1.38 sec: 1.35x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 849 ms: 1.32x faster                                    |
| async_tree_memoization     | 975 ms                                               | 745 ms: 1.31x faster                                    |
| async_tree_io_tg           | 1.87 sec                                             | 1.46 sec: 1.28x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 899 ms: 1.27x faster                                    |
| coroutines                 | 30.6 ms                                              | 29.2 ms: 1.05x faster                                   |
| async_generators           | 615 ms                                               | 592 ms: 1.04x faster                                    |
| Geometric mean             | (ref)                                                | 1.20x faster                                            |

Benchmark hidden because not significant (3): asyncio_tcp_ssl, asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:----------------------------------------------------:|:-------------------------------------------------------:|
| float          | 124 ms                                               | 115 ms: 1.08x faster                                    |
| pidigits       | 256 ms                                               | 248 ms: 1.04x faster                                    |
| nbody          | 117 ms                                               | 124 ms: 1.06x slower                                    |
| Geometric mean | (ref)                                                | 1.02x faster                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------|:----------------------------------------------------:|:-------------------------------------------------------:|
| regex_compile  | 186 ms                                               | 177 ms: 1.05x faster                                    |
| regex_effbot   | 5.02 ms                                              | 4.84 ms: 1.04x faster                                   |
| regex_dna      | 268 ms                                               | 288 ms: 1.07x slower                                    |
| regex_v8       | 29.9 ms                                              | 32.4 ms: 1.08x slower                                   |
| Geometric mean | (ref)                                                | 1.02x slower                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|--------------------|:----------------------------------------------------:|:-------------------------------------------------------:|
| xml_etree_generate | 138 ms                                               | 129 ms: 1.07x faster                                    |
| pickle_pure_python | 436 us                                               | 417 us: 1.05x faster                                    |
| tomli_loads        | 2.86 sec                                             | 2.80 sec: 1.02x faster                                  |
| json_dumps         | 14.0 ms                                              | 14.9 ms: 1.06x slower                                   |
| Geometric mean     | (ref)                                                | 1.01x faster                                            |

Benchmark hidden because not significant (10): pickle, xml_etree_parse, pickle_list, unpickle_pure_python, unpickle_list, unpickle, json_loads, xml_etree_iterparse, pickle_dict, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|------------------------|:----------------------------------------------------:|:-------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 14.6 ms: 1.11x faster                                   |
| Geometric mean         | (ref)                                                | 1.07x faster                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_xml, mako, django_template, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 |
|----------------------------|:----------------------------------------------------:|:-------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 576 ms: 1.42x faster                                    |
| async_tree_none_tg         | 726 ms                                               | 521 ms: 1.39x faster                                    |
| comprehensions             | 28.6 us                                              | 20.9 us: 1.37x faster                                   |
| async_tree_memoization_tg  | 912 ms                                               | 672 ms: 1.36x faster                                    |
| async_tree_io              | 1.86 sec                                             | 1.38 sec: 1.35x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 849 ms: 1.32x faster                                    |
| async_tree_memoization     | 975 ms                                               | 745 ms: 1.31x faster                                    |
| async_tree_io_tg           | 1.87 sec                                             | 1.46 sec: 1.28x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 899 ms: 1.27x faster                                    |
| raytrace                   | 405 ms                                               | 350 ms: 1.16x faster                                    |
| generators                 | 44.7 ms                                              | 39.2 ms: 1.14x faster                                   |
| bench_thread_pool          | 3.42 ms                                              | 3.06 ms: 1.12x faster                                   |
| python_startup_no_site     | 16.2 ms                                              | 14.6 ms: 1.11x faster                                   |
| crypto_pyaes               | 110 ms                                               | 99.8 ms: 1.10x faster                                   |
| bench_mp_pool              | 21.2 ms                                              | 19.4 ms: 1.10x faster                                   |
| json                       | 7.14 ms                                              | 6.55 ms: 1.09x faster                                   |
| chaos                      | 92.1 ms                                              | 84.7 ms: 1.09x faster                                   |
| gc_traversal               | 6.42 ms                                              | 5.91 ms: 1.09x faster                                   |
| float                      | 124 ms                                               | 115 ms: 1.08x faster                                    |
| bpe_tokeniser              | 6.76 sec                                             | 6.25 sec: 1.08x faster                                  |
| pathlib                    | 31.6 ms                                              | 29.3 ms: 1.08x faster                                   |
| logging_simple             | 9.68 us                                              | 8.98 us: 1.08x faster                                   |
| scimark_monte_carlo        | 96.8 ms                                              | 89.9 ms: 1.08x faster                                   |
| logging_silent             | 139 ns                                               | 130 ns: 1.07x faster                                    |
| nqueens                    | 116 ms                                               | 108 ms: 1.07x faster                                    |
| pycparser                  | 1.68 sec                                             | 1.57 sec: 1.07x faster                                  |
| xml_etree_generate         | 138 ms                                               | 129 ms: 1.07x faster                                    |
| dask                       | 916 ms                                               | 872 ms: 1.05x faster                                    |
| regex_compile              | 186 ms                                               | 177 ms: 1.05x faster                                    |
| coroutines                 | 30.6 ms                                              | 29.2 ms: 1.05x faster                                   |
| pickle_pure_python         | 436 us                                               | 417 us: 1.05x faster                                    |
| async_generators           | 615 ms                                               | 592 ms: 1.04x faster                                    |
| regex_effbot               | 5.02 ms                                              | 4.84 ms: 1.04x faster                                   |
| pidigits                   | 256 ms                                               | 248 ms: 1.04x faster                                    |
| tomli_loads                | 2.86 sec                                             | 2.80 sec: 1.02x faster                                  |
| fannkuch                   | 525 ms                                               | 543 ms: 1.03x slower                                    |
| richards                   | 62.8 ms                                              | 65.8 ms: 1.05x slower                                   |
| nbody                      | 117 ms                                               | 124 ms: 1.06x slower                                    |
| json_dumps                 | 14.0 ms                                              | 14.9 ms: 1.06x slower                                   |
| sympy_expand               | 591 ms                                               | 631 ms: 1.07x slower                                    |
| regex_dna                  | 268 ms                                               | 288 ms: 1.07x slower                                    |
| meteor_contest             | 146 ms                                               | 157 ms: 1.07x slower                                    |
| sqlite_synth               | 3.77 us                                              | 4.07 us: 1.08x slower                                   |
| regex_v8                   | 29.9 ms                                              | 32.4 ms: 1.08x slower                                   |
| aiohttp                    | 2.05 ms                                              | 2.23 ms: 1.09x slower                                   |
| richards_super             | 69.7 ms                                              | 76.3 ms: 1.10x slower                                   |
| go                         | 173 ms                                               | 195 ms: 1.13x slower                                    |
| coverage                   | 96.9 ms                                              | 110 ms: 1.14x slower                                    |
| spectral_norm              | 136 ms                                               | 159 ms: 1.17x slower                                    |
| gunicorn                   | 1.92 ms                                              | 2.25 ms: 1.17x slower                                   |
| telco                      | 9.53 ms                                              | 11.4 ms: 1.20x slower                                   |
| create_gc_cycles           | 2.00 ms                                              | 2.46 ms: 1.23x slower                                   |
| flaskblogging              | 6.97 ms                                              | 8.78 ms: 1.26x slower                                   |
| Geometric mean             | (ref)                                                | 1.03x faster                                            |

Benchmark hidden because not significant (49): tornado_http, sqlglot_optimize, dulwich_log, typing_runtime_protocols, 2to3, pickle, xml_etree_parse, sympy_str, sqlglot_parse, python_startup, pickle_list, unpickle_pure_python, unpickle_list, sympy_sum, html5lib, pylint, pprint_safe_repr, unpickle, genshi_xml, docutils, scimark_fft, asyncio_tcp_ssl, sqlglot_transpile, logging_format, scimark_lu, mako, deepcopy, pyflate, asyncio_tcp, pprint_pformat, json_loads, scimark_sparse_mat_mult, mdp, thrift, scimark_sor, deepcopy_memo, sqlglot_normalize, chameleon, hexiom, xml_etree_iterparse, deepcopy_reduce, pickle_dict, sympy_integrate, deltablue, asyncio_websockets, django_template, unpack_sequence, xml_etree_process, genshi_text
Ignored benchmarks (3) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.87% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x