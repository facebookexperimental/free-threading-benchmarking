# Results vs. 3.13.0rc2

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.086x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.55 sec: 1.13x faster                                                |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 900 ms: 1.54x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 466 ms: 1.52x faster                                                  |
| async_tree_none            | 572 ms                                                       | 380 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 934 ms: 1.50x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 471 ms: 1.42x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 375 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 691 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 696 ms: 1.22x faster                                                  |
| async_generators           | 567 ms                                                       | 508 ms: 1.12x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 717 ms: 1.07x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 101 ms: 1.14x faster                                                  |
| nbody          | 119 ms                                                       | 125 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.29 ms: 1.10x faster                                                 |
| regex_compile  | 182 ms                                                       | 165 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|---------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 145 ms: 1.22x faster                                                  |
| xml_etree_parse     | 231 ms                                                       | 197 ms: 1.17x faster                                                  |
| xml_etree_generate  | 122 ms                                                       | 110 ms: 1.12x faster                                                  |
| tomli_loads         | 2.78 sec                                                     | 2.50 sec: 1.11x faster                                                |
| xml_etree_process   | 85.9 ms                                                      | 81.3 ms: 1.06x faster                                                 |
| json_dumps          | 14.1 ms                                                      | 14.9 ms: 1.05x slower                                                 |
| json_loads          | 34.3 us                                                      | 42.1 us: 1.23x slower                                                 |
| Geometric mean      | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (2): unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 17.3 ms: 1.13x slower                                                 |
| python_startup         | 22.4 ms                                                      | 29.3 ms: 1.31x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.22x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml     | 72.1 ms                                                      | 63.9 ms: 1.13x faster                                                 |
| genshi_text    | 31.7 ms                                                      | 28.7 ms: 1.10x faster                                                 |
| mako           | 15.9 ms                                                      | 16.8 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 3.80 sec                                                     | 1.93 sec: 1.97x faster                                                |
| async_tree_io              | 1.39 sec                                                     | 900 ms: 1.54x faster                                                  |
| deepcopy                   | 498 us                                                       | 327 us: 1.52x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 466 ms: 1.52x faster                                                  |
| async_tree_none            | 572 ms                                                       | 380 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 934 ms: 1.50x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 471 ms: 1.42x faster                                                  |
| go                         | 191 ms                                                       | 142 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 375 ms: 1.34x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 38.2 us: 1.31x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 691 ms: 1.29x faster                                                  |
| telco                      | 12.2 ms                                                      | 9.53 ms: 1.28x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 3.29 us: 1.25x faster                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 696 ms: 1.22x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 145 ms: 1.22x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 197 ms: 1.17x faster                                                  |
| spectral_norm              | 157 ms                                                       | 134 ms: 1.17x faster                                                  |
| pylint                     | 470 ms                                                       | 407 ms: 1.16x faster                                                  |
| richards_super             | 73.2 ms                                                      | 63.6 ms: 1.15x faster                                                 |
| richards                   | 65.5 ms                                                      | 57.2 ms: 1.14x faster                                                 |
| float                      | 116 ms                                                       | 101 ms: 1.14x faster                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 2.53 ms: 1.14x faster                                                 |
| scimark_sor                | 179 ms                                                       | 158 ms: 1.13x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.55 sec: 1.13x faster                                                |
| genshi_xml                 | 72.1 ms                                                      | 63.9 ms: 1.13x faster                                                 |
| sympy_str                  | 379 ms                                                       | 338 ms: 1.12x faster                                                  |
| xml_etree_generate         | 122 ms                                                       | 110 ms: 1.12x faster                                                  |
| async_generators           | 567 ms                                                       | 508 ms: 1.12x faster                                                  |
| chaos                      | 83.6 ms                                                      | 75.0 ms: 1.11x faster                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 81.4 ms: 1.11x faster                                                 |
| tomli_loads                | 2.78 sec                                                     | 2.50 sec: 1.11x faster                                                |
| regex_effbot               | 4.74 ms                                                      | 4.29 ms: 1.10x faster                                                 |
| genshi_text                | 31.7 ms                                                      | 28.7 ms: 1.10x faster                                                 |
| regex_compile              | 182 ms                                                       | 165 ms: 1.10x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 904 ms: 1.09x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.20 ms: 1.09x faster                                                 |
| scimark_fft                | 473 ms                                                       | 440 ms: 1.08x faster                                                  |
| comprehensions             | 22.2 us                                                      | 20.8 us: 1.07x faster                                                 |
| asyncio_websockets         | 766 ms                                                       | 717 ms: 1.07x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.77 us: 1.06x faster                                                 |
| xml_etree_process          | 85.9 ms                                                      | 81.3 ms: 1.06x faster                                                 |
| meteor_contest             | 150 ms                                                       | 143 ms: 1.05x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 95.2 ms: 1.05x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 28.5 ms: 1.05x faster                                                 |
| nqueens                    | 112 ms                                                       | 107 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 1.85 sec: 1.05x faster                                                |
| pyflate                    | 664 ms                                                       | 636 ms: 1.04x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 6.05 sec: 1.04x faster                                                |
| fannkuch                   | 547 ms                                                       | 530 ms: 1.03x faster                                                  |
| mako                       | 15.9 ms                                                      | 16.8 ms: 1.05x slower                                                 |
| nbody                      | 119 ms                                                       | 125 ms: 1.05x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 14.9 ms: 1.05x slower                                                 |
| logging_simple             | 8.56 us                                                      | 9.03 us: 1.06x slower                                                 |
| logging_format             | 9.24 us                                                      | 9.82 us: 1.06x slower                                                 |
| json                       | 6.51 ms                                                      | 6.96 ms: 1.07x slower                                                 |
| coverage                   | 107 ms                                                       | 115 ms: 1.07x slower                                                  |
| generators                 | 40.0 ms                                                      | 44.6 ms: 1.11x slower                                                 |
| python_startup_no_site     | 15.3 ms                                                      | 17.3 ms: 1.13x slower                                                 |
| json_loads                 | 34.3 us                                                      | 42.1 us: 1.23x slower                                                 |
| python_startup             | 22.4 ms                                                      | 29.3 ms: 1.31x slower                                                 |
| create_gc_cycles           | 2.41 ms                                                      | 3.50 ms: 1.45x slower                                                 |
| gc_traversal               | 5.70 ms                                                      | 8.36 ms: 1.47x slower                                                 |
| bench_mp_pool              | 18.7 ms                                                      | 90.7 ms: 4.85x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                          |

Benchmark hidden because not significant (19): sympy_integrate, dulwich_log, typing_runtime_protocols, pycparser, unpickle_pure_python, sympy_expand, deltablue, hexiom, logging_silent, 2to3, pidigits, raytrace, django_template, sympy_sum, coroutines, pickle_pure_python, scimark_lu, regex_dna, regex_v8
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250408-3.14.0a6+-09d4621/bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.086x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.14x