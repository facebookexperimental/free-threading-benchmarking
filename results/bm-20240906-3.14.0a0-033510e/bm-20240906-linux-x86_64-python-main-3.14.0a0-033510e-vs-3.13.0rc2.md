# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 033510e
- commit date: 2024-09-06
- overall geometric mean: 1.01x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 415 ms: 1.07x faster                                  |
| docutils       | 4.01 sec                                                     | 3.82 sec: 1.05x faster                                |
| html5lib       | 92.6 ms                                                      | 88.4 ms: 1.05x faster                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|---------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none           | 572 ms                                                       | 501 ms: 1.14x faster                                  |
| async_tree_memoization    | 709 ms                                                       | 637 ms: 1.11x faster                                  |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 823 ms: 1.08x faster                                  |
| async_tree_memoization_tg | 670 ms                                                       | 621 ms: 1.08x faster                                  |
| async_tree_io_tg          | 1.40 sec                                                     | 1.32 sec: 1.06x faster                                |
| asyncio_tcp               | 948 ms                                                       | 901 ms: 1.05x faster                                  |
| async_tree_none_tg        | 504 ms                                                       | 483 ms: 1.04x faster                                  |
| Geometric mean            | (ref)                                                        | 1.04x faster                                          |

Benchmark hidden because not significant (6): asyncio_websockets, async_tree_io, asyncio_tcp_ssl, async_tree_cpu_io_mixed_tg, async_generators, coroutines

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 34.9 ms: 1.06x slower                                 |
| regex_effbot   | 4.74 ms                                                      | 5.19 ms: 1.10x slower                                 |
| Geometric mean | (ref)                                                        | 1.04x slower                                          |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|---------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 167 ms: 1.06x faster                                  |
| pickle_dict         | 47.2 us                                                      | 44.6 us: 1.06x faster                                 |
| unpickle_list       | 6.68 us                                                      | 7.20 us: 1.08x slower                                 |
| pickle              | 15.1 us                                                      | 16.5 us: 1.09x slower                                 |
| json_loads          | 34.3 us                                                      | 37.9 us: 1.11x slower                                 |
| json_dumps          | 14.1 ms                                                      | 15.8 ms: 1.12x slower                                 |
| Geometric mean      | (ref)                                                        | 1.02x slower                                          |

Benchmark hidden because not significant (8): xml_etree_generate, tomli_loads, unpickle_pure_python, xml_etree_process, xml_etree_parse, unpickle, pickle_list, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 21.6 ms: 1.04x faster                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text    | 31.7 ms                                                      | 33.6 ms: 1.06x slower                                 |
| mako           | 15.9 ms                                                      | 18.2 ms: 1.14x slower                                 |
| Geometric mean | (ref)                                                        | 1.05x slower                                          |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-main-3.14.0a0-033510e |
|---------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| unpack_sequence           | 74.3 ns                                                      | 51.6 ns: 1.44x faster                                 |
| deepcopy                  | 498 us                                                       | 354 us: 1.41x faster                                  |
| go                        | 191 ms                                                       | 161 ms: 1.19x faster                                  |
| deepcopy_memo             | 50.1 us                                                      | 43.0 us: 1.16x faster                                 |
| async_tree_none           | 572 ms                                                       | 501 ms: 1.14x faster                                  |
| deepcopy_reduce           | 4.10 us                                                      | 3.62 us: 1.13x faster                                 |
| sympy_integrate           | 30.2 ms                                                      | 27.0 ms: 1.12x faster                                 |
| scimark_sparse_mat_mult   | 6.76 ms                                                      | 6.07 ms: 1.11x faster                                 |
| async_tree_memoization    | 709 ms                                                       | 637 ms: 1.11x faster                                  |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 823 ms: 1.08x faster                                  |
| async_tree_memoization_tg | 670 ms                                                       | 621 ms: 1.08x faster                                  |
| pprint_safe_repr          | 987 ms                                                       | 916 ms: 1.08x faster                                  |
| spectral_norm             | 157 ms                                                       | 146 ms: 1.08x faster                                  |
| telco                     | 12.2 ms                                                      | 11.3 ms: 1.07x faster                                 |
| 2to3                      | 445 ms                                                       | 415 ms: 1.07x faster                                  |
| async_tree_io_tg          | 1.40 sec                                                     | 1.32 sec: 1.06x faster                                |
| xml_etree_iterparse       | 177 ms                                                       | 167 ms: 1.06x faster                                  |
| pickle_dict               | 47.2 us                                                      | 44.6 us: 1.06x faster                                 |
| scimark_sor               | 179 ms                                                       | 169 ms: 1.06x faster                                  |
| sympy_str                 | 379 ms                                                       | 358 ms: 1.06x faster                                  |
| scimark_monte_carlo       | 90.6 ms                                                      | 85.8 ms: 1.06x faster                                 |
| thrift                    | 1.10 ms                                                      | 1.05 ms: 1.05x faster                                 |
| asyncio_tcp               | 948 ms                                                       | 901 ms: 1.05x faster                                  |
| docutils                  | 4.01 sec                                                     | 3.82 sec: 1.05x faster                                |
| html5lib                  | 92.6 ms                                                      | 88.4 ms: 1.05x faster                                 |
| async_tree_none_tg        | 504 ms                                                       | 483 ms: 1.04x faster                                  |
| python_startup            | 22.4 ms                                                      | 21.6 ms: 1.04x faster                                 |
| bpe_tokeniser             | 6.28 sec                                                     | 6.12 sec: 1.03x faster                                |
| mdp                       | 3.80 sec                                                     | 3.99 sec: 1.05x slower                                |
| scimark_lu                | 146 ms                                                       | 154 ms: 1.05x slower                                  |
| json                      | 6.51 ms                                                      | 6.88 ms: 1.06x slower                                 |
| genshi_text               | 31.7 ms                                                      | 33.6 ms: 1.06x slower                                 |
| logging_format            | 9.24 us                                                      | 9.82 us: 1.06x slower                                 |
| regex_v8                  | 32.8 ms                                                      | 34.9 ms: 1.06x slower                                 |
| unpickle_list             | 6.68 us                                                      | 7.20 us: 1.08x slower                                 |
| bench_mp_pool             | 18.7 ms                                                      | 20.4 ms: 1.09x slower                                 |
| generators                | 40.0 ms                                                      | 43.6 ms: 1.09x slower                                 |
| pickle                    | 15.1 us                                                      | 16.5 us: 1.09x slower                                 |
| logging_simple            | 8.56 us                                                      | 9.36 us: 1.09x slower                                 |
| regex_effbot              | 4.74 ms                                                      | 5.19 ms: 1.10x slower                                 |
| json_loads                | 34.3 us                                                      | 37.9 us: 1.11x slower                                 |
| bench_thread_pool         | 2.89 ms                                                      | 3.22 ms: 1.11x slower                                 |
| json_dumps                | 14.1 ms                                                      | 15.8 ms: 1.12x slower                                 |
| mako                      | 15.9 ms                                                      | 18.2 ms: 1.14x slower                                 |
| dulwich_log               | 93.7 ms                                                      | 123 ms: 1.31x slower                                  |
| Geometric mean            | (ref)                                                        | 1.01x faster                                          |

Benchmark hidden because not significant (52): regex_compile, sqlglot_parse, genshi_xml, xml_etree_generate, sqlite_synth, sqlglot_optimize, sqlglot_transpile, pprint_pformat, create_gc_cycles, nbody, richards_super, asyncio_websockets, tornado_http, async_tree_io, fannkuch, pycparser, python_startup_no_site, crypto_pyaes, asyncio_tcp_ssl, gc_traversal, scimark_fft, sympy_sum, meteor_contest, typing_runtime_protocols, raytrace, tomli_loads, float, comprehensions, unpickle_pure_python, richards, pathlib, chaos, hexiom, coverage, async_tree_cpu_io_mixed_tg, sqlglot_normalize, sympy_expand, xml_etree_process, xml_etree_parse, unpickle, pickle_list, async_generators, pidigits, logging_silent, pylint, pyflate, nqueens, regex_dna, deltablue, django_template, coroutines, pickle_pure_python
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x