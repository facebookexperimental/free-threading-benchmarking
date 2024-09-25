# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e913d2c
- commit date: 2024-08-15
- overall geometric mean: 1.05x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_memoization    | 775 ms                                                                | 670 ms: 1.16x faster                                  |
| async_tree_none_tg        | 526 ms                                                                | 466 ms: 1.13x faster                                  |
| async_tree_io_tg          | 1.43 sec                                                              | 1.27 sec: 1.13x faster                                |
| async_tree_io             | 1.39 sec                                                              | 1.29 sec: 1.08x faster                                |
| async_tree_memoization_tg | 692 ms                                                                | 650 ms: 1.06x faster                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 857 ms: 1.05x faster                                  |
| coroutines                | 29.3 ms                                                               | 31.3 ms: 1.07x slower                                 |
| Geometric mean            | (ref)                                                                 | 1.05x faster                                          |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed_tg, async_tree_none, async_generators, asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| nbody          | 126 ms                                                                | 116 ms: 1.08x faster                                  |
| Geometric mean | (ref)                                                                 | 1.01x faster                                          |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 189 ms                                                                | 175 ms: 1.08x faster                                  |
| regex_dna      | 284 ms                                                                | 292 ms: 1.03x slower                                  |
| regex_effbot   | 4.63 ms                                                               | 5.30 ms: 1.14x slower                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.78 us: 1.10x faster                                 |
| unpickle             | 22.2 us                                                               | 20.4 us: 1.09x faster                                 |
| tomli_loads          | 2.84 sec                                                              | 2.73 sec: 1.04x faster                                |
| unpickle_pure_python | 285 us                                                                | 275 us: 1.04x faster                                  |
| xml_etree_process    | 82.2 ms                                                               | 86.3 ms: 1.05x slower                                 |
| xml_etree_parse      | 216 ms                                                                | 227 ms: 1.05x slower                                  |
| json_dumps           | 13.9 ms                                                               | 15.7 ms: 1.13x slower                                 |
| unpickle_list        | 6.78 us                                                               | 7.68 us: 1.13x slower                                 |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                          |

Benchmark hidden because not significant (6): json_loads, xml_etree_generate, pickle_pure_python, xml_etree_iterparse, pickle_dict, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 22.6 ms: 1.04x faster                                 |
| python_startup_no_site | 16.0 ms                                                               | 15.4 ms: 1.04x faster                                 |
| Geometric mean         | (ref)                                                                 | 1.04x faster                                          |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_xml, django_template, mako, genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                     | 229 ms                                                                | 11.2 ms: 20.45x faster                                |
| deepcopy                  | 498 us                                                                | 383 us: 1.30x faster                                  |
| deepcopy_memo             | 50.9 us                                                               | 39.8 us: 1.28x faster                                 |
| async_tree_memoization    | 775 ms                                                                | 670 ms: 1.16x faster                                  |
| pathlib                   | 31.8 ms                                                               | 28.0 ms: 1.14x faster                                 |
| async_tree_none_tg        | 526 ms                                                                | 466 ms: 1.13x faster                                  |
| deepcopy_reduce           | 4.31 us                                                               | 3.83 us: 1.13x faster                                 |
| async_tree_io_tg          | 1.43 sec                                                              | 1.27 sec: 1.13x faster                                |
| pickle_list               | 7.48 us                                                               | 6.78 us: 1.10x faster                                 |
| logging_simple            | 9.16 us                                                               | 8.33 us: 1.10x faster                                 |
| unpickle                  | 22.2 us                                                               | 20.4 us: 1.09x faster                                 |
| sqlglot_optimize          | 77.9 ms                                                               | 71.7 ms: 1.09x faster                                 |
| richards                  | 68.8 ms                                                               | 63.5 ms: 1.08x faster                                 |
| nbody                     | 126 ms                                                                | 116 ms: 1.08x faster                                  |
| async_tree_io             | 1.39 sec                                                              | 1.29 sec: 1.08x faster                                |
| mdp                       | 4.01 sec                                                              | 3.71 sec: 1.08x faster                                |
| regex_compile             | 189 ms                                                                | 175 ms: 1.08x faster                                  |
| raytrace                  | 351 ms                                                                | 328 ms: 1.07x faster                                  |
| async_tree_memoization_tg | 692 ms                                                                | 650 ms: 1.06x faster                                  |
| sqlglot_parse             | 1.92 ms                                                               | 1.81 ms: 1.06x faster                                 |
| pyflate                   | 710 ms                                                                | 674 ms: 1.05x faster                                  |
| sympy_integrate           | 28.7 ms                                                               | 27.3 ms: 1.05x faster                                 |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 857 ms: 1.05x faster                                  |
| scimark_sor               | 176 ms                                                                | 169 ms: 1.04x faster                                  |
| python_startup            | 23.5 ms                                                               | 22.6 ms: 1.04x faster                                 |
| tomli_loads               | 2.84 sec                                                              | 2.73 sec: 1.04x faster                                |
| python_startup_no_site    | 16.0 ms                                                               | 15.4 ms: 1.04x faster                                 |
| unpickle_pure_python      | 285 us                                                                | 275 us: 1.04x faster                                  |
| pprint_pformat            | 2.04 sec                                                              | 1.96 sec: 1.04x faster                                |
| pprint_safe_repr          | 991 ms                                                                | 957 ms: 1.04x faster                                  |
| bpe_tokeniser             | 6.53 sec                                                              | 6.31 sec: 1.04x faster                                |
| regex_dna                 | 284 ms                                                                | 292 ms: 1.03x slower                                  |
| crypto_pyaes              | 102 ms                                                                | 106 ms: 1.04x slower                                  |
| xml_etree_process         | 82.2 ms                                                               | 86.3 ms: 1.05x slower                                 |
| xml_etree_parse           | 216 ms                                                                | 227 ms: 1.05x slower                                  |
| coroutines                | 29.3 ms                                                               | 31.3 ms: 1.07x slower                                 |
| nqueens                   | 108 ms                                                                | 116 ms: 1.07x slower                                  |
| scimark_fft               | 469 ms                                                                | 510 ms: 1.09x slower                                  |
| thrift                    | 1.09 ms                                                               | 1.19 ms: 1.10x slower                                 |
| json                      | 6.79 ms                                                               | 7.54 ms: 1.11x slower                                 |
| json_dumps                | 13.9 ms                                                               | 15.7 ms: 1.13x slower                                 |
| unpickle_list             | 6.78 us                                                               | 7.68 us: 1.13x slower                                 |
| regex_effbot              | 4.63 ms                                                               | 5.30 ms: 1.14x slower                                 |
| bench_thread_pool         | 3.01 ms                                                               | 3.58 ms: 1.19x slower                                 |
| unpack_sequence           | 54.6 ns                                                               | 66.6 ns: 1.22x slower                                 |
| Geometric mean            | (ref)                                                                 | 1.05x faster                                          |

Benchmark hidden because not significant (51): tornado_http, regex_v8, 2to3, meteor_contest, async_tree_cpu_io_mixed_tg, scimark_sparse_mat_mult, sqlite_synth, coverage, richards_super, deltablue, async_tree_none, sympy_expand, async_generators, pycparser, sqlglot_normalize, gc_traversal, sympy_str, comprehensions, asyncio_tcp, logging_silent, pidigits, fannkuch, json_loads, scimark_monte_carlo, sqlglot_transpile, genshi_xml, asyncio_tcp_ssl, chaos, generators, xml_etree_generate, bench_mp_pool, asyncio_websockets, create_gc_cycles, hexiom, go, pickle_pure_python, scimark_lu, sympy_sum, logging_format, xml_etree_iterparse, html5lib, django_template, docutils, mako, genshi_text, pickle_dict, spectral_norm, pickle, pylint, typing_runtime_protocols, float
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x