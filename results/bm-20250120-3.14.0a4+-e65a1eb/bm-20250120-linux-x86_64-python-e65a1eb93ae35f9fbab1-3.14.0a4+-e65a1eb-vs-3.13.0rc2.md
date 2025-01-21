# Results vs. 3.13.0rc2

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.025x faster
- HPT reliability: 94.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 476 ms: 1.07x slower                                                   |
| docutils       | 4.01 sec                                                     | 3.71 sec: 1.08x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 877 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 909 ms: 1.54x faster                                                   |
| async_tree_none            | 572 ms                                                       | 388 ms: 1.48x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 490 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 364 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 660 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 500 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 649 ms: 1.31x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 716 ms: 1.07x faster                                                   |
| async_generators           | 567 ms                                                       | 539 ms: 1.05x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 129 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_compile, regex_dna, regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 156 ms: 1.13x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 215 ms: 1.08x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.61 sec: 1.06x faster                                                 |
| pickle_pure_python   | 416 us                                                       | 438 us: 1.05x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 316 us: 1.09x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 15.6 ms: 1.10x slower                                                  |
| json_loads           | 34.3 us                                                      | 39.6 us: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 18.4 ms: 1.20x slower                                                  |
| python_startup         | 22.4 ms                                                      | 30.3 ms: 1.35x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.28x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 28.5 ms: 1.11x faster                                                  |
| genshi_xml      | 72.1 ms                                                      | 68.1 ms: 1.06x faster                                                  |
| django_template | 44.3 ms                                                      | 49.7 ms: 1.12x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 877 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 909 ms: 1.54x faster                                                   |
| async_tree_none            | 572 ms                                                       | 388 ms: 1.48x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 490 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 364 ms: 1.38x faster                                                   |
| deepcopy                   | 498 us                                                       | 360 us: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 660 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 500 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 649 ms: 1.31x faster                                                   |
| go                         | 191 ms                                                       | 151 ms: 1.27x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 40.1 us: 1.25x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.38 us: 1.21x faster                                                  |
| pylint                     | 470 ms                                                       | 413 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 156 ms: 1.13x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 28.5 ms: 1.11x faster                                                  |
| richards_super             | 73.2 ms                                                      | 66.8 ms: 1.10x faster                                                  |
| spectral_norm              | 157 ms                                                       | 143 ms: 1.09x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.71 sec: 1.08x faster                                                 |
| richards                   | 65.5 ms                                                      | 60.6 ms: 1.08x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 215 ms: 1.08x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 716 ms: 1.07x faster                                                   |
| sympy_sum                  | 210 ms                                                       | 197 ms: 1.07x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.89 sec: 1.07x faster                                                 |
| sympy_integrate            | 30.2 ms                                                      | 28.3 ms: 1.07x faster                                                  |
| scimark_sor                | 179 ms                                                       | 167 ms: 1.07x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.61 sec: 1.06x faster                                                 |
| fannkuch                   | 547 ms                                                       | 514 ms: 1.06x faster                                                   |
| genshi_xml                 | 72.1 ms                                                      | 68.1 ms: 1.06x faster                                                  |
| async_generators           | 567 ms                                                       | 539 ms: 1.05x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.82 us: 1.05x faster                                                  |
| scimark_fft                | 473 ms                                                       | 453 ms: 1.04x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.02 sec: 1.04x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 438 us: 1.05x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.06 sec: 1.06x slower                                                 |
| thrift                     | 1.10 ms                                                      | 1.17 ms: 1.06x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 96.3 ms: 1.06x slower                                                  |
| 2to3                       | 445 ms                                                       | 476 ms: 1.07x slower                                                   |
| logging_silent             | 130 ns                                                       | 139 ns: 1.07x slower                                                   |
| generators                 | 40.0 ms                                                      | 42.8 ms: 1.07x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 157 ms: 1.07x slower                                                   |
| nbody                      | 119 ms                                                       | 129 ms: 1.09x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 316 us: 1.09x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 8.85 ms: 1.09x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.6 ms: 1.10x slower                                                  |
| raytrace                   | 344 ms                                                       | 383 ms: 1.11x slower                                                   |
| coverage                   | 107 ms                                                       | 120 ms: 1.12x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 105 ms: 1.12x slower                                                   |
| django_template            | 44.3 ms                                                      | 49.7 ms: 1.12x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 84.2 ms: 1.13x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 161 ms: 1.15x slower                                                   |
| json_loads                 | 34.3 us                                                      | 39.6 us: 1.16x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 263 us: 1.17x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 18.4 ms: 1.20x slower                                                  |
| logging_format             | 9.24 us                                                      | 11.2 us: 1.21x slower                                                  |
| json                       | 6.51 ms                                                      | 7.94 ms: 1.22x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.81 ms: 1.32x slower                                                  |
| python_startup             | 22.4 ms                                                      | 30.3 ms: 1.35x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.93 ms: 1.63x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 9.71 ms: 1.70x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 102 ms: 5.47x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (28): float, meteor_contest, deltablue, html5lib, telco, scimark_sparse_mat_mult, regex_compile, pycparser, nqueens, comprehensions, crypto_pyaes, sqlglot_parse, sqlglot_transpile, sympy_expand, pathlib, coroutines, regex_dna, mdp, regex_effbot, mako, xml_etree_generate, pyflate, regex_v8, pidigits, xml_etree_process, chaos, sympy_str, logging_simple
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 94.77% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x