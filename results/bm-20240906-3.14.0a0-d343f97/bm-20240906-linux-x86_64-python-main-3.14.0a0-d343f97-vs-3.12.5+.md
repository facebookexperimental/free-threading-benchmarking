# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d343f97
- commit date: 2024-09-06
- overall geometric mean: 1.02x faster
- HPT reliability: 63.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| html5lib       | 100 ms                                               | 89.1 ms: 1.12x faster                                 |
| Geometric mean | (ref)                                                | 1.02x faster                                          |

Benchmark hidden because not significant (3): 2to3, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 502 ms: 1.63x faster                                  |
| async_tree_memoization     | 975 ms                                               | 686 ms: 1.42x faster                                  |
| async_tree_none_tg         | 726 ms                                               | 519 ms: 1.40x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 667 ms: 1.37x faster                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.39 sec: 1.34x faster                                |
| async_tree_io              | 1.86 sec                                             | 1.39 sec: 1.34x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 888 ms: 1.29x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 887 ms: 1.26x faster                                  |
| async_generators           | 615 ms                                               | 586 ms: 1.05x faster                                  |
| asyncio_websockets         | 752 ms                                               | 786 ms: 1.04x slower                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 2.99 sec: 1.06x slower                                |
| Geometric mean             | (ref)                                                | 1.21x faster                                          |

Benchmark hidden because not significant (2): asyncio_tcp, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                               | 247 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                | 1.01x faster                                          |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 29.9 ms                                              | 32.1 ms: 1.07x slower                                 |
| regex_dna      | 268 ms                                               | 297 ms: 1.11x slower                                  |
| Geometric mean | (ref)                                                | 1.05x slower                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|--------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_generate | 138 ms                                               | 125 ms: 1.10x faster                                  |
| unpickle           | 21.6 us                                              | 19.9 us: 1.09x faster                                 |
| unpickle_list      | 6.83 us                                              | 7.33 us: 1.07x slower                                 |
| pickle_dict        | 45.5 us                                              | 49.2 us: 1.08x slower                                 |
| pickle_list        | 7.01 us                                              | 7.57 us: 1.08x slower                                 |
| json_loads         | 35.9 us                                              | 41.2 us: 1.15x slower                                 |
| Geometric mean     | (ref)                                                | 1.02x slower                                          |

Benchmark hidden because not significant (8): xml_etree_parse, unpickle_pure_python, xml_etree_iterparse, tomli_loads, xml_etree_process, json_dumps, pickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 17.8 ms: 1.10x slower                                 |
| python_startup         | 22.7 ms                                              | 25.6 ms: 1.13x slower                                 |
| Geometric mean         | (ref)                                                | 1.11x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|-----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 45.4 ms                                              | 48.4 ms: 1.07x slower                                 |
| genshi_xml      | 69.1 ms                                              | 76.1 ms: 1.10x slower                                 |
| genshi_text     | 30.3 ms                                              | 34.1 ms: 1.12x slower                                 |
| mako            | 16.1 ms                                              | 19.0 ms: 1.18x slower                                 |
| Geometric mean  | (ref)                                                | 1.12x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 502 ms: 1.63x faster                                  |
| deepcopy                   | 486 us                                               | 341 us: 1.43x faster                                  |
| async_tree_memoization     | 975 ms                                               | 686 ms: 1.42x faster                                  |
| async_tree_none_tg         | 726 ms                                               | 519 ms: 1.40x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 667 ms: 1.37x faster                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.39 sec: 1.34x faster                                |
| async_tree_io              | 1.86 sec                                             | 1.39 sec: 1.34x faster                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 888 ms: 1.29x faster                                  |
| deepcopy_memo              | 51.0 us                                              | 39.8 us: 1.28x faster                                 |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 887 ms: 1.26x faster                                  |
| comprehensions             | 28.6 us                                              | 23.0 us: 1.25x faster                                 |
| crypto_pyaes               | 110 ms                                               | 93.8 ms: 1.17x faster                                 |
| deepcopy_reduce            | 4.18 us                                              | 3.61 us: 1.16x faster                                 |
| unpack_sequence            | 70.8 ns                                              | 62.2 ns: 1.14x faster                                 |
| html5lib                   | 100 ms                                               | 89.1 ms: 1.12x faster                                 |
| raytrace                   | 405 ms                                               | 361 ms: 1.12x faster                                  |
| chaos                      | 92.1 ms                                              | 82.8 ms: 1.11x faster                                 |
| logging_simple             | 9.68 us                                              | 8.80 us: 1.10x faster                                 |
| xml_etree_generate         | 138 ms                                               | 125 ms: 1.10x faster                                  |
| unpickle                   | 21.6 us                                              | 19.9 us: 1.09x faster                                 |
| generators                 | 44.7 ms                                              | 41.7 ms: 1.07x faster                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 91.7 ms: 1.05x faster                                 |
| sqlglot_transpile          | 2.32 ms                                              | 2.21 ms: 1.05x faster                                 |
| async_generators           | 615 ms                                               | 586 ms: 1.05x faster                                  |
| bpe_tokeniser              | 6.76 sec                                             | 6.49 sec: 1.04x faster                                |
| pidigits                   | 256 ms                                               | 247 ms: 1.04x faster                                  |
| scimark_fft                | 481 ms                                               | 499 ms: 1.04x slower                                  |
| pyflate                    | 664 ms                                               | 690 ms: 1.04x slower                                  |
| asyncio_websockets         | 752 ms                                               | 786 ms: 1.04x slower                                  |
| hexiom                     | 8.19 ms                                              | 8.58 ms: 1.05x slower                                 |
| logging_silent             | 139 ns                                               | 146 ns: 1.05x slower                                  |
| fannkuch                   | 525 ms                                               | 553 ms: 1.05x slower                                  |
| sympy_expand               | 591 ms                                               | 623 ms: 1.05x slower                                  |
| richards_super             | 69.7 ms                                              | 73.7 ms: 1.06x slower                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 2.99 sec: 1.06x slower                                |
| sqlite_synth               | 3.77 us                                              | 4.02 us: 1.07x slower                                 |
| django_template            | 45.4 ms                                              | 48.4 ms: 1.07x slower                                 |
| unpickle_list              | 6.83 us                                              | 7.33 us: 1.07x slower                                 |
| regex_v8                   | 29.9 ms                                              | 32.1 ms: 1.07x slower                                 |
| bench_mp_pool              | 21.2 ms                                              | 22.8 ms: 1.08x slower                                 |
| pickle_dict                | 45.5 us                                              | 49.2 us: 1.08x slower                                 |
| pickle_list                | 7.01 us                                              | 7.57 us: 1.08x slower                                 |
| mdp                        | 3.77 sec                                             | 4.09 sec: 1.09x slower                                |
| sqlglot_parse              | 1.85 ms                                              | 2.03 ms: 1.10x slower                                 |
| python_startup_no_site     | 16.2 ms                                              | 17.8 ms: 1.10x slower                                 |
| genshi_xml                 | 69.1 ms                                              | 76.1 ms: 1.10x slower                                 |
| regex_dna                  | 268 ms                                               | 297 ms: 1.11x slower                                  |
| logging_format             | 9.56 us                                              | 10.7 us: 1.12x slower                                 |
| genshi_text                | 30.3 ms                                              | 34.1 ms: 1.12x slower                                 |
| python_startup             | 22.7 ms                                              | 25.6 ms: 1.13x slower                                 |
| bench_thread_pool          | 3.42 ms                                              | 3.86 ms: 1.13x slower                                 |
| json_loads                 | 35.9 us                                              | 41.2 us: 1.15x slower                                 |
| spectral_norm              | 136 ms                                               | 160 ms: 1.17x slower                                  |
| mako                       | 16.1 ms                                              | 19.0 ms: 1.18x slower                                 |
| coverage                   | 96.9 ms                                              | 117 ms: 1.21x slower                                  |
| telco                      | 9.53 ms                                              | 11.9 ms: 1.24x slower                                 |
| create_gc_cycles           | 2.00 ms                                              | 2.70 ms: 1.35x slower                                 |
| Geometric mean             | (ref)                                                | 1.02x faster                                          |

Benchmark hidden because not significant (40): sqlglot_optimize, pathlib, xml_etree_parse, float, unpickle_pure_python, dulwich_log, 2to3, xml_etree_iterparse, go, sympy_str, thrift, typing_runtime_protocols, regex_effbot, gc_traversal, tomli_loads, pycparser, scimark_sparse_mat_mult, pprint_pformat, nqueens, xml_etree_process, asyncio_tcp, coroutines, richards, scimark_lu, docutils, json, sympy_sum, scimark_sor, deltablue, sqlglot_normalize, sympy_integrate, json_dumps, tornado_http, regex_compile, pprint_safe_repr, meteor_contest, nbody, pickle, pickle_pure_python, pylint
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 63.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x