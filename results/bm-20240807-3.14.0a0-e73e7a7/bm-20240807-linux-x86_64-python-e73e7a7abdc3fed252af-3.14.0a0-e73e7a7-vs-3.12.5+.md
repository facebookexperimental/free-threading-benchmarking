# Results vs. 3.12.5+

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.03x faster
- HPT reliability: 94.11%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 501 ms: 1.64x faster                                                  |
| async_tree_none_tg         | 726 ms                                               | 485 ms: 1.50x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.29 sec: 1.44x faster                                                |
| async_tree_io_tg           | 1.87 sec                                             | 1.30 sec: 1.44x faster                                                |
| async_tree_memoization_tg  | 912 ms                                               | 650 ms: 1.40x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 705 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 829 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 856 ms: 1.33x faster                                                  |
| async_generators           | 615 ms                                               | 579 ms: 1.06x faster                                                  |
| asyncio_tcp                | 988 ms                                               | 940 ms: 1.05x faster                                                  |
| coroutines                 | 30.6 ms                                              | 32.6 ms: 1.07x slower                                                 |
| Geometric mean             | (ref)                                                | 1.25x faster                                                          |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 256 ms                                               | 245 ms: 1.05x faster                                                  |
| float          | 124 ms                                               | 119 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                | 1.02x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 5.47 ms: 1.09x slower                                                 |
| regex_dna      | 268 ms                                               | 300 ms: 1.12x slower                                                  |
| regex_v8       | 29.9 ms                                              | 38.1 ms: 1.27x slower                                                 |
| Geometric mean | (ref)                                                | 1.12x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|--------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_generate | 138 ms                                               | 123 ms: 1.11x faster                                                  |
| xml_etree_parse    | 244 ms                                               | 226 ms: 1.08x faster                                                  |
| tomli_loads        | 2.86 sec                                             | 2.66 sec: 1.07x faster                                                |
| json_loads         | 35.9 us                                              | 37.5 us: 1.05x slower                                                 |
| xml_etree_process  | 82.7 ms                                              | 86.9 ms: 1.05x slower                                                 |
| Geometric mean     | (ref)                                                | 1.02x faster                                                          |

Benchmark hidden because not significant (9): pickle_list, xml_etree_iterparse, unpickle_pure_python, pickle, unpickle_list, pickle_pure_python, unpickle, pickle_dict, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 14.9 ms: 1.09x faster                                                 |
| python_startup         | 22.7 ms                                              | 23.8 ms: 1.05x slower                                                 |
| Geometric mean         | (ref)                                                | 1.02x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 45.4 ms                                              | 48.3 ms: 1.06x slower                                                 |
| mako            | 16.1 ms                                              | 18.3 ms: 1.13x slower                                                 |
| Geometric mean  | (ref)                                                | 1.07x slower                                                          |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 501 ms: 1.64x faster                                                  |
| async_tree_none_tg         | 726 ms                                               | 485 ms: 1.50x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.29 sec: 1.44x faster                                                |
| async_tree_io_tg           | 1.87 sec                                             | 1.30 sec: 1.44x faster                                                |
| async_tree_memoization_tg  | 912 ms                                               | 650 ms: 1.40x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 705 ms: 1.38x faster                                                  |
| deepcopy                   | 486 us                                               | 359 us: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 829 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 856 ms: 1.33x faster                                                  |
| deepcopy_memo              | 51.0 us                                              | 40.2 us: 1.27x faster                                                 |
| comprehensions             | 28.6 us                                              | 24.0 us: 1.20x faster                                                 |
| raytrace                   | 405 ms                                               | 340 ms: 1.19x faster                                                  |
| unpack_sequence            | 70.8 ns                                              | 61.3 ns: 1.15x faster                                                 |
| deepcopy_reduce            | 4.18 us                                              | 3.63 us: 1.15x faster                                                 |
| gc_traversal               | 6.42 ms                                              | 5.59 ms: 1.15x faster                                                 |
| logging_simple             | 9.68 us                                              | 8.46 us: 1.14x faster                                                 |
| xml_etree_generate         | 138 ms                                               | 123 ms: 1.11x faster                                                  |
| bpe_tokeniser              | 6.76 sec                                             | 6.08 sec: 1.11x faster                                                |
| nqueens                    | 116 ms                                               | 105 ms: 1.10x faster                                                  |
| python_startup_no_site     | 16.2 ms                                              | 14.9 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 89.4 ms: 1.08x faster                                                 |
| generators                 | 44.7 ms                                              | 41.5 ms: 1.08x faster                                                 |
| xml_etree_parse            | 244 ms                                               | 226 ms: 1.08x faster                                                  |
| tomli_loads                | 2.86 sec                                             | 2.66 sec: 1.07x faster                                                |
| pathlib                    | 31.6 ms                                              | 29.7 ms: 1.06x faster                                                 |
| async_generators           | 615 ms                                               | 579 ms: 1.06x faster                                                  |
| json                       | 7.14 ms                                              | 6.76 ms: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 6.59 ms: 1.05x faster                                                 |
| asyncio_tcp                | 988 ms                                               | 940 ms: 1.05x faster                                                  |
| meteor_contest             | 146 ms                                               | 139 ms: 1.05x faster                                                  |
| crypto_pyaes               | 110 ms                                               | 105 ms: 1.05x faster                                                  |
| pidigits                   | 256 ms                                               | 245 ms: 1.05x faster                                                  |
| float                      | 124 ms                                               | 119 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.99 sec                                             | 1.94 sec: 1.02x faster                                                |
| json_loads                 | 35.9 us                                              | 37.5 us: 1.05x slower                                                 |
| xml_etree_process          | 82.7 ms                                              | 86.9 ms: 1.05x slower                                                 |
| python_startup             | 22.7 ms                                              | 23.8 ms: 1.05x slower                                                 |
| django_template            | 45.4 ms                                              | 48.3 ms: 1.06x slower                                                 |
| coroutines                 | 30.6 ms                                              | 32.6 ms: 1.07x slower                                                 |
| logging_format             | 9.56 us                                              | 10.2 us: 1.07x slower                                                 |
| sqlite_synth               | 3.77 us                                              | 4.10 us: 1.09x slower                                                 |
| regex_effbot               | 5.02 ms                                              | 5.47 ms: 1.09x slower                                                 |
| richards_super             | 69.7 ms                                              | 76.3 ms: 1.09x slower                                                 |
| richards                   | 62.8 ms                                              | 69.2 ms: 1.10x slower                                                 |
| regex_dna                  | 268 ms                                               | 300 ms: 1.12x slower                                                  |
| mako                       | 16.1 ms                                              | 18.3 ms: 1.13x slower                                                 |
| go                         | 173 ms                                               | 198 ms: 1.14x slower                                                  |
| spectral_norm              | 136 ms                                               | 157 ms: 1.15x slower                                                  |
| create_gc_cycles           | 2.00 ms                                              | 2.41 ms: 1.21x slower                                                 |
| telco                      | 9.53 ms                                              | 11.5 ms: 1.21x slower                                                 |
| coverage                   | 96.9 ms                                              | 117 ms: 1.21x slower                                                  |
| regex_v8                   | 29.9 ms                                              | 38.1 ms: 1.27x slower                                                 |
| Geometric mean             | (ref)                                                | 1.03x faster                                                          |

Benchmark hidden because not significant (44): html5lib, chaos, pickle_list, xml_etree_iterparse, sympy_integrate, unpickle_pure_python, pickle, typing_runtime_protocols, 2to3, sympy_str, mdp, asyncio_tcp_ssl, scimark_fft, pylint, tornado_http, logging_silent, deltablue, pycparser, unpickle_list, pickle_pure_python, scimark_sor, bench_thread_pool, bench_mp_pool, unpickle, pickle_dict, scimark_lu, fannkuch, sqlglot_normalize, asyncio_websockets, sqlglot_parse, docutils, pprint_safe_repr, sqlglot_transpile, sympy_expand, pyflate, regex_compile, json_dumps, nbody, sympy_sum, thrift, hexiom, genshi_xml, sqlglot_optimize, genshi_text
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 94.11% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x