# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e913d2c
- commit date: 2024-08-15
- overall geometric mean: 1.04x faster
- HPT reliability: 99.76%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 422 ms: 1.08x faster                                  |
| tornado_http   | 261 ms                                               | 241 ms: 1.09x faster                                  |
| Geometric mean | (ref)                                                | 1.06x faster                                          |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 508 ms: 1.61x faster                                  |
| async_tree_none_tg         | 726 ms                                               | 466 ms: 1.56x faster                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.27 sec: 1.47x faster                                |
| async_tree_memoization     | 975 ms                                               | 670 ms: 1.46x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.29 sec: 1.45x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 650 ms: 1.40x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 857 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 847 ms: 1.32x faster                                  |
| async_generators           | 615 ms                                               | 574 ms: 1.07x faster                                  |
| Geometric mean             | (ref)                                                | 1.26x faster                                          |

Benchmark hidden because not significant (4): asyncio_tcp, asyncio_websockets, asyncio_tcp_ssl, coroutines

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 186 ms                                               | 175 ms: 1.06x faster                                  |
| regex_dna      | 268 ms                                               | 292 ms: 1.09x slower                                  |
| regex_v8       | 29.9 ms                                              | 35.4 ms: 1.18x slower                                 |
| Geometric mean | (ref)                                                | 1.06x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_generate   | 138 ms                                               | 121 ms: 1.14x faster                                  |
| unpickle_pure_python | 304 us                                               | 275 us: 1.10x faster                                  |
| xml_etree_parse      | 244 ms                                               | 227 ms: 1.07x faster                                  |
| unpickle             | 21.6 us                                              | 20.4 us: 1.06x faster                                 |
| tomli_loads          | 2.86 sec                                             | 2.73 sec: 1.05x faster                                |
| xml_etree_process    | 82.7 ms                                              | 86.3 ms: 1.04x slower                                 |
| pickle_dict          | 45.5 us                                              | 47.7 us: 1.05x slower                                 |
| json_loads           | 35.9 us                                              | 37.6 us: 1.05x slower                                 |
| json_dumps           | 14.0 ms                                              | 15.7 ms: 1.12x slower                                 |
| unpickle_list        | 6.83 us                                              | 7.68 us: 1.12x slower                                 |
| Geometric mean       | (ref)                                                | 1.01x faster                                          |

Benchmark hidden because not significant (4): xml_etree_iterparse, pickle_list, pickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 15.4 ms: 1.05x faster                                 |
| Geometric mean         | (ref)                                                | 1.03x faster                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| mako           | 16.1 ms                                              | 17.0 ms: 1.06x slower                                 |
| genshi_text    | 30.3 ms                                              | 32.4 ms: 1.07x slower                                 |
| Geometric mean | (ref)                                                | 1.05x slower                                          |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 508 ms: 1.61x faster                                  |
| async_tree_none_tg         | 726 ms                                               | 466 ms: 1.56x faster                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.27 sec: 1.47x faster                                |
| async_tree_memoization     | 975 ms                                               | 670 ms: 1.46x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.29 sec: 1.45x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 650 ms: 1.40x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 857 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 847 ms: 1.32x faster                                  |
| deepcopy_memo              | 51.0 us                                              | 39.8 us: 1.28x faster                                 |
| comprehensions             | 28.6 us                                              | 22.4 us: 1.28x faster                                 |
| deepcopy                   | 486 us                                               | 383 us: 1.27x faster                                  |
| raytrace                   | 405 ms                                               | 328 ms: 1.23x faster                                  |
| logging_simple             | 9.68 us                                              | 8.33 us: 1.16x faster                                 |
| xml_etree_generate         | 138 ms                                               | 121 ms: 1.14x faster                                  |
| pathlib                    | 31.6 ms                                              | 28.0 ms: 1.13x faster                                 |
| chaos                      | 92.1 ms                                              | 81.7 ms: 1.13x faster                                 |
| gc_traversal               | 6.42 ms                                              | 5.70 ms: 1.13x faster                                 |
| sqlglot_optimize           | 80.2 ms                                              | 71.7 ms: 1.12x faster                                 |
| unpickle_pure_python       | 304 us                                               | 275 us: 1.10x faster                                  |
| generators                 | 44.7 ms                                              | 41.0 ms: 1.09x faster                                 |
| deepcopy_reduce            | 4.18 us                                              | 3.83 us: 1.09x faster                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 88.7 ms: 1.09x faster                                 |
| tornado_http               | 261 ms                                               | 241 ms: 1.09x faster                                  |
| 2to3                       | 456 ms                                               | 422 ms: 1.08x faster                                  |
| xml_etree_parse            | 244 ms                                               | 227 ms: 1.07x faster                                  |
| bpe_tokeniser              | 6.76 sec                                             | 6.31 sec: 1.07x faster                                |
| async_generators           | 615 ms                                               | 574 ms: 1.07x faster                                  |
| regex_compile              | 186 ms                                               | 175 ms: 1.06x faster                                  |
| sympy_integrate            | 29.0 ms                                              | 27.3 ms: 1.06x faster                                 |
| unpickle                   | 21.6 us                                              | 20.4 us: 1.06x faster                                 |
| python_startup_no_site     | 16.2 ms                                              | 15.4 ms: 1.05x faster                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 6.60 ms: 1.05x faster                                 |
| tomli_loads                | 2.86 sec                                             | 2.73 sec: 1.05x faster                                |
| hexiom                     | 8.19 ms                                              | 8.52 ms: 1.04x slower                                 |
| xml_etree_process          | 82.7 ms                                              | 86.3 ms: 1.04x slower                                 |
| pickle_dict                | 45.5 us                                              | 47.7 us: 1.05x slower                                 |
| json_loads                 | 35.9 us                                              | 37.6 us: 1.05x slower                                 |
| sympy_expand               | 591 ms                                               | 622 ms: 1.05x slower                                  |
| sympy_sum                  | 218 ms                                               | 230 ms: 1.05x slower                                  |
| mako                       | 16.1 ms                                              | 17.0 ms: 1.06x slower                                 |
| json                       | 7.14 ms                                              | 7.54 ms: 1.06x slower                                 |
| scimark_fft                | 481 ms                                               | 510 ms: 1.06x slower                                  |
| genshi_text                | 30.3 ms                                              | 32.4 ms: 1.07x slower                                 |
| thrift                     | 1.10 ms                                              | 1.19 ms: 1.08x slower                                 |
| regex_dna                  | 268 ms                                               | 292 ms: 1.09x slower                                  |
| json_dumps                 | 14.0 ms                                              | 15.7 ms: 1.12x slower                                 |
| unpickle_list              | 6.83 us                                              | 7.68 us: 1.12x slower                                 |
| go                         | 173 ms                                               | 196 ms: 1.13x slower                                  |
| spectral_norm              | 136 ms                                               | 155 ms: 1.14x slower                                  |
| telco                      | 9.53 ms                                              | 11.2 ms: 1.18x slower                                 |
| regex_v8                   | 29.9 ms                                              | 35.4 ms: 1.18x slower                                 |
| coverage                   | 96.9 ms                                              | 117 ms: 1.20x slower                                  |
| create_gc_cycles           | 2.00 ms                                              | 2.51 ms: 1.26x slower                                 |
| Geometric mean             | (ref)                                                | 1.04x faster                                          |

Benchmark hidden because not significant (43): bench_mp_pool, html5lib, unpack_sequence, xml_etree_iterparse, sqlglot_transpile, crypto_pyaes, pickle_list, logging_silent, asyncio_tcp, float, sqlglot_parse, sympy_str, asyncio_websockets, scimark_lu, mdp, pprint_safe_repr, pidigits, pprint_pformat, scimark_sor, pickle, deltablue, pickle_pure_python, nbody, docutils, python_startup, logging_format, pycparser, pylint, asyncio_tcp_ssl, nqueens, sqlite_synth, richards, fannkuch, pyflate, coroutines, richards_super, meteor_contest, sqlglot_normalize, django_template, typing_runtime_protocols, genshi_xml, bench_thread_pool, regex_effbot
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.76% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x