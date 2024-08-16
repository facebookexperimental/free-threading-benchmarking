# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 410 ms: 1.11x faster                                  |
| docutils       | 4.05 sec                                             | 3.93 sec: 1.03x faster                                |
| html5lib       | 100 ms                                               | 88.8 ms: 1.13x faster                                 |
| Geometric mean | (ref)                                                | 1.08x faster                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none_tg         | 726 ms                                               | 464 ms: 1.56x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 584 ms: 1.56x faster                                  |
| async_tree_none            | 820 ms                                               | 531 ms: 1.54x faster                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.24 sec: 1.50x faster                                |
| async_tree_memoization     | 975 ms                                               | 671 ms: 1.45x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.28 sec: 1.45x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 821 ms: 1.39x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 818 ms: 1.37x faster                                  |
| async_generators           | 615 ms                                               | 570 ms: 1.08x faster                                  |
| Geometric mean             | (ref)                                                | 1.28x faster                                          |

Benchmark hidden because not significant (4): asyncio_tcp, coroutines, asyncio_websockets, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| float          | 124 ms                                               | 115 ms: 1.08x faster                                  |
| pidigits       | 256 ms                                               | 240 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                | 1.06x faster                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 268 ms                                               | 286 ms: 1.07x slower                                  |
| regex_v8       | 29.9 ms                                              | 32.9 ms: 1.10x slower                                 |
| Geometric mean | (ref)                                                | 1.03x slower                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|---------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_generate  | 138 ms                                               | 116 ms: 1.19x faster                                  |
| xml_etree_parse     | 244 ms                                               | 216 ms: 1.13x faster                                  |
| pickle_list         | 7.01 us                                              | 6.29 us: 1.11x faster                                 |
| unpickle            | 21.6 us                                              | 20.1 us: 1.08x faster                                 |
| xml_etree_iterparse | 173 ms                                               | 161 ms: 1.07x faster                                  |
| tomli_loads         | 2.86 sec                                             | 2.68 sec: 1.07x faster                                |
| json_dumps          | 14.0 ms                                              | 14.8 ms: 1.06x slower                                 |
| json_loads          | 35.9 us                                              | 37.9 us: 1.06x slower                                 |
| Geometric mean      | (ref)                                                | 1.04x faster                                          |

Benchmark hidden because not significant (6): pickle_pure_python, unpickle_pure_python, unpickle_list, pickle_dict, pickle, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 14.8 ms: 1.10x faster                                 |
| python_startup         | 22.7 ms                                              | 21.4 ms: 1.06x faster                                 |
| Geometric mean         | (ref)                                                | 1.08x faster                                          |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): django_template, genshi_xml, mako, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none_tg         | 726 ms                                               | 464 ms: 1.56x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 584 ms: 1.56x faster                                  |
| async_tree_none            | 820 ms                                               | 531 ms: 1.54x faster                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.24 sec: 1.50x faster                                |
| async_tree_memoization     | 975 ms                                               | 671 ms: 1.45x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.28 sec: 1.45x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 821 ms: 1.39x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 818 ms: 1.37x faster                                  |
| comprehensions             | 28.6 us                                              | 21.3 us: 1.35x faster                                 |
| deepcopy                   | 486 us                                               | 361 us: 1.35x faster                                  |
| deepcopy_memo              | 51.0 us                                              | 38.7 us: 1.32x faster                                 |
| raytrace                   | 405 ms                                               | 339 ms: 1.19x faster                                  |
| xml_etree_generate         | 138 ms                                               | 116 ms: 1.19x faster                                  |
| generators                 | 44.7 ms                                              | 38.3 ms: 1.17x faster                                 |
| logging_simple             | 9.68 us                                              | 8.31 us: 1.16x faster                                 |
| gc_traversal               | 6.42 ms                                              | 5.66 ms: 1.13x faster                                 |
| chaos                      | 92.1 ms                                              | 81.6 ms: 1.13x faster                                 |
| xml_etree_parse            | 244 ms                                               | 216 ms: 1.13x faster                                  |
| html5lib                   | 100 ms                                               | 88.8 ms: 1.13x faster                                 |
| deepcopy_reduce            | 4.18 us                                              | 3.71 us: 1.13x faster                                 |
| pickle_list                | 7.01 us                                              | 6.29 us: 1.11x faster                                 |
| 2to3                       | 456 ms                                               | 410 ms: 1.11x faster                                  |
| pathlib                    | 31.6 ms                                              | 28.6 ms: 1.11x faster                                 |
| logging_silent             | 139 ns                                               | 126 ns: 1.10x faster                                  |
| sqlglot_optimize           | 80.2 ms                                              | 73.2 ms: 1.10x faster                                 |
| python_startup_no_site     | 16.2 ms                                              | 14.8 ms: 1.10x faster                                 |
| bpe_tokeniser              | 6.76 sec                                             | 6.17 sec: 1.09x faster                                |
| scimark_monte_carlo        | 96.8 ms                                              | 88.4 ms: 1.09x faster                                 |
| sqlglot_transpile          | 2.32 ms                                              | 2.13 ms: 1.09x faster                                 |
| dulwich_log                | 104 ms                                               | 95.9 ms: 1.08x faster                                 |
| float                      | 124 ms                                               | 115 ms: 1.08x faster                                  |
| crypto_pyaes               | 110 ms                                               | 102 ms: 1.08x faster                                  |
| async_generators           | 615 ms                                               | 570 ms: 1.08x faster                                  |
| unpickle                   | 21.6 us                                              | 20.1 us: 1.08x faster                                 |
| nqueens                    | 116 ms                                               | 107 ms: 1.08x faster                                  |
| sqlglot_parse              | 1.85 ms                                              | 1.72 ms: 1.08x faster                                 |
| thrift                     | 1.10 ms                                              | 1.03 ms: 1.07x faster                                 |
| xml_etree_iterparse        | 173 ms                                               | 161 ms: 1.07x faster                                  |
| tomli_loads                | 2.86 sec                                             | 2.68 sec: 1.07x faster                                |
| pidigits                   | 256 ms                                               | 240 ms: 1.07x faster                                  |
| typing_runtime_protocols   | 224 us                                               | 210 us: 1.07x faster                                  |
| pycparser                  | 1.68 sec                                             | 1.57 sec: 1.07x faster                                |
| python_startup             | 22.7 ms                                              | 21.4 ms: 1.06x faster                                 |
| dask                       | 916 ms                                               | 868 ms: 1.05x faster                                  |
| sympy_str                  | 379 ms                                               | 360 ms: 1.05x faster                                  |
| mdp                        | 3.77 sec                                             | 3.61 sec: 1.04x faster                                |
| pprint_pformat             | 1.99 sec                                             | 1.92 sec: 1.03x faster                                |
| docutils                   | 4.05 sec                                             | 3.93 sec: 1.03x faster                                |
| sqlglot_normalize          | 144 ms                                               | 150 ms: 1.04x slower                                  |
| json_dumps                 | 14.0 ms                                              | 14.8 ms: 1.06x slower                                 |
| json_loads                 | 35.9 us                                              | 37.9 us: 1.06x slower                                 |
| regex_dna                  | 268 ms                                               | 286 ms: 1.07x slower                                  |
| json                       | 7.14 ms                                              | 7.74 ms: 1.08x slower                                 |
| regex_v8                   | 29.9 ms                                              | 32.9 ms: 1.10x slower                                 |
| go                         | 173 ms                                               | 191 ms: 1.10x slower                                  |
| unpack_sequence            | 70.8 ns                                              | 78.4 ns: 1.11x slower                                 |
| create_gc_cycles           | 2.00 ms                                              | 2.27 ms: 1.14x slower                                 |
| telco                      | 9.53 ms                                              | 11.1 ms: 1.17x slower                                 |
| spectral_norm              | 136 ms                                               | 164 ms: 1.20x slower                                  |
| coverage                   | 96.9 ms                                              | 126 ms: 1.30x slower                                  |
| Geometric mean             | (ref)                                                | 1.07x faster                                          |

Benchmark hidden because not significant (38): tornado_http, bench_mp_pool, scimark_sparse_mat_mult, pickle_pure_python, richards, asyncio_tcp, regex_effbot, unpickle_pure_python, deltablue, regex_compile, nbody, logging_format, sympy_sum, pprint_safe_repr, coroutines, sqlite_synth, richards_super, pylint, unpickle_list, scimark_fft, scimark_lu, pickle_dict, bench_thread_pool, pickle, django_template, meteor_contest, asyncio_websockets, asyncio_tcp_ssl, pyflate, genshi_xml, sympy_integrate, xml_etree_process, scimark_sor, hexiom, sympy_expand, mako, fannkuch, genshi_text
Ignored benchmarks (7) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x