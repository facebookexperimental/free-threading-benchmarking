# Results vs. 3.13.0rc2

- fork: python
- ref: 99d965635ae2ac4bffdc
- machine: linux-x86_64
- commit hash: 99d9656
- commit date: 2025-02-17
- overall geometric mean: 1.062x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.56 sec: 1.13x faster                                                 |
| html5lib       | 92.6 ms                                                      | 82.9 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.09x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 919 ms: 1.53x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 931 ms: 1.49x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 480 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 464 ms: 1.44x faster                                                   |
| async_tree_none            | 572 ms                                                       | 410 ms: 1.40x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 403 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 719 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 697 ms: 1.22x faster                                                   |
| async_generators           | 567 ms                                                       | 545 ms: 1.04x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 98.6 ms: 1.18x faster                                                  |
| pidigits       | 251 ms                                                       | 226 ms: 1.11x faster                                                   |
| nbody          | 119 ms                                                       | 124 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.20 ms: 1.13x faster                                                  |
| regex_compile  | 182 ms                                                       | 171 ms: 1.06x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 35.0 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 150 ms: 1.18x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 201 ms: 1.15x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.53 sec: 1.10x faster                                                 |
| unpickle_pure_python | 290 us                                                       | 303 us: 1.04x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 16.1 ms: 1.14x slower                                                  |
| json_loads           | 34.3 us                                                      | 40.3 us: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (3): pickle_pure_python, xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 26.6 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                        | 1.10x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 31.7 ms                                                      | 27.8 ms: 1.14x faster                                                  |
| genshi_xml     | 72.1 ms                                                      | 65.2 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 919 ms: 1.53x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 931 ms: 1.49x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 480 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 464 ms: 1.44x faster                                                   |
| async_tree_none            | 572 ms                                                       | 410 ms: 1.40x faster                                                   |
| deepcopy                   | 498 us                                                       | 379 us: 1.31x faster                                                   |
| spectral_norm              | 157 ms                                                       | 121 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 403 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 719 ms: 1.24x faster                                                   |
| go                         | 191 ms                                                       | 155 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 697 ms: 1.22x faster                                                   |
| pylint                     | 470 ms                                                       | 385 ms: 1.22x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 41.3 us: 1.21x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 150 ms: 1.18x faster                                                   |
| float                      | 116 ms                                                       | 98.6 ms: 1.18x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.5 ms: 1.16x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 5.81 ms: 1.16x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 201 ms: 1.15x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 27.8 ms: 1.14x faster                                                  |
| scimark_sor                | 179 ms                                                       | 158 ms: 1.13x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.20 ms: 1.13x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.56 sec: 1.13x faster                                                 |
| richards                   | 65.5 ms                                                      | 58.2 ms: 1.12x faster                                                  |
| thrift                     | 1.10 ms                                                      | 983 us: 1.12x faster                                                   |
| html5lib                   | 92.6 ms                                                      | 82.9 ms: 1.12x faster                                                  |
| pidigits                   | 251 ms                                                       | 226 ms: 1.11x faster                                                   |
| chaos                      | 83.6 ms                                                      | 75.6 ms: 1.11x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 65.2 ms: 1.11x faster                                                  |
| logging_format             | 9.24 us                                                      | 8.38 us: 1.10x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.53 sec: 1.10x faster                                                 |
| comprehensions             | 22.2 us                                                      | 20.2 us: 1.10x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.76 us: 1.09x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 27.8 ms: 1.09x faster                                                  |
| sympy_str                  | 379 ms                                                       | 350 ms: 1.08x faster                                                   |
| fannkuch                   | 547 ms                                                       | 508 ms: 1.08x faster                                                   |
| scimark_fft                | 473 ms                                                       | 442 ms: 1.07x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.87 sec: 1.07x faster                                                 |
| nqueens                    | 112 ms                                                       | 105 ms: 1.07x faster                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.06 ms: 1.07x faster                                                  |
| regex_compile              | 182 ms                                                       | 171 ms: 1.06x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.58 sec: 1.06x faster                                                 |
| sqlite_synth               | 3.99 us                                                      | 3.81 us: 1.05x faster                                                  |
| async_generators           | 567 ms                                                       | 545 ms: 1.04x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 948 ms: 1.04x faster                                                   |
| nbody                      | 119 ms                                                       | 124 ms: 1.04x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 303 us: 1.04x slower                                                   |
| logging_silent             | 130 ns                                                       | 136 ns: 1.05x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 8.49 ms: 1.05x slower                                                  |
| raytrace                   | 344 ms                                                       | 361 ms: 1.05x slower                                                   |
| regex_v8                   | 32.8 ms                                                      | 35.0 ms: 1.07x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 80.0 ms: 1.07x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.13 ms: 1.09x slower                                                  |
| json                       | 6.51 ms                                                      | 7.38 ms: 1.13x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 16.1 ms: 1.14x slower                                                  |
| coverage                   | 107 ms                                                       | 124 ms: 1.16x slower                                                   |
| json_loads                 | 34.3 us                                                      | 40.3 us: 1.17x slower                                                  |
| python_startup             | 22.4 ms                                                      | 26.6 ms: 1.19x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.46 ms: 1.43x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.78 ms: 1.54x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 91.0 ms: 4.87x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (28): deltablue, typing_runtime_protocols, coroutines, pickle_pure_python, sympy_sum, crypto_pyaes, richards_super, scimark_monte_carlo, 2to3, meteor_contest, asyncio_websockets, xml_etree_generate, pyflate, regex_dna, sympy_expand, pprint_pformat, logging_simple, xml_etree_process, pycparser, dulwich_log, django_template, sqlglot_normalize, python_startup_no_site, scimark_lu, mako, sqlglot_parse, generators, pathlib
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.13x