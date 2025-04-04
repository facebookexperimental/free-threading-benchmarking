# Results vs. 3.13.0rc2

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: linux-x86_64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.073x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 473 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 709 ms                                                       | 478 ms: 1.48x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 939 ms: 1.48x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 952 ms: 1.47x faster                                                   |
| async_tree_none            | 572 ms                                                       | 389 ms: 1.47x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 486 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 384 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 714 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 693 ms: 1.23x faster                                                   |
| async_generators           | 567 ms                                                       | 525 ms: 1.08x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 730 ms: 1.05x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 97.7 ms: 1.19x faster                                                  |
| pidigits       | 251 ms                                                       | 239 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                       | 129 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 29.2 ms: 1.12x faster                                                  |
| regex_compile  | 182 ms                                                       | 167 ms: 1.09x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.38 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark         | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse   | 231 ms                                                       | 203 ms: 1.14x faster                                                   |
| xml_etree_process | 85.9 ms                                                      | 77.0 ms: 1.12x faster                                                  |
| tomli_loads       | 2.78 sec                                                     | 2.52 sec: 1.10x faster                                                 |
| json_dumps        | 14.1 ms                                                      | 15.6 ms: 1.11x slower                                                  |
| json_loads        | 34.3 us                                                      | 39.7 us: 1.16x slower                                                  |
| Geometric mean    | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_iterparse, unpickle_pure_python, xml_etree_generate, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.3 ms: 1.33x slower                                                  |
| python_startup         | 22.4 ms                                                      | 31.8 ms: 1.42x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 28.7 ms: 1.10x faster                                                  |
| django_template | 44.3 ms                                                      | 47.1 ms: 1.06x slower                                                  |
| mako            | 15.9 ms                                                      | 18.7 ms: 1.17x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 3.80 sec                                                     | 1.98 sec: 1.92x faster                                                 |
| async_tree_memoization     | 709 ms                                                       | 478 ms: 1.48x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 939 ms: 1.48x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 952 ms: 1.47x faster                                                   |
| async_tree_none            | 572 ms                                                       | 389 ms: 1.47x faster                                                   |
| deepcopy                   | 498 us                                                       | 344 us: 1.45x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 486 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 384 ms: 1.31x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 39.0 us: 1.28x faster                                                  |
| go                         | 191 ms                                                       | 153 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 714 ms: 1.24x faster                                                   |
| spectral_norm              | 157 ms                                                       | 126 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 693 ms: 1.23x faster                                                   |
| float                      | 116 ms                                                       | 97.7 ms: 1.19x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 5.75 ms: 1.18x faster                                                  |
| pylint                     | 470 ms                                                       | 405 ms: 1.16x faster                                                   |
| scimark_sor                | 179 ms                                                       | 154 ms: 1.16x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.54 us: 1.16x faster                                                  |
| richards_super             | 73.2 ms                                                      | 63.5 ms: 1.15x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.6 ms: 1.15x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 203 ms: 1.14x faster                                                   |
| dulwich_log                | 93.7 ms                                                      | 83.0 ms: 1.13x faster                                                  |
| chaos                      | 83.6 ms                                                      | 74.4 ms: 1.12x faster                                                  |
| regex_v8                   | 32.8 ms                                                      | 29.2 ms: 1.12x faster                                                  |
| xml_etree_process          | 85.9 ms                                                      | 77.0 ms: 1.12x faster                                                  |
| richards                   | 65.5 ms                                                      | 58.7 ms: 1.12x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 28.7 ms: 1.10x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.52 sec: 1.10x faster                                                 |
| pyflate                    | 664 ms                                                       | 606 ms: 1.10x faster                                                   |
| regex_compile              | 182 ms                                                       | 167 ms: 1.09x faster                                                   |
| sympy_integrate            | 30.2 ms                                                      | 27.7 ms: 1.09x faster                                                  |
| fannkuch                   | 547 ms                                                       | 505 ms: 1.08x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.38 ms: 1.08x faster                                                  |
| async_generators           | 567 ms                                                       | 525 ms: 1.08x faster                                                   |
| scimark_fft                | 473 ms                                                       | 438 ms: 1.08x faster                                                   |
| crypto_pyaes               | 100 ms                                                       | 93.0 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 84.5 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 920 ms: 1.07x faster                                                   |
| sympy_sum                  | 210 ms                                                       | 198 ms: 1.06x faster                                                   |
| meteor_contest             | 150 ms                                                       | 142 ms: 1.06x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.78 us: 1.05x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 214 us: 1.05x faster                                                   |
| pidigits                   | 251 ms                                                       | 239 ms: 1.05x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 730 ms: 1.05x faster                                                   |
| sympy_str                  | 379 ms                                                       | 361 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.94 sec                                                     | 1.87 sec: 1.04x faster                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 6.12 sec: 1.03x faster                                                 |
| coverage                   | 107 ms                                                       | 112 ms: 1.05x slower                                                   |
| 2to3                       | 445 ms                                                       | 473 ms: 1.06x slower                                                   |
| django_template            | 44.3 ms                                                      | 47.1 ms: 1.06x slower                                                  |
| json                       | 6.51 ms                                                      | 7.03 ms: 1.08x slower                                                  |
| nbody                      | 119 ms                                                       | 129 ms: 1.08x slower                                                   |
| generators                 | 40.0 ms                                                      | 43.6 ms: 1.09x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.6 ms: 1.11x slower                                                  |
| logging_format             | 9.24 us                                                      | 10.2 us: 1.11x slower                                                  |
| json_loads                 | 34.3 us                                                      | 39.7 us: 1.16x slower                                                  |
| mako                       | 15.9 ms                                                      | 18.7 ms: 1.17x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 20.3 ms: 1.33x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.88 ms: 1.34x slower                                                  |
| python_startup             | 22.4 ms                                                      | 31.8 ms: 1.42x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.37 ms: 1.47x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 4.09 ms: 1.69x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 95.9 ms: 5.13x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (19): xml_etree_iterparse, nqueens, raytrace, docutils, logging_silent, comprehensions, pathlib, hexiom, genshi_xml, pycparser, unpickle_pure_python, xml_etree_generate, regex_dna, scimark_lu, sympy_expand, coroutines, deltablue, logging_simple, pickle_pure_python
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.14x