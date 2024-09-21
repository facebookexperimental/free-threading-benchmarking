# Results vs. 3.13.0rc2

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.01x slower
- HPT reliability: 78.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 4.14 sec: 1.03x slower                                                |
| Geometric mean | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none  | 572 ms                                                       | 501 ms: 1.14x faster                                                  |
| async_tree_io_tg | 1.40 sec                                                     | 1.30 sec: 1.08x faster                                                |
| async_tree_io    | 1.39 sec                                                     | 1.29 sec: 1.08x faster                                                |
| coroutines       | 30.9 ms                                                      | 32.6 ms: 1.06x slower                                                 |
| Geometric mean   | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (9): async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, asyncio_tcp, async_tree_memoization, asyncio_websockets, asyncio_tcp_ssl, async_generators

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): pidigits, nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 192 ms: 1.06x slower                                                  |
| regex_dna      | 282 ms                                                       | 300 ms: 1.06x slower                                                  |
| regex_effbot   | 4.74 ms                                                      | 5.47 ms: 1.16x slower                                                 |
| regex_v8       | 32.8 ms                                                      | 38.1 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|--------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads        | 2.78 sec                                                     | 2.66 sec: 1.04x faster                                                |
| pickle_pure_python | 416 us                                                       | 436 us: 1.05x slower                                                  |
| json_loads         | 34.3 us                                                      | 37.5 us: 1.09x slower                                                 |
| Geometric mean     | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (11): xml_etree_iterparse, xml_etree_parse, pickle_dict, pickle_list, xml_etree_generate, xml_etree_process, unpickle_pure_python, pickle, unpickle_list, json_dumps, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 23.8 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 44.3 ms                                                      | 48.3 ms: 1.09x slower                                                 |
| mako            | 15.9 ms                                                      | 18.3 ms: 1.15x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|--------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deepcopy           | 498 us                                                       | 359 us: 1.39x faster                                                  |
| deepcopy_memo      | 50.1 us                                                      | 40.2 us: 1.25x faster                                                 |
| unpack_sequence    | 74.3 ns                                                      | 61.3 ns: 1.21x faster                                                 |
| async_tree_none    | 572 ms                                                       | 501 ms: 1.14x faster                                                  |
| deepcopy_reduce    | 4.10 us                                                      | 3.63 us: 1.13x faster                                                 |
| async_tree_io_tg   | 1.40 sec                                                     | 1.30 sec: 1.08x faster                                                |
| async_tree_io      | 1.39 sec                                                     | 1.29 sec: 1.08x faster                                                |
| meteor_contest     | 150 ms                                                       | 139 ms: 1.08x faster                                                  |
| sympy_integrate    | 30.2 ms                                                      | 28.1 ms: 1.08x faster                                                 |
| nqueens            | 112 ms                                                       | 105 ms: 1.06x faster                                                  |
| telco              | 12.2 ms                                                      | 11.5 ms: 1.06x faster                                                 |
| scimark_sor        | 179 ms                                                       | 171 ms: 1.05x faster                                                  |
| tomli_loads        | 2.78 sec                                                     | 2.66 sec: 1.04x faster                                                |
| bpe_tokeniser      | 6.28 sec                                                     | 6.08 sec: 1.03x faster                                                |
| mdp                | 3.80 sec                                                     | 3.71 sec: 1.02x faster                                                |
| docutils           | 4.01 sec                                                     | 4.14 sec: 1.03x slower                                                |
| crypto_pyaes       | 100 ms                                                       | 105 ms: 1.04x slower                                                  |
| sqlglot_normalize  | 140 ms                                                       | 146 ms: 1.05x slower                                                  |
| pickle_pure_python | 416 us                                                       | 436 us: 1.05x slower                                                  |
| hexiom             | 8.11 ms                                                      | 8.52 ms: 1.05x slower                                                 |
| regex_compile      | 182 ms                                                       | 192 ms: 1.06x slower                                                  |
| coroutines         | 30.9 ms                                                      | 32.6 ms: 1.06x slower                                                 |
| regex_dna          | 282 ms                                                       | 300 ms: 1.06x slower                                                  |
| python_startup     | 22.4 ms                                                      | 23.8 ms: 1.06x slower                                                 |
| pycparser          | 1.57 sec                                                     | 1.67 sec: 1.07x slower                                                |
| logging_silent     | 130 ns                                                       | 139 ns: 1.07x slower                                                  |
| sqlglot_parse      | 1.76 ms                                                      | 1.89 ms: 1.08x slower                                                 |
| scimark_lu         | 146 ms                                                       | 158 ms: 1.08x slower                                                  |
| sympy_sum          | 210 ms                                                       | 226 ms: 1.08x slower                                                  |
| comprehensions     | 22.2 us                                                      | 24.0 us: 1.08x slower                                                 |
| sqlglot_transpile  | 2.20 ms                                                      | 2.37 ms: 1.08x slower                                                 |
| django_template    | 44.3 ms                                                      | 48.3 ms: 1.09x slower                                                 |
| coverage           | 107 ms                                                       | 117 ms: 1.09x slower                                                  |
| json_loads         | 34.3 us                                                      | 37.5 us: 1.09x slower                                                 |
| logging_format     | 9.24 us                                                      | 10.2 us: 1.11x slower                                                 |
| sqlglot_optimize   | 74.7 ms                                                      | 83.9 ms: 1.12x slower                                                 |
| bench_mp_pool      | 18.7 ms                                                      | 21.4 ms: 1.14x slower                                                 |
| mako               | 15.9 ms                                                      | 18.3 ms: 1.15x slower                                                 |
| regex_effbot       | 4.74 ms                                                      | 5.47 ms: 1.16x slower                                                 |
| regex_v8           | 32.8 ms                                                      | 38.1 ms: 1.16x slower                                                 |
| bench_thread_pool  | 2.89 ms                                                      | 3.44 ms: 1.19x slower                                                 |
| Geometric mean     | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (55): xml_etree_iterparse, async_tree_none_tg, async_tree_cpu_io_mixed, typing_runtime_protocols, async_tree_memoization_tg, python_startup_no_site, async_tree_cpu_io_mixed_tg, scimark_sparse_mat_mult, fannkuch, pidigits, xml_etree_parse, pickle_dict, gc_traversal, pickle_list, sympy_str, scimark_monte_carlo, logging_simple, raytrace, asyncio_tcp, pathlib, async_tree_memoization, pprint_pformat, deltablue, create_gc_cycles, genshi_xml, asyncio_websockets, asyncio_tcp_ssl, spectral_norm, scimark_fft, 2to3, pprint_safe_repr, sympy_expand, xml_etree_generate, genshi_text, xml_etree_process, pylint, unpickle_pure_python, pickle, nbody, html5lib, async_generators, unpickle_list, pyflate, sqlite_synth, float, json_dumps, tornado_http, go, generators, json, richards_super, thrift, chaos, richards, unpickle
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 78.50% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x