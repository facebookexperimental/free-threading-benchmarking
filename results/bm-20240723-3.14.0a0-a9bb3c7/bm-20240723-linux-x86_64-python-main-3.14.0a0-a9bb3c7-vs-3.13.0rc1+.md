# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 410 ms: 1.08x faster                                  |
| html5lib       | 98.1 ms                                                 | 88.8 ms: 1.10x faster                                 |
| Geometric mean | (ref)                                                   | 1.05x faster                                          |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|---------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg          | 1.46 sec                                                | 1.24 sec: 1.17x faster                                |
| async_tree_memoization_tg | 672 ms                                                  | 584 ms: 1.15x faster                                  |
| async_tree_none_tg        | 521 ms                                                  | 464 ms: 1.12x faster                                  |
| async_tree_memoization    | 745 ms                                                  | 671 ms: 1.11x faster                                  |
| async_tree_cpu_io_mixed   | 899 ms                                                  | 821 ms: 1.09x faster                                  |
| async_tree_none           | 576 ms                                                  | 531 ms: 1.09x faster                                  |
| async_tree_io             | 1.38 sec                                                | 1.28 sec: 1.07x faster                                |
| async_generators          | 592 ms                                                  | 570 ms: 1.04x faster                                  |
| Geometric mean            | (ref)                                                   | 1.07x faster                                          |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, asyncio_tcp, asyncio_websockets, asyncio_tcp_ssl, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| nbody          | 124 ms                                                  | 114 ms: 1.09x faster                                  |
| pidigits       | 248 ms                                                  | 240 ms: 1.03x faster                                  |
| Geometric mean | (ref)                                                   | 1.04x faster                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_dna, regex_effbot, regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|---------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_generate  | 129 ms                                                  | 116 ms: 1.11x faster                                  |
| xml_etree_iterparse | 176 ms                                                  | 161 ms: 1.10x faster                                  |
| xml_etree_parse     | 236 ms                                                  | 216 ms: 1.09x faster                                  |
| pickle_list         | 6.82 us                                                 | 6.29 us: 1.08x faster                                 |
| unpickle            | 21.4 us                                                 | 20.1 us: 1.06x faster                                 |
| tomli_loads         | 2.80 sec                                                | 2.68 sec: 1.05x faster                                |
| json_loads          | 36.1 us                                                 | 37.9 us: 1.05x slower                                 |
| Geometric mean      | (ref)                                                   | 1.03x faster                                          |

Benchmark hidden because not significant (7): xml_etree_process, pickle_dict, json_dumps, unpickle_pure_python, pickle_pure_python, unpickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup | 22.0 ms                                                 | 21.4 ms: 1.03x faster                                 |
| Geometric mean | (ref)                                                   | 1.01x faster                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): django_template, genshi_text, genshi_xml, mako

All benchmarks:
===============

| Benchmark                 | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|---------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| deepcopy                  | 484 us                                                  | 361 us: 1.34x faster                                  |
| deepcopy_memo             | 51.7 us                                                 | 38.7 us: 1.34x faster                                 |
| async_tree_io_tg          | 1.46 sec                                                | 1.24 sec: 1.17x faster                                |
| deepcopy_reduce           | 4.27 us                                                 | 3.71 us: 1.15x faster                                 |
| async_tree_memoization_tg | 672 ms                                                  | 584 ms: 1.15x faster                                  |
| async_tree_none_tg        | 521 ms                                                  | 464 ms: 1.12x faster                                  |
| xml_etree_generate        | 129 ms                                                  | 116 ms: 1.11x faster                                  |
| richards_super            | 76.3 ms                                                 | 68.7 ms: 1.11x faster                                 |
| async_tree_memoization    | 745 ms                                                  | 671 ms: 1.11x faster                                  |
| html5lib                  | 98.1 ms                                                 | 88.8 ms: 1.10x faster                                 |
| sqlite_synth              | 4.07 us                                                 | 3.71 us: 1.10x faster                                 |
| xml_etree_iterparse       | 176 ms                                                  | 161 ms: 1.10x faster                                  |
| async_tree_cpu_io_mixed   | 899 ms                                                  | 821 ms: 1.09x faster                                  |
| xml_etree_parse           | 236 ms                                                  | 216 ms: 1.09x faster                                  |
| richards                  | 65.8 ms                                                 | 60.4 ms: 1.09x faster                                 |
| thrift                    | 1.11 ms                                                 | 1.03 ms: 1.09x faster                                 |
| async_tree_none           | 576 ms                                                  | 531 ms: 1.09x faster                                  |
| nbody                     | 124 ms                                                  | 114 ms: 1.09x faster                                  |
| pickle_list               | 6.82 us                                                 | 6.29 us: 1.08x faster                                 |
| create_gc_cycles          | 2.46 ms                                                 | 2.27 ms: 1.08x faster                                 |
| logging_simple            | 8.98 us                                                 | 8.31 us: 1.08x faster                                 |
| sqlglot_transpile         | 2.30 ms                                                 | 2.13 ms: 1.08x faster                                 |
| 2to3                      | 442 ms                                                  | 410 ms: 1.08x faster                                  |
| async_tree_io             | 1.38 sec                                                | 1.28 sec: 1.07x faster                                |
| meteor_contest            | 157 ms                                                  | 146 ms: 1.07x faster                                  |
| unpickle                  | 21.4 us                                                 | 20.1 us: 1.06x faster                                 |
| deltablue                 | 4.56 ms                                                 | 4.31 ms: 1.06x faster                                 |
| mdp                       | 3.80 sec                                                | 3.61 sec: 1.05x faster                                |
| tomli_loads               | 2.80 sec                                                | 2.68 sec: 1.05x faster                                |
| sympy_expand              | 631 ms                                                  | 605 ms: 1.04x faster                                  |
| async_generators          | 592 ms                                                  | 570 ms: 1.04x faster                                  |
| pprint_pformat            | 2.00 sec                                                | 1.92 sec: 1.04x faster                                |
| pidigits                  | 248 ms                                                  | 240 ms: 1.03x faster                                  |
| python_startup            | 22.0 ms                                                 | 21.4 ms: 1.03x faster                                 |
| json_loads                | 36.1 us                                                 | 37.9 us: 1.05x slower                                 |
| unpack_sequence           | 73.9 ns                                                 | 78.4 ns: 1.06x slower                                 |
| bench_thread_pool         | 3.06 ms                                                 | 3.42 ms: 1.12x slower                                 |
| coverage                  | 110 ms                                                  | 126 ms: 1.15x slower                                  |
| json                      | 6.55 ms                                                 | 7.74 ms: 1.18x slower                                 |
| Geometric mean            | (ref)                                                   | 1.03x faster                                          |

Benchmark hidden because not significant (59): scimark_sparse_mat_mult, sqlglot_parse, gc_traversal, dulwich_log, sqlglot_optimize, chaos, async_tree_cpu_io_mixed_tg, django_template, xml_etree_process, raytrace, asyncio_tcp, typing_runtime_protocols, logging_silent, pathlib, pickle_dict, go, telco, asyncio_websockets, generators, sympy_str, docutils, scimark_monte_carlo, genshi_text, sympy_integrate, logging_format, bpe_tokeniser, fannkuch, pprint_safe_repr, regex_dna, nqueens, json_dumps, tornado_http, hexiom, unpickle_pure_python, dask, pycparser, sympy_sum, scimark_lu, scimark_sor, float, scimark_fft, regex_effbot, pickle_pure_python, pylint, python_startup_no_site, pyflate, asyncio_tcp_ssl, regex_v8, comprehensions, crypto_pyaes, unpickle_list, genshi_xml, sqlglot_normalize, regex_compile, coroutines, mako, spectral_norm, pickle, bench_mp_pool
Ignored benchmarks (4) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x