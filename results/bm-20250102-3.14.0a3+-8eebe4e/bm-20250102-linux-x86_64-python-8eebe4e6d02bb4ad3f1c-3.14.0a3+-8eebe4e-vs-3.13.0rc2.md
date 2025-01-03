# Results vs. 3.13.0rc2

- fork: python
- ref: 8eebe4e6d02bb4ad3f1c
- machine: linux-x86_64
- commit hash: 8eebe4e
- commit date: 2025-01-02
- overall geometric mean: 1.101x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 410 ms: 1.08x faster                                                   |
| docutils       | 4.01 sec                                                     | 3.51 sec: 1.14x faster                                                 |
| html5lib       | 92.6 ms                                                      | 81.3 ms: 1.14x faster                                                  |
| Geometric mean | (ref)                                                        | 1.12x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 820 ms: 1.71x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 838 ms: 1.66x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 432 ms: 1.55x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 466 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 336 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 383 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 643 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 683 ms: 1.30x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 707 ms: 1.08x faster                                                   |
| async_generators           | 567 ms                                                       | 538 ms: 1.06x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.36x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 100 ms: 1.15x faster                                                   |
| pidigits       | 251 ms                                                       | 231 ms: 1.09x faster                                                   |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.17 ms: 1.14x faster                                                  |
| regex_compile  | 182 ms                                                       | 161 ms: 1.13x faster                                                   |
| regex_dna      | 282 ms                                                       | 268 ms: 1.05x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 31.7 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                        | 1.09x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 147 ms: 1.20x faster                                                   |
| xml_etree_parse     | 231 ms                                                       | 204 ms: 1.13x faster                                                   |
| xml_etree_generate  | 122 ms                                                       | 109 ms: 1.12x faster                                                   |
| xml_etree_process   | 85.9 ms                                                      | 78.3 ms: 1.10x faster                                                  |
| tomli_loads         | 2.78 sec                                                     | 2.61 sec: 1.06x faster                                                 |
| json_dumps          | 14.1 ms                                                      | 14.6 ms: 1.03x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (3): json_loads, unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 14.7 ms: 1.04x faster                                                  |
| python_startup         | 22.4 ms                                                      | 23.3 ms: 1.04x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 72.1 ms                                                      | 60.0 ms: 1.20x faster                                                  |
| genshi_text    | 31.7 ms                                                      | 28.3 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 820 ms: 1.71x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 838 ms: 1.66x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 432 ms: 1.55x faster                                                   |
| deepcopy                   | 498 us                                                       | 321 us: 1.55x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 466 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 336 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 383 ms: 1.49x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 37.1 us: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 643 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 683 ms: 1.30x faster                                                   |
| pylint                     | 470 ms                                                       | 378 ms: 1.25x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.35 us: 1.22x faster                                                  |
| go                         | 191 ms                                                       | 157 ms: 1.22x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 147 ms: 1.20x faster                                                   |
| genshi_xml                 | 72.1 ms                                                      | 60.0 ms: 1.20x faster                                                  |
| spectral_norm              | 157 ms                                                       | 133 ms: 1.18x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.5 ms: 1.16x faster                                                  |
| float                      | 116 ms                                                       | 100 ms: 1.15x faster                                                   |
| pathlib                    | 29.9 ms                                                      | 26.2 ms: 1.14x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.51 sec: 1.14x faster                                                 |
| html5lib                   | 92.6 ms                                                      | 81.3 ms: 1.14x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.17 ms: 1.14x faster                                                  |
| regex_compile              | 182 ms                                                       | 161 ms: 1.13x faster                                                   |
| richards                   | 65.5 ms                                                      | 57.8 ms: 1.13x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 204 ms: 1.13x faster                                                   |
| richards_super             | 73.2 ms                                                      | 65.0 ms: 1.13x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 28.3 ms: 1.12x faster                                                  |
| xml_etree_generate         | 122 ms                                                       | 109 ms: 1.12x faster                                                   |
| thrift                     | 1.10 ms                                                      | 984 us: 1.12x faster                                                   |
| scimark_sor                | 179 ms                                                       | 160 ms: 1.12x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.57 us: 1.12x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 27.3 ms: 1.11x faster                                                  |
| xml_etree_process          | 85.9 ms                                                      | 78.3 ms: 1.10x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 206 us: 1.09x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.75 sec: 1.09x faster                                                 |
| json                       | 6.51 ms                                                      | 5.97 ms: 1.09x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 908 ms: 1.09x faster                                                   |
| pidigits                   | 251 ms                                                       | 231 ms: 1.09x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.50 sec: 1.09x faster                                                 |
| 2to3                       | 445 ms                                                       | 410 ms: 1.08x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 707 ms: 1.08x faster                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.03 ms: 1.08x faster                                                  |
| chaos                      | 83.6 ms                                                      | 77.2 ms: 1.08x faster                                                  |
| nqueens                    | 112 ms                                                       | 103 ms: 1.08x faster                                                   |
| meteor_contest             | 150 ms                                                       | 139 ms: 1.08x faster                                                   |
| deltablue                  | 4.44 ms                                                      | 4.13 ms: 1.07x faster                                                  |
| pyflate                    | 664 ms                                                       | 621 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.94 sec                                                     | 1.82 sec: 1.07x faster                                                 |
| tomli_loads                | 2.78 sec                                                     | 2.61 sec: 1.06x faster                                                 |
| fannkuch                   | 547 ms                                                       | 517 ms: 1.06x faster                                                   |
| async_generators           | 567 ms                                                       | 538 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.42 ms: 1.05x faster                                                  |
| regex_dna                  | 282 ms                                                       | 268 ms: 1.05x faster                                                   |
| generators                 | 40.0 ms                                                      | 38.1 ms: 1.05x faster                                                  |
| scimark_fft                | 473 ms                                                       | 451 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 86.3 ms: 1.05x faster                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 71.3 ms: 1.05x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 96.1 ms: 1.04x faster                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 14.7 ms: 1.04x faster                                                  |
| comprehensions             | 22.2 us                                                      | 21.4 us: 1.04x faster                                                  |
| regex_v8                   | 32.8 ms                                                      | 31.7 ms: 1.03x faster                                                  |
| raytrace                   | 344 ms                                                       | 336 ms: 1.02x faster                                                   |
| logging_silent             | 130 ns                                                       | 134 ns: 1.03x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 14.6 ms: 1.03x slower                                                  |
| python_startup             | 22.4 ms                                                      | 23.3 ms: 1.04x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.96 ms: 1.40x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.57 ms: 1.48x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 89.3 ms: 4.78x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.08x faster                                                           |

Benchmark hidden because not significant (20): logging_simple, sympy_str, coroutines, sympy_expand, json_loads, django_template, sqlglot_normalize, sympy_sum, unpickle_pure_python, mako, pycparser, dulwich_log, nbody, scimark_lu, logging_format, bench_thread_pool, pickle_pure_python, sqlglot_parse, coverage, hexiom
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.101x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x