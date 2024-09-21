# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e913d2c
- commit date: 2024-08-15
- overall geometric mean: 1.00x slower
- HPT reliability: 87.06%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 422 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                          |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none        | 572 ms                                                       | 508 ms: 1.12x faster                                  |
| async_tree_io_tg       | 1.40 sec                                                     | 1.27 sec: 1.10x faster                                |
| async_tree_none_tg     | 504 ms                                                       | 466 ms: 1.08x faster                                  |
| async_tree_io          | 1.39 sec                                                     | 1.29 sec: 1.08x faster                                |
| async_tree_memoization | 709 ms                                                       | 670 ms: 1.06x faster                                  |
| asyncio_websockets     | 766 ms                                                       | 734 ms: 1.04x faster                                  |
| Geometric mean         | (ref)                                                        | 1.04x faster                                          |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_generators, coroutines, asyncio_tcp, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 292 ms: 1.04x slower                                  |
| regex_v8       | 32.8 ms                                                      | 35.4 ms: 1.08x slower                                 |
| regex_effbot   | 4.74 ms                                                      | 5.30 ms: 1.12x slower                                 |
| Geometric mean | (ref)                                                        | 1.05x slower                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 166 ms: 1.07x faster                                  |
| unpickle_pure_python | 290 us                                                       | 275 us: 1.06x faster                                  |
| json_loads           | 34.3 us                                                      | 37.6 us: 1.10x slower                                 |
| json_dumps           | 14.1 ms                                                      | 15.7 ms: 1.11x slower                                 |
| unpickle_list        | 6.68 us                                                      | 7.68 us: 1.15x slower                                 |
| Geometric mean       | (ref)                                                        | 1.02x slower                                          |

Benchmark hidden because not significant (9): tomli_loads, xml_etree_parse, xml_etree_generate, pickle_list, unpickle, xml_etree_process, pickle_dict, pickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 44.3 ms                                                      | 47.1 ms: 1.06x slower                                 |
| mako            | 15.9 ms                                                      | 17.0 ms: 1.07x slower                                 |
| Geometric mean  | (ref)                                                        | 1.04x slower                                          |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| deepcopy               | 498 us                                                       | 383 us: 1.30x faster                                  |
| deepcopy_memo          | 50.1 us                                                      | 39.8 us: 1.26x faster                                 |
| async_tree_none        | 572 ms                                                       | 508 ms: 1.12x faster                                  |
| unpack_sequence        | 74.3 ns                                                      | 66.6 ns: 1.12x faster                                 |
| sympy_integrate        | 30.2 ms                                                      | 27.3 ms: 1.11x faster                                 |
| async_tree_io_tg       | 1.40 sec                                                     | 1.27 sec: 1.10x faster                                |
| telco                  | 12.2 ms                                                      | 11.2 ms: 1.09x faster                                 |
| async_tree_none_tg     | 504 ms                                                       | 466 ms: 1.08x faster                                  |
| async_tree_io          | 1.39 sec                                                     | 1.29 sec: 1.08x faster                                |
| deepcopy_reduce        | 4.10 us                                                      | 3.83 us: 1.07x faster                                 |
| pathlib                | 29.9 ms                                                      | 28.0 ms: 1.07x faster                                 |
| xml_etree_iterparse    | 177 ms                                                       | 166 ms: 1.07x faster                                  |
| async_tree_memoization | 709 ms                                                       | 670 ms: 1.06x faster                                  |
| scimark_sor            | 179 ms                                                       | 169 ms: 1.06x faster                                  |
| unpickle_pure_python   | 290 us                                                       | 275 us: 1.06x faster                                  |
| 2to3                   | 445 ms                                                       | 422 ms: 1.06x faster                                  |
| raytrace               | 344 ms                                                       | 328 ms: 1.05x faster                                  |
| sqlite_synth           | 3.99 us                                                      | 3.80 us: 1.05x faster                                 |
| asyncio_websockets     | 766 ms                                                       | 734 ms: 1.04x faster                                  |
| sqlglot_optimize       | 74.7 ms                                                      | 71.7 ms: 1.04x faster                                 |
| pprint_safe_repr       | 987 ms                                                       | 957 ms: 1.03x faster                                  |
| mdp                    | 3.80 sec                                                     | 3.71 sec: 1.02x faster                                |
| regex_dna              | 282 ms                                                       | 292 ms: 1.04x slower                                  |
| hexiom                 | 8.11 ms                                                      | 8.52 ms: 1.05x slower                                 |
| sqlglot_normalize      | 140 ms                                                       | 147 ms: 1.05x slower                                  |
| crypto_pyaes           | 100 ms                                                       | 106 ms: 1.06x slower                                  |
| pycparser              | 1.57 sec                                                     | 1.67 sec: 1.06x slower                                |
| django_template        | 44.3 ms                                                      | 47.1 ms: 1.06x slower                                 |
| mako                   | 15.9 ms                                                      | 17.0 ms: 1.07x slower                                 |
| scimark_fft            | 473 ms                                                       | 510 ms: 1.08x slower                                  |
| regex_v8               | 32.8 ms                                                      | 35.4 ms: 1.08x slower                                 |
| thrift                 | 1.10 ms                                                      | 1.19 ms: 1.08x slower                                 |
| coverage               | 107 ms                                                       | 117 ms: 1.09x slower                                  |
| sympy_sum              | 210 ms                                                       | 230 ms: 1.09x slower                                  |
| json_loads             | 34.3 us                                                      | 37.6 us: 1.10x slower                                 |
| json_dumps             | 14.1 ms                                                      | 15.7 ms: 1.11x slower                                 |
| regex_effbot           | 4.74 ms                                                      | 5.30 ms: 1.12x slower                                 |
| unpickle_list          | 6.68 us                                                      | 7.68 us: 1.15x slower                                 |
| json                   | 6.51 ms                                                      | 7.54 ms: 1.16x slower                                 |
| bench_thread_pool      | 2.89 ms                                                      | 3.58 ms: 1.24x slower                                 |
| Geometric mean         | (ref)                                                        | 1.00x slower                                          |

Benchmark hidden because not significant (56): tornado_http, regex_compile, async_tree_cpu_io_mixed, richards, async_tree_memoization_tg, fannkuch, richards_super, logging_simple, sympy_str, chaos, nbody, scimark_sparse_mat_mult, scimark_monte_carlo, tomli_loads, xml_etree_parse, xml_etree_generate, pickle_list, spectral_norm, async_tree_cpu_io_mixed_tg, unpickle, deltablue, genshi_xml, meteor_contest, gc_traversal, bpe_tokeniser, docutils, python_startup_no_site, xml_etree_process, comprehensions, python_startup, pidigits, pickle_dict, pprint_pformat, async_generators, coroutines, html5lib, asyncio_tcp, pyflate, sqlglot_transpile, asyncio_tcp_ssl, genshi_text, generators, go, pylint, sqlglot_parse, logging_format, typing_runtime_protocols, sympy_expand, pickle, nqueens, scimark_lu, create_gc_cycles, pickle_pure_python, logging_silent, float, bench_mp_pool
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 87.06% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x