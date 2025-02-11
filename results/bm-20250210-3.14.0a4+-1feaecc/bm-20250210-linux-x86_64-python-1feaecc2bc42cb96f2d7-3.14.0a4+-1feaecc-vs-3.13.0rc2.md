# Results vs. 3.13.0rc2

- fork: python
- ref: 1feaecc2bc42cb96f2d7
- machine: linux-x86_64
- commit hash: 1feaecc
- commit date: 2025-02-10
- overall geometric mean: 1.065x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.70 sec: 1.08x faster                                                 |
| html5lib       | 92.6 ms                                                      | 81.6 ms: 1.14x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 923 ms: 1.50x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 934 ms: 1.50x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 473 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 404 ms: 1.42x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 477 ms: 1.40x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 370 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 711 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 700 ms: 1.22x faster                                                   |
| async_generators           | 567 ms                                                       | 524 ms: 1.08x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 29.3 ms: 1.05x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 105 ms: 1.10x faster                                                   |
| pidigits       | 251 ms                                                       | 239 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 166 ms: 1.10x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.39 ms: 1.08x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 34.7 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_process   | 85.9 ms                                                      | 77.9 ms: 1.10x faster                                                  |
| xml_etree_parse     | 231 ms                                                       | 210 ms: 1.10x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.57 sec: 1.08x faster                                                 |
| xml_etree_iterparse | 177 ms                                                       | 166 ms: 1.07x faster                                                   |
| xml_etree_generate  | 122 ms                                                       | 115 ms: 1.06x faster                                                   |
| json_loads          | 34.3 us                                                      | 38.0 us: 1.11x slower                                                  |
| json_dumps          | 14.1 ms                                                      | 16.3 ms: 1.15x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (2): unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 16.0 ms: 1.05x slower                                                  |
| python_startup         | 22.4 ms                                                      | 27.0 ms: 1.20x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.12x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 72.1 ms                                                      | 62.8 ms: 1.15x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (3): genshi_text, django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 923 ms: 1.50x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 934 ms: 1.50x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 473 ms: 1.50x faster                                                   |
| deepcopy                   | 498 us                                                       | 340 us: 1.46x faster                                                   |
| async_tree_none            | 572 ms                                                       | 404 ms: 1.42x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 477 ms: 1.40x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 370 ms: 1.36x faster                                                   |
| spectral_norm              | 157 ms                                                       | 118 ms: 1.32x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 38.6 us: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 711 ms: 1.25x faster                                                   |
| telco                      | 12.2 ms                                                      | 9.93 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 700 ms: 1.22x faster                                                   |
| pylint                     | 470 ms                                                       | 390 ms: 1.21x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 5.63 ms: 1.20x faster                                                  |
| go                         | 191 ms                                                       | 160 ms: 1.20x faster                                                   |
| scimark_sor                | 179 ms                                                       | 154 ms: 1.16x faster                                                   |
| genshi_xml                 | 72.1 ms                                                      | 62.8 ms: 1.15x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 199 us: 1.14x faster                                                   |
| html5lib                   | 92.6 ms                                                      | 81.6 ms: 1.14x faster                                                  |
| sympy_str                  | 379 ms                                                       | 335 ms: 1.13x faster                                                   |
| chaos                      | 83.6 ms                                                      | 73.9 ms: 1.13x faster                                                  |
| fannkuch                   | 547 ms                                                       | 487 ms: 1.12x faster                                                   |
| richards                   | 65.5 ms                                                      | 58.6 ms: 1.12x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 89.7 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.67 sec: 1.11x faster                                                 |
| xml_etree_process          | 85.9 ms                                                      | 77.9 ms: 1.10x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 210 ms: 1.10x faster                                                   |
| regex_compile              | 182 ms                                                       | 166 ms: 1.10x faster                                                   |
| float                      | 116 ms                                                       | 105 ms: 1.10x faster                                                   |
| richards_super             | 73.2 ms                                                      | 67.1 ms: 1.09x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 911 ms: 1.08x faster                                                   |
| async_generators           | 567 ms                                                       | 524 ms: 1.08x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.70 sec: 1.08x faster                                                 |
| tomli_loads                | 2.78 sec                                                     | 2.57 sec: 1.08x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 4.39 ms: 1.08x faster                                                  |
| mdp                        | 3.80 sec                                                     | 3.53 sec: 1.08x faster                                                 |
| deltablue                  | 4.44 ms                                                      | 4.14 ms: 1.07x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.73 us: 1.07x faster                                                  |
| comprehensions             | 22.2 us                                                      | 20.8 us: 1.07x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 166 ms: 1.07x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 115 ms: 1.06x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 29.3 ms: 1.05x faster                                                  |
| pidigits                   | 251 ms                                                       | 239 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.94 sec                                                     | 1.85 sec: 1.05x faster                                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 71.4 ms: 1.05x faster                                                  |
| scimark_fft                | 473 ms                                                       | 452 ms: 1.05x faster                                                   |
| pyflate                    | 664 ms                                                       | 639 ms: 1.04x faster                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 16.0 ms: 1.05x slower                                                  |
| regex_v8                   | 32.8 ms                                                      | 34.7 ms: 1.06x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 32.1 ms: 1.06x slower                                                  |
| logging_silent             | 130 ns                                                       | 142 ns: 1.09x slower                                                   |
| coverage                   | 107 ms                                                       | 118 ms: 1.10x slower                                                   |
| json_loads                 | 34.3 us                                                      | 38.0 us: 1.11x slower                                                  |
| raytrace                   | 344 ms                                                       | 385 ms: 1.12x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 16.3 ms: 1.15x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.37 ms: 1.17x slower                                                  |
| python_startup             | 22.4 ms                                                      | 27.0 ms: 1.20x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 9.97 ms: 1.75x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 5.09 ms: 2.11x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 92.2 ms: 4.93x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (28): logging_simple, genshi_text, django_template, sympy_sum, sympy_expand, mako, pycparser, dulwich_log, deepcopy_reduce, unpickle_pure_python, meteor_contest, pathlib, sqlglot_transpile, nqueens, asyncio_websockets, thrift, sqlglot_normalize, nbody, pickle_pure_python, hexiom, sqlglot_parse, generators, 2to3, regex_dna, logging_format, scimark_lu, json, scimark_monte_carlo
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.065x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x