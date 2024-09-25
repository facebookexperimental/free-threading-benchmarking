# Results vs. 3.12.5+

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.01x faster
- HPT reliability: 65.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.05 sec                                             | 4.22 sec: 1.04x slower                                                |
| Geometric mean | (ref)                                                | 1.01x faster                                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 523 ms: 1.57x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 647 ms: 1.51x faster                                                  |
| async_tree_none_tg         | 726 ms                                               | 494 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 912 ms                                               | 643 ms: 1.42x faster                                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.33 sec: 1.41x faster                                                |
| async_tree_io              | 1.86 sec                                             | 1.42 sec: 1.31x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 875 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 893 ms: 1.28x faster                                                  |
| async_generators           | 615 ms                                               | 591 ms: 1.04x faster                                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 2.90 sec: 1.03x slower                                                |
| asyncio_websockets         | 752 ms                                               | 781 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                | 1.23x faster                                                          |

Benchmark hidden because not significant (2): coroutines, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 117 ms                                               | 129 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                | 1.03x slower                                                          |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 268 ms                                               | 310 ms: 1.16x slower                                                  |
| regex_v8       | 29.9 ms                                              | 36.2 ms: 1.21x slower                                                 |
| Geometric mean | (ref)                                                | 1.10x slower                                                          |

Benchmark hidden because not significant (2): regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|--------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_generate | 138 ms                                               | 128 ms: 1.07x faster                                                  |
| tomli_loads        | 2.86 sec                                             | 2.72 sec: 1.05x faster                                                |
| xml_etree_process  | 82.7 ms                                              | 86.8 ms: 1.05x slower                                                 |
| unpickle_list      | 6.83 us                                              | 7.18 us: 1.05x slower                                                 |
| json_loads         | 35.9 us                                              | 37.8 us: 1.05x slower                                                 |
| json_dumps         | 14.0 ms                                              | 15.4 ms: 1.10x slower                                                 |
| Geometric mean     | (ref)                                                | 1.01x slower                                                          |

Benchmark hidden because not significant (8): unpickle, pickle_pure_python, pickle, unpickle_pure_python, pickle_dict, pickle_list, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 17.7 ms: 1.09x slower                                                 |
| python_startup         | 22.7 ms                                              | 26.1 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                | 1.12x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 16.1 ms                                              | 18.5 ms: 1.15x slower                                                 |
| Geometric mean | (ref)                                                | 1.06x slower                                                          |

Benchmark hidden because not significant (3): django_template, genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 523 ms: 1.57x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 647 ms: 1.51x faster                                                  |
| async_tree_none_tg         | 726 ms                                               | 494 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 912 ms                                               | 643 ms: 1.42x faster                                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.33 sec: 1.41x faster                                                |
| deepcopy                   | 486 us                                               | 362 us: 1.34x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.42 sec: 1.31x faster                                                |
| comprehensions             | 28.6 us                                              | 22.1 us: 1.30x faster                                                 |
| deepcopy_memo              | 51.0 us                                              | 39.5 us: 1.29x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 875 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 893 ms: 1.28x faster                                                  |
| crypto_pyaes               | 110 ms                                               | 95.7 ms: 1.14x faster                                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 6.13 ms: 1.13x faster                                                 |
| raytrace                   | 405 ms                                               | 358 ms: 1.13x faster                                                  |
| logging_simple             | 9.68 us                                              | 8.60 us: 1.13x faster                                                 |
| chaos                      | 92.1 ms                                              | 83.6 ms: 1.10x faster                                                 |
| generators                 | 44.7 ms                                              | 41.1 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 89.4 ms: 1.08x faster                                                 |
| xml_etree_generate         | 138 ms                                               | 128 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 6.76 sec                                             | 6.41 sec: 1.05x faster                                                |
| tomli_loads                | 2.86 sec                                             | 2.72 sec: 1.05x faster                                                |
| scimark_lu                 | 155 ms                                               | 149 ms: 1.04x faster                                                  |
| async_generators           | 615 ms                                               | 591 ms: 1.04x faster                                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 2.90 sec: 1.03x slower                                                |
| asyncio_websockets         | 752 ms                                               | 781 ms: 1.04x slower                                                  |
| docutils                   | 4.05 sec                                             | 4.22 sec: 1.04x slower                                                |
| mdp                        | 3.77 sec                                             | 3.93 sec: 1.04x slower                                                |
| xml_etree_process          | 82.7 ms                                              | 86.8 ms: 1.05x slower                                                 |
| unpickle_list              | 6.83 us                                              | 7.18 us: 1.05x slower                                                 |
| richards                   | 62.8 ms                                              | 66.0 ms: 1.05x slower                                                 |
| json_loads                 | 35.9 us                                              | 37.8 us: 1.05x slower                                                 |
| sqlglot_normalize          | 144 ms                                               | 152 ms: 1.06x slower                                                  |
| pycparser                  | 1.68 sec                                             | 1.79 sec: 1.07x slower                                                |
| sqlite_synth               | 3.77 us                                              | 4.03 us: 1.07x slower                                                 |
| sympy_expand               | 591 ms                                               | 635 ms: 1.07x slower                                                  |
| deltablue                  | 4.45 ms                                              | 4.79 ms: 1.08x slower                                                 |
| fannkuch                   | 525 ms                                               | 565 ms: 1.08x slower                                                  |
| python_startup_no_site     | 16.2 ms                                              | 17.7 ms: 1.09x slower                                                 |
| json_dumps                 | 14.0 ms                                              | 15.4 ms: 1.10x slower                                                 |
| nbody                      | 117 ms                                               | 129 ms: 1.11x slower                                                  |
| pyflate                    | 664 ms                                               | 735 ms: 1.11x slower                                                  |
| hexiom                     | 8.19 ms                                              | 9.21 ms: 1.12x slower                                                 |
| bench_thread_pool          | 3.42 ms                                              | 3.89 ms: 1.14x slower                                                 |
| mako                       | 16.1 ms                                              | 18.5 ms: 1.15x slower                                                 |
| python_startup             | 22.7 ms                                              | 26.1 ms: 1.15x slower                                                 |
| regex_dna                  | 268 ms                                               | 310 ms: 1.16x slower                                                  |
| spectral_norm              | 136 ms                                               | 161 ms: 1.18x slower                                                  |
| regex_v8                   | 29.9 ms                                              | 36.2 ms: 1.21x slower                                                 |
| telco                      | 9.53 ms                                              | 11.5 ms: 1.21x slower                                                 |
| coverage                   | 96.9 ms                                              | 121 ms: 1.25x slower                                                  |
| bench_mp_pool              | 21.2 ms                                              | 26.6 ms: 1.25x slower                                                 |
| create_gc_cycles           | 2.00 ms                                              | 2.70 ms: 1.35x slower                                                 |
| Geometric mean             | (ref)                                                | 1.01x faster                                                          |

Benchmark hidden because not significant (45): html5lib, unpickle, sqlglot_optimize, pickle_pure_python, gc_traversal, pathlib, sympy_sum, go, coroutines, scimark_fft, pickle, deepcopy_reduce, unpickle_pure_python, asyncio_tcp, sqlglot_transpile, nqueens, 2to3, pidigits, pprint_pformat, pickle_dict, json, tornado_http, float, sqlglot_parse, scimark_sor, logging_format, regex_compile, richards_super, unpack_sequence, django_template, genshi_text, logging_silent, pprint_safe_repr, typing_runtime_protocols, sympy_integrate, regex_effbot, pickle_list, dulwich_log, xml_etree_parse, meteor_contest, genshi_xml, xml_etree_iterparse, pylint, sympy_str, thrift
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 65.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x