# Results vs. 3.13.0rc2

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: linux-x86_64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.086x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.68 sec: 1.09x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 709 ms                                                       | 449 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 890 ms: 1.57x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 883 ms: 1.57x faster                                                   |
| async_tree_none            | 572 ms                                                       | 374 ms: 1.53x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 482 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 674 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 384 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 674 ms: 1.26x faster                                                   |
| async_generators           | 567 ms                                                       | 535 ms: 1.06x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 731 ms: 1.05x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 32.8 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 95.2 ms: 1.22x faster                                                  |
| pidigits       | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| nbody          | 119 ms                                                       | 128 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 169 ms: 1.08x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.39 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 145 ms: 1.22x faster                                                   |
| xml_etree_parse     | 231 ms                                                       | 202 ms: 1.14x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.46 sec: 1.13x faster                                                 |
| xml_etree_process   | 85.9 ms                                                      | 80.4 ms: 1.07x faster                                                  |
| json_loads          | 34.3 us                                                      | 36.5 us: 1.07x slower                                                  |
| json_dumps          | 14.1 ms                                                      | 16.4 ms: 1.16x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_generate, unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 17.6 ms: 1.15x slower                                                  |
| python_startup         | 22.4 ms                                                      | 29.8 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 65.2 ms: 1.11x faster                                                  |
| django_template | 44.3 ms                                                      | 43.0 ms: 1.03x faster                                                  |
| Geometric mean  | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (2): genshi_text, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 3.80 sec                                                     | 1.94 sec: 1.95x faster                                                 |
| async_tree_memoization     | 709 ms                                                       | 449 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 890 ms: 1.57x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 883 ms: 1.57x faster                                                   |
| async_tree_none            | 572 ms                                                       | 374 ms: 1.53x faster                                                   |
| deepcopy                   | 498 us                                                       | 333 us: 1.49x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 482 ms: 1.39x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 36.7 us: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 674 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 384 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 674 ms: 1.26x faster                                                   |
| go                         | 191 ms                                                       | 152 ms: 1.26x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 145 ms: 1.22x faster                                                   |
| telco                      | 12.2 ms                                                      | 9.95 ms: 1.22x faster                                                  |
| float                      | 116 ms                                                       | 95.2 ms: 1.22x faster                                                  |
| chaos                      | 83.6 ms                                                      | 69.9 ms: 1.20x faster                                                  |
| scimark_sor                | 179 ms                                                       | 151 ms: 1.18x faster                                                   |
| spectral_norm              | 157 ms                                                       | 134 ms: 1.17x faster                                                   |
| pylint                     | 470 ms                                                       | 403 ms: 1.17x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.47 us: 1.15x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 202 ms: 1.14x faster                                                   |
| richards_super             | 73.2 ms                                                      | 64.4 ms: 1.14x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.46 sec: 1.13x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 3.69 us: 1.11x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 65.2 ms: 1.11x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.12 ms: 1.10x faster                                                  |
| pyflate                    | 664 ms                                                       | 605 ms: 1.10x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 905 ms: 1.09x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.68 sec: 1.09x faster                                                 |
| typing_runtime_protocols   | 226 us                                                       | 207 us: 1.09x faster                                                   |
| dulwich_log                | 93.7 ms                                                      | 86.0 ms: 1.09x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 27.9 ms: 1.09x faster                                                  |
| scimark_fft                | 473 ms                                                       | 438 ms: 1.08x faster                                                   |
| regex_compile              | 182 ms                                                       | 169 ms: 1.08x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.39 ms: 1.08x faster                                                  |
| fannkuch                   | 547 ms                                                       | 511 ms: 1.07x faster                                                   |
| xml_etree_process          | 85.9 ms                                                      | 80.4 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 1.82 sec: 1.07x faster                                                 |
| richards                   | 65.5 ms                                                      | 61.7 ms: 1.06x faster                                                  |
| async_generators           | 567 ms                                                       | 535 ms: 1.06x faster                                                   |
| pathlib                    | 29.9 ms                                                      | 28.2 ms: 1.06x faster                                                  |
| pidigits                   | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.97 sec: 1.05x faster                                                 |
| asyncio_websockets         | 766 ms                                                       | 731 ms: 1.05x faster                                                   |
| django_template            | 44.3 ms                                                      | 43.0 ms: 1.03x faster                                                  |
| raytrace                   | 344 ms                                                       | 336 ms: 1.03x faster                                                   |
| scimark_lu                 | 146 ms                                                       | 155 ms: 1.06x slower                                                   |
| coroutines                 | 30.9 ms                                                      | 32.8 ms: 1.06x slower                                                  |
| json_loads                 | 34.3 us                                                      | 36.5 us: 1.07x slower                                                  |
| generators                 | 40.0 ms                                                      | 43.0 ms: 1.07x slower                                                  |
| nbody                      | 119 ms                                                       | 128 ms: 1.08x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 17.6 ms: 1.15x slower                                                  |
| json                       | 6.51 ms                                                      | 7.54 ms: 1.16x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 16.4 ms: 1.16x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.60 ms: 1.25x slower                                                  |
| python_startup             | 22.4 ms                                                      | 29.8 ms: 1.33x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.62 ms: 1.34x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.64 ms: 1.51x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 96.7 ms: 5.17x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (23): sympy_str, sympy_expand, logging_simple, logging_silent, sympy_sum, xml_etree_generate, regex_v8, deltablue, logging_format, comprehensions, genshi_text, coverage, regex_dna, nqueens, meteor_contest, crypto_pyaes, pycparser, scimark_monte_carlo, unpickle_pure_python, 2to3, hexiom, mako, pickle_pure_python
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.086x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x