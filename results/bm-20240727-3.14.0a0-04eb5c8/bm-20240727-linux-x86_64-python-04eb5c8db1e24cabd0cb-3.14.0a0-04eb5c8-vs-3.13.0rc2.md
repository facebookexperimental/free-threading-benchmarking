# Results vs. 3.13.0rc2

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tornado_http   | 251 ms                                                       | 228 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (3): 2to3, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 499 ms: 1.15x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 1.22 sec: 1.15x faster                                                |
| async_tree_memoization_tg  | 670 ms                                                       | 591 ms: 1.13x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 626 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 794 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 451 ms: 1.12x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 1.26 sec: 1.10x faster                                                |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 806 ms: 1.06x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                          |

Benchmark hidden because not significant (5): asyncio_websockets, asyncio_tcp, asyncio_tcp_ssl, async_generators, coroutines

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): pidigits, float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 35.8 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (3): regex_compile, regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 158 ms: 1.12x faster                                                  |
| pickle_list          | 6.86 us                                                      | 6.33 us: 1.08x faster                                                 |
| xml_etree_process    | 85.9 ms                                                      | 81.3 ms: 1.06x faster                                                 |
| tomli_loads          | 2.78 sec                                                     | 2.66 sec: 1.05x faster                                                |
| xml_etree_generate   | 122 ms                                                       | 117 ms: 1.04x faster                                                  |
| unpickle_pure_python | 290 us                                                       | 306 us: 1.05x slower                                                  |
| unpickle_list        | 6.68 us                                                      | 7.22 us: 1.08x slower                                                 |
| json_loads           | 34.3 us                                                      | 37.1 us: 1.08x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 15.5 ms: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (5): unpickle, pickle_dict, xml_etree_parse, pickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 31.7 ms                                                      | 30.2 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (3): django_template, genshi_xml, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deepcopy                   | 498 us                                                       | 372 us: 1.34x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 38.4 us: 1.31x faster                                                 |
| async_tree_none            | 572 ms                                                       | 499 ms: 1.15x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 1.22 sec: 1.15x faster                                                |
| async_tree_memoization_tg  | 670 ms                                                       | 591 ms: 1.13x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 626 ms: 1.13x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 5.99 ms: 1.13x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 3.64 us: 1.13x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 26.6 ms: 1.12x faster                                                 |
| xml_etree_iterparse        | 177 ms                                                       | 158 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 794 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 451 ms: 1.12x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.9 ms: 1.11x faster                                                 |
| richards_super             | 73.2 ms                                                      | 66.2 ms: 1.11x faster                                                 |
| unpack_sequence            | 74.3 ns                                                      | 67.4 ns: 1.10x faster                                                 |
| tornado_http               | 251 ms                                                       | 228 ms: 1.10x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 1.26 sec: 1.10x faster                                                |
| sympy_str                  | 379 ms                                                       | 345 ms: 1.10x faster                                                  |
| meteor_contest             | 150 ms                                                       | 138 ms: 1.09x faster                                                  |
| pickle_list                | 6.86 us                                                      | 6.33 us: 1.08x faster                                                 |
| deltablue                  | 4.44 ms                                                      | 4.11 ms: 1.08x faster                                                 |
| logging_simple             | 8.56 us                                                      | 7.95 us: 1.08x faster                                                 |
| sympy_integrate            | 30.2 ms                                                      | 28.1 ms: 1.08x faster                                                 |
| comprehensions             | 22.2 us                                                      | 20.9 us: 1.06x faster                                                 |
| scimark_sor                | 179 ms                                                       | 168 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 806 ms: 1.06x faster                                                  |
| chaos                      | 83.6 ms                                                      | 79.1 ms: 1.06x faster                                                 |
| xml_etree_process          | 85.9 ms                                                      | 81.3 ms: 1.06x faster                                                 |
| genshi_text                | 31.7 ms                                                      | 30.2 ms: 1.05x faster                                                 |
| tomli_loads                | 2.78 sec                                                     | 2.66 sec: 1.05x faster                                                |
| xml_etree_generate         | 122 ms                                                       | 117 ms: 1.04x faster                                                  |
| mdp                        | 3.80 sec                                                     | 3.64 sec: 1.04x faster                                                |
| spectral_norm              | 157 ms                                                       | 150 ms: 1.04x faster                                                  |
| gc_traversal               | 5.70 ms                                                      | 5.48 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 87.1 ms: 1.04x faster                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 6.13 sec: 1.03x faster                                                |
| pycparser                  | 1.57 sec                                                     | 1.63 sec: 1.04x slower                                                |
| hexiom                     | 8.11 ms                                                      | 8.49 ms: 1.05x slower                                                 |
| unpickle_pure_python       | 290 us                                                       | 306 us: 1.05x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 155 ms: 1.06x slower                                                  |
| unpickle_list              | 6.68 us                                                      | 7.22 us: 1.08x slower                                                 |
| json_loads                 | 34.3 us                                                      | 37.1 us: 1.08x slower                                                 |
| regex_v8                   | 32.8 ms                                                      | 35.8 ms: 1.09x slower                                                 |
| coverage                   | 107 ms                                                       | 118 ms: 1.10x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.5 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (52): 2to3, regex_compile, create_gc_cycles, sqlglot_transpile, sqlglot_parse, logging_format, unpickle, pidigits, richards, float, asyncio_websockets, asyncio_tcp, fannkuch, raytrace, generators, python_startup_no_site, logging_silent, go, sympy_expand, pprint_safe_repr, docutils, sympy_sum, python_startup, asyncio_tcp_ssl, pyflate, dask, pickle_dict, django_template, xml_etree_parse, nbody, scimark_fft, crypto_pyaes, pprint_pformat, regex_dna, thrift, html5lib, regex_effbot, pylint, bench_mp_pool, genshi_xml, async_generators, mako, coroutines, bench_thread_pool, pickle, json, sqlglot_normalize, pickle_pure_python, sqlite_synth, sqlglot_optimize, typing_runtime_protocols, nqueens
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x