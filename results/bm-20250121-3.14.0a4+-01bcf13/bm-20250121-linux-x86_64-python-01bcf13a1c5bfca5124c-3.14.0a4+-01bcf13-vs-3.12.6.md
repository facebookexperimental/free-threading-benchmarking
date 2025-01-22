# Results vs. 3.12.6

- fork: python
- ref: 01bcf13a1c5bfca5124c
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.048x faster
- HPT reliability: 98.46%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 510 ms: 1.12x slower                                                   |
| docutils       | 4.00 sec                                               | 3.61 sec: 1.11x faster                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 886 ms: 2.18x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 892 ms: 2.07x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 504 ms: 1.94x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 380 ms: 1.85x faster                                                   |
| async_tree_none            | 741 ms                                                 | 400 ms: 1.85x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 545 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 696 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 745 ms: 1.45x faster                                                   |
| async_generators           | 589 ms                                                 | 543 ms: 1.08x faster                                                   |
| coroutines                 | 29.5 ms                                                | 33.3 ms: 1.13x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 115 ms: 1.07x faster                                                   |
| pidigits       | 250 ms                                                 | 275 ms: 1.10x slower                                                   |
| nbody          | 119 ms                                                 | 141 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.39 ms: 1.17x faster                                                  |
| regex_v8       | 32.5 ms                                                | 36.1 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse    | 241 ms                                                 | 209 ms: 1.15x faster                                                   |
| tomli_loads        | 2.88 sec                                               | 2.68 sec: 1.08x faster                                                 |
| pickle_pure_python | 436 us                                                 | 469 us: 1.08x slower                                                   |
| json_loads         | 37.9 us                                                | 42.4 us: 1.12x slower                                                  |
| json_dumps         | 14.3 ms                                                | 19.9 ms: 1.39x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (4): xml_etree_iterparse, unpickle_pure_python, xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 23.7 ms                                                | 30.8 ms: 1.30x slower                                                  |
| Geometric mean | (ref)                                                  | 1.15x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 51.0 ms: 1.14x slower                                                  |
| mako            | 15.7 ms                                                | 18.1 ms: 1.15x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 77.9 ms: 1.15x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.11x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 886 ms: 2.18x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 892 ms: 2.07x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 504 ms: 1.94x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 380 ms: 1.85x faster                                                   |
| async_tree_none            | 741 ms                                                 | 400 ms: 1.85x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 545 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 696 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 745 ms: 1.45x faster                                                   |
| comprehensions             | 27.1 us                                                | 20.3 us: 1.34x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 40.3 us: 1.30x faster                                                  |
| deepcopy                   | 468 us                                                 | 394 us: 1.19x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.39 ms: 1.17x faster                                                  |
| raytrace                   | 408 ms                                                 | 349 ms: 1.17x faster                                                   |
| deepcopy_reduce            | 4.04 us                                                | 3.46 us: 1.17x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 189 ms: 1.15x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 209 ms: 1.15x faster                                                   |
| pylint                     | 465 ms                                                 | 414 ms: 1.12x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 198 ms: 1.12x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.55 sec: 1.12x faster                                                 |
| docutils                   | 4.00 sec                                               | 3.61 sec: 1.11x faster                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 5.96 sec: 1.11x faster                                                 |
| scimark_fft                | 500 ms                                                 | 453 ms: 1.10x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 88.3 ms: 1.09x faster                                                  |
| async_generators           | 589 ms                                                 | 543 ms: 1.08x faster                                                   |
| chaos                      | 84.9 ms                                                | 78.6 ms: 1.08x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 208 us: 1.08x faster                                                   |
| pyflate                    | 727 ms                                                 | 675 ms: 1.08x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.68 sec: 1.08x faster                                                 |
| float                      | 123 ms                                                 | 115 ms: 1.07x faster                                                   |
| scimark_sor                | 167 ms                                                 | 157 ms: 1.06x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.70 sec: 1.05x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 4.06 us: 1.05x slower                                                  |
| json                       | 6.85 ms                                                | 7.18 ms: 1.05x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 469 us: 1.08x slower                                                   |
| richards                   | 60.3 ms                                                | 65.0 ms: 1.08x slower                                                  |
| dulwich_log                | 100 ms                                                 | 110 ms: 1.09x slower                                                   |
| fannkuch                   | 540 ms                                                 | 592 ms: 1.09x slower                                                   |
| deltablue                  | 4.27 ms                                                | 4.68 ms: 1.10x slower                                                  |
| pidigits                   | 250 ms                                                 | 275 ms: 1.10x slower                                                   |
| regex_v8                   | 32.5 ms                                                | 36.1 ms: 1.11x slower                                                  |
| 2to3                       | 456 ms                                                 | 510 ms: 1.12x slower                                                   |
| json_loads                 | 37.9 us                                                | 42.4 us: 1.12x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.52 ms: 1.12x slower                                                  |
| hexiom                     | 8.27 ms                                                | 9.28 ms: 1.12x slower                                                  |
| coroutines                 | 29.5 ms                                                | 33.3 ms: 1.13x slower                                                  |
| django_template            | 44.9 ms                                                | 51.0 ms: 1.14x slower                                                  |
| mako                       | 15.7 ms                                                | 18.1 ms: 1.15x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 4.01 ms: 1.15x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 77.9 ms: 1.15x slower                                                  |
| logging_format             | 9.59 us                                                | 11.2 us: 1.17x slower                                                  |
| nbody                      | 119 ms                                                 | 141 ms: 1.19x slower                                                   |
| telco                      | 9.59 ms                                                | 11.9 ms: 1.24x slower                                                  |
| coverage                   | 95.4 ms                                                | 120 ms: 1.26x slower                                                   |
| python_startup             | 23.7 ms                                                | 30.8 ms: 1.30x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 19.9 ms: 1.39x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 8.79 ms: 1.50x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 4.11 ms: 2.12x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 98.9 ms: 4.78x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (32): spectral_norm, nqueens, xml_etree_iterparse, sympy_str, sqlalchemy_imperative, pprint_pformat, pathlib, pprint_safe_repr, go, sympy_expand, thrift, scimark_lu, regex_dna, sqlglot_normalize, logging_silent, logging_simple, meteor_contest, genshi_text, html5lib, unpickle_pure_python, sqlglot_transpile, xml_etree_process, asyncio_websockets, python_startup_no_site, crypto_pyaes, sqlglot_parse, richards_super, sqlglot_optimize, regex_compile, generators, xml_etree_generate, sympy_integrate
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.048x faster

# HPT report

- Reliability score: 98.46% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x