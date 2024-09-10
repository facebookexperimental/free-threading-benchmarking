# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 033510e
- commit date: 2024-09-06
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 415 ms: 1.10x faster                                  |
| docutils       | 4.05 sec                                             | 3.82 sec: 1.06x faster                                |
| html5lib       | 100 ms                                               | 88.4 ms: 1.13x faster                                 |
| Geometric mean | (ref)                                                | 1.09x faster                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 501 ms: 1.63x faster                                  |
| async_tree_memoization     | 975 ms                                               | 637 ms: 1.53x faster                                  |
| async_tree_none_tg         | 726 ms                                               | 483 ms: 1.50x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 621 ms: 1.47x faster                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.32 sec: 1.42x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 823 ms: 1.39x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.36 sec: 1.36x faster                                |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 853 ms: 1.31x faster                                  |
| asyncio_tcp                | 988 ms                                               | 901 ms: 1.10x faster                                  |
| async_generators           | 615 ms                                               | 575 ms: 1.07x faster                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 2.73 sec: 1.03x faster                                |
| Geometric mean             | (ref)                                                | 1.27x faster                                          |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| float          | 124 ms                                               | 115 ms: 1.08x faster                                  |
| Geometric mean | (ref)                                                | 1.03x faster                                          |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 186 ms                                               | 175 ms: 1.06x faster                                  |
| regex_dna      | 268 ms                                               | 288 ms: 1.07x slower                                  |
| regex_v8       | 29.9 ms                                              | 34.9 ms: 1.17x slower                                 |
| Geometric mean | (ref)                                                | 1.05x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_generate   | 138 ms                                               | 118 ms: 1.16x faster                                  |
| unpickle_pure_python | 304 us                                               | 288 us: 1.06x faster                                  |
| tomli_loads          | 2.86 sec                                             | 2.75 sec: 1.04x faster                                |
| unpickle_list        | 6.83 us                                              | 7.20 us: 1.05x slower                                 |
| json_loads           | 35.9 us                                              | 37.9 us: 1.06x slower                                 |
| json_dumps           | 14.0 ms                                              | 15.8 ms: 1.13x slower                                 |
| Geometric mean       | (ref)                                                | 1.01x faster                                          |

Benchmark hidden because not significant (8): xml_etree_parse, unpickle, xml_etree_iterparse, pickle_dict, pickle_list, pickle_pure_python, pickle, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 15.1 ms: 1.08x faster                                 |
| python_startup         | 22.7 ms                                              | 21.6 ms: 1.05x faster                                 |
| Geometric mean         | (ref)                                                | 1.06x faster                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text    | 30.3 ms                                              | 33.6 ms: 1.11x slower                                 |
| mako           | 16.1 ms                                              | 18.2 ms: 1.13x slower                                 |
| Geometric mean | (ref)                                                | 1.06x slower                                          |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 501 ms: 1.63x faster                                  |
| async_tree_memoization     | 975 ms                                               | 637 ms: 1.53x faster                                  |
| async_tree_none_tg         | 726 ms                                               | 483 ms: 1.50x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 621 ms: 1.47x faster                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.32 sec: 1.42x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 823 ms: 1.39x faster                                  |
| deepcopy                   | 486 us                                               | 354 us: 1.37x faster                                  |
| unpack_sequence            | 70.8 ns                                              | 51.6 ns: 1.37x faster                                 |
| async_tree_io              | 1.86 sec                                             | 1.36 sec: 1.36x faster                                |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 853 ms: 1.31x faster                                  |
| comprehensions             | 28.6 us                                              | 22.0 us: 1.30x faster                                 |
| raytrace                   | 405 ms                                               | 340 ms: 1.19x faster                                  |
| deepcopy_memo              | 51.0 us                                              | 43.0 us: 1.19x faster                                 |
| xml_etree_generate         | 138 ms                                               | 118 ms: 1.16x faster                                  |
| deepcopy_reduce            | 4.18 us                                              | 3.62 us: 1.16x faster                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 6.07 ms: 1.14x faster                                 |
| gc_traversal               | 6.42 ms                                              | 5.62 ms: 1.14x faster                                 |
| html5lib                   | 100 ms                                               | 88.4 ms: 1.13x faster                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 85.8 ms: 1.13x faster                                 |
| crypto_pyaes               | 110 ms                                               | 98.5 ms: 1.11x faster                                 |
| sqlglot_optimize           | 80.2 ms                                              | 72.3 ms: 1.11x faster                                 |
| chaos                      | 92.1 ms                                              | 83.1 ms: 1.11x faster                                 |
| bpe_tokeniser              | 6.76 sec                                             | 6.12 sec: 1.10x faster                                |
| 2to3                       | 456 ms                                               | 415 ms: 1.10x faster                                  |
| asyncio_tcp                | 988 ms                                               | 901 ms: 1.10x faster                                  |
| sqlglot_parse              | 1.85 ms                                              | 1.69 ms: 1.09x faster                                 |
| sqlglot_transpile          | 2.32 ms                                              | 2.13 ms: 1.09x faster                                 |
| pycparser                  | 1.68 sec                                             | 1.54 sec: 1.09x faster                                |
| float                      | 124 ms                                               | 115 ms: 1.08x faster                                  |
| go                         | 173 ms                                               | 161 ms: 1.08x faster                                  |
| python_startup_no_site     | 16.2 ms                                              | 15.1 ms: 1.08x faster                                 |
| sympy_integrate            | 29.0 ms                                              | 27.0 ms: 1.07x faster                                 |
| async_generators           | 615 ms                                               | 575 ms: 1.07x faster                                  |
| pathlib                    | 31.6 ms                                              | 29.7 ms: 1.06x faster                                 |
| regex_compile              | 186 ms                                               | 175 ms: 1.06x faster                                  |
| pprint_safe_repr           | 972 ms                                               | 916 ms: 1.06x faster                                  |
| docutils                   | 4.05 sec                                             | 3.82 sec: 1.06x faster                                |
| sympy_str                  | 379 ms                                               | 358 ms: 1.06x faster                                  |
| unpickle_pure_python       | 304 us                                               | 288 us: 1.06x faster                                  |
| thrift                     | 1.10 ms                                              | 1.05 ms: 1.05x faster                                 |
| logging_silent             | 139 ns                                               | 132 ns: 1.05x faster                                  |
| sympy_sum                  | 218 ms                                               | 207 ms: 1.05x faster                                  |
| python_startup             | 22.7 ms                                              | 21.6 ms: 1.05x faster                                 |
| pprint_pformat             | 1.99 sec                                             | 1.89 sec: 1.05x faster                                |
| tomli_loads                | 2.86 sec                                             | 2.75 sec: 1.04x faster                                |
| asyncio_tcp_ssl            | 2.82 sec                                             | 2.73 sec: 1.03x faster                                |
| unpickle_list              | 6.83 us                                              | 7.20 us: 1.05x slower                                 |
| json_loads                 | 35.9 us                                              | 37.9 us: 1.06x slower                                 |
| mdp                        | 3.77 sec                                             | 3.99 sec: 1.06x slower                                |
| spectral_norm              | 136 ms                                               | 146 ms: 1.07x slower                                  |
| regex_dna                  | 268 ms                                               | 288 ms: 1.07x slower                                  |
| genshi_text                | 30.3 ms                                              | 33.6 ms: 1.11x slower                                 |
| coverage                   | 96.9 ms                                              | 107 ms: 1.11x slower                                  |
| mako                       | 16.1 ms                                              | 18.2 ms: 1.13x slower                                 |
| json_dumps                 | 14.0 ms                                              | 15.8 ms: 1.13x slower                                 |
| regex_v8                   | 29.9 ms                                              | 34.9 ms: 1.17x slower                                 |
| create_gc_cycles           | 2.00 ms                                              | 2.35 ms: 1.18x slower                                 |
| dulwich_log                | 104 ms                                               | 123 ms: 1.18x slower                                  |
| telco                      | 9.53 ms                                              | 11.3 ms: 1.19x slower                                 |
| Geometric mean             | (ref)                                                | 1.06x faster                                          |

Benchmark hidden because not significant (38): bench_thread_pool, tornado_http, xml_etree_parse, bench_mp_pool, unpickle, xml_etree_iterparse, json, logging_simple, scimark_fft, generators, sqlglot_normalize, pickle_dict, nqueens, hexiom, scimark_sor, pickle_list, nbody, scimark_lu, typing_runtime_protocols, pidigits, pylint, pickle_pure_python, asyncio_websockets, django_template, genshi_xml, meteor_contest, pyflate, sympy_expand, sqlite_synth, fannkuch, richards_super, deltablue, logging_format, regex_effbot, richards, pickle, xml_etree_process, coroutines
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.02x