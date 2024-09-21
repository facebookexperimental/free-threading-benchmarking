# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d343f97
- commit date: 2024-09-06
- overall geometric mean: 1.01x faster
- HPT reliability: 62.90%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| docutils       | 4.00 sec                                               | 4.12 sec: 1.03x slower                                |
| Geometric mean | (ref)                                                  | 1.01x slower                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 741 ms                                                 | 502 ms: 1.48x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 686 ms: 1.42x faster                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 667 ms: 1.39x faster                                  |
| async_tree_io_tg           | 1.93 sec                                               | 1.39 sec: 1.39x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 519 ms: 1.36x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.39 sec: 1.33x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 887 ms: 1.24x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 888 ms: 1.21x faster                                  |
| coroutines                 | 29.5 ms                                                | 30.8 ms: 1.04x slower                                 |
| asyncio_websockets         | 748 ms                                                 | 786 ms: 1.05x slower                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.99 sec: 1.06x slower                                |
| asyncio_tcp                | 923 ms                                                 | 992 ms: 1.08x slower                                  |
| Geometric mean             | (ref)                                                  | 1.18x faster                                          |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 297 ms: 1.07x slower                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                          |

Benchmark hidden because not significant (3): regex_effbot, regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict    | 52.7 us                                                | 49.2 us: 1.07x faster                                 |
| unpickle       | 21.2 us                                                | 19.9 us: 1.07x faster                                 |
| unpickle_list  | 6.83 us                                                | 7.33 us: 1.07x slower                                 |
| pickle_list    | 6.97 us                                                | 7.57 us: 1.09x slower                                 |
| json_loads     | 37.9 us                                                | 41.2 us: 1.09x slower                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                          |

Benchmark hidden because not significant (9): xml_etree_parse, unpickle_pure_python, tomli_loads, xml_etree_generate, xml_etree_process, xml_etree_iterparse, json_dumps, pickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup | 23.7 ms                                                | 25.6 ms: 1.08x slower                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 44.9 ms                                                | 48.4 ms: 1.08x slower                                 |
| genshi_xml      | 67.6 ms                                                | 76.1 ms: 1.13x slower                                 |
| genshi_text     | 30.2 ms                                                | 34.1 ms: 1.13x slower                                 |
| mako            | 15.7 ms                                                | 19.0 ms: 1.21x slower                                 |
| Geometric mean  | (ref)                                                  | 1.13x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-main-3.14.0a0-d343f97 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_none            | 741 ms                                                 | 502 ms: 1.48x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 686 ms: 1.42x faster                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 667 ms: 1.39x faster                                  |
| async_tree_io_tg           | 1.93 sec                                               | 1.39 sec: 1.39x faster                                |
| deepcopy                   | 468 us                                                 | 341 us: 1.37x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 519 ms: 1.36x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.39 sec: 1.33x faster                                |
| deepcopy_memo              | 52.4 us                                                | 39.8 us: 1.32x faster                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 887 ms: 1.24x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 888 ms: 1.21x faster                                  |
| comprehensions             | 27.1 us                                                | 23.0 us: 1.18x faster                                 |
| crypto_pyaes               | 107 ms                                                 | 93.8 ms: 1.14x faster                                 |
| raytrace                   | 408 ms                                                 | 361 ms: 1.13x faster                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.61 us: 1.12x faster                                 |
| logging_simple             | 9.45 us                                                | 8.80 us: 1.07x faster                                 |
| pycparser                  | 1.79 sec                                               | 1.67 sec: 1.07x faster                                |
| pickle_dict                | 52.7 us                                                | 49.2 us: 1.07x faster                                 |
| unpickle                   | 21.2 us                                                | 19.9 us: 1.07x faster                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.21 ms: 1.06x faster                                 |
| pyflate                    | 727 ms                                                 | 690 ms: 1.05x faster                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 91.7 ms: 1.05x faster                                 |
| mdp                        | 3.97 sec                                               | 4.09 sec: 1.03x slower                                |
| docutils                   | 4.00 sec                                               | 4.12 sec: 1.03x slower                                |
| pprint_safe_repr           | 967 ms                                                 | 1.01 sec: 1.04x slower                                |
| coroutines                 | 29.5 ms                                                | 30.8 ms: 1.04x slower                                 |
| richards                   | 60.3 ms                                                | 63.3 ms: 1.05x slower                                 |
| asyncio_websockets         | 748 ms                                                 | 786 ms: 1.05x slower                                  |
| json                       | 6.85 ms                                                | 7.28 ms: 1.06x slower                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.99 sec: 1.06x slower                                |
| regex_dna                  | 278 ms                                                 | 297 ms: 1.07x slower                                  |
| deltablue                  | 4.27 ms                                                | 4.57 ms: 1.07x slower                                 |
| sympy_expand               | 582 ms                                                 | 623 ms: 1.07x slower                                  |
| unpickle_list              | 6.83 us                                                | 7.33 us: 1.07x slower                                 |
| asyncio_tcp                | 923 ms                                                 | 992 ms: 1.08x slower                                  |
| django_template            | 44.9 ms                                                | 48.4 ms: 1.08x slower                                 |
| python_startup             | 23.7 ms                                                | 25.6 ms: 1.08x slower                                 |
| gc_traversal               | 5.86 ms                                                | 6.35 ms: 1.08x slower                                 |
| pickle_list                | 6.97 us                                                | 7.57 us: 1.09x slower                                 |
| json_loads                 | 37.9 us                                                | 41.2 us: 1.09x slower                                 |
| bench_mp_pool              | 20.7 ms                                                | 22.8 ms: 1.10x slower                                 |
| bench_thread_pool          | 3.48 ms                                                | 3.86 ms: 1.11x slower                                 |
| logging_format             | 9.59 us                                                | 10.7 us: 1.12x slower                                 |
| genshi_xml                 | 67.6 ms                                                | 76.1 ms: 1.13x slower                                 |
| genshi_text                | 30.2 ms                                                | 34.1 ms: 1.13x slower                                 |
| sqlglot_parse              | 1.79 ms                                                | 2.03 ms: 1.14x slower                                 |
| mako                       | 15.7 ms                                                | 19.0 ms: 1.21x slower                                 |
| coverage                   | 95.4 ms                                                | 117 ms: 1.23x slower                                  |
| telco                      | 9.59 ms                                                | 11.9 ms: 1.24x slower                                 |
| create_gc_cycles           | 1.94 ms                                                | 2.70 ms: 1.39x slower                                 |
| Geometric mean             | (ref)                                                  | 1.01x faster                                          |

Benchmark hidden because not significant (48): sqlglot_normalize, pathlib, regex_effbot, xml_etree_parse, sympy_str, float, chaos, 2to3, unpickle_pure_python, tomli_loads, xml_etree_generate, typing_runtime_protocols, bpe_tokeniser, pidigits, regex_v8, xml_etree_process, go, nqueens, async_generators, scimark_fft, sqlglot_optimize, sympy_integrate, pprint_pformat, xml_etree_iterparse, html5lib, sympy_sum, dulwich_log, json_dumps, richards_super, generators, python_startup_no_site, tornado_http, pickle, fannkuch, thrift, nbody, scimark_lu, spectral_norm, regex_compile, unpack_sequence, scimark_sparse_mat_mult, hexiom, sqlite_synth, meteor_contest, scimark_sor, logging_silent, pickle_pure_python, pylint
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 62.90% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x