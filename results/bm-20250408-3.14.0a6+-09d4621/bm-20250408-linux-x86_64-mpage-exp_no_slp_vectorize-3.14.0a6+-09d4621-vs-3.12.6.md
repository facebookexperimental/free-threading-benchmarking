# Results vs. 3.12.6

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.126x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.55 sec: 1.13x faster                                                |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 466 ms: 2.10x faster                                                  |
| async_tree_io_tg           | 1.93 sec                                               | 934 ms: 2.07x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 900 ms: 2.05x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 471 ms: 1.98x faster                                                  |
| async_tree_none            | 741 ms                                                 | 380 ms: 1.95x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 375 ms: 1.88x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 696 ms: 1.58x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 691 ms: 1.56x faster                                                  |
| async_generators           | 589 ms                                                 | 508 ms: 1.16x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 717 ms: 1.04x faster                                                  |
| coroutines                 | 29.5 ms                                                | 31.3 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.60x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 101 ms: 1.21x faster                                                  |
| nbody          | 119 ms                                                 | 125 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.29 ms: 1.20x faster                                                 |
| regex_compile  | 187 ms                                                 | 165 ms: 1.13x faster                                                  |
| regex_dna      | 278 ms                                                 | 291 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 197 ms: 1.22x faster                                                  |
| xml_etree_iterparse  | 169 ms                                                 | 145 ms: 1.16x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 110 ms: 1.16x faster                                                  |
| tomli_loads          | 2.88 sec                                               | 2.50 sec: 1.15x faster                                                |
| unpickle_pure_python | 300 us                                                 | 285 us: 1.05x faster                                                  |
| json_dumps           | 14.3 ms                                                | 14.9 ms: 1.04x slower                                                 |
| json_loads           | 37.9 us                                                | 42.1 us: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (2): xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 23.7 ms                                                | 29.3 ms: 1.24x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml     | 67.6 ms                                                | 63.9 ms: 1.06x faster                                                 |
| genshi_text    | 30.2 ms                                                | 28.7 ms: 1.05x faster                                                 |
| mako           | 15.7 ms                                                | 16.8 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 466 ms: 2.10x faster                                                  |
| async_tree_io_tg           | 1.93 sec                                               | 934 ms: 2.07x faster                                                  |
| mdp                        | 3.97 sec                                               | 1.93 sec: 2.06x faster                                                |
| async_tree_io              | 1.85 sec                                               | 900 ms: 2.05x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 471 ms: 1.98x faster                                                  |
| async_tree_none            | 741 ms                                                 | 380 ms: 1.95x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 375 ms: 1.88x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 696 ms: 1.58x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 691 ms: 1.56x faster                                                  |
| deepcopy                   | 468 us                                                 | 327 us: 1.43x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 2.53 ms: 1.38x faster                                                 |
| deepcopy_memo              | 52.4 us                                                | 38.2 us: 1.37x faster                                                 |
| comprehensions             | 27.1 us                                                | 20.8 us: 1.30x faster                                                 |
| deepcopy_reduce            | 4.04 us                                                | 3.29 us: 1.23x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 197 ms: 1.22x faster                                                  |
| go                         | 172 ms                                                 | 142 ms: 1.21x faster                                                  |
| float                      | 123 ms                                                 | 101 ms: 1.21x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.29 ms: 1.20x faster                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 81.4 ms: 1.18x faster                                                 |
| raytrace                   | 408 ms                                                 | 345 ms: 1.18x faster                                                  |
| spectral_norm              | 156 ms                                                 | 134 ms: 1.16x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 145 ms: 1.16x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.54 sec: 1.16x faster                                                |
| xml_etree_generate         | 127 ms                                                 | 110 ms: 1.16x faster                                                  |
| async_generators           | 589 ms                                                 | 508 ms: 1.16x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.50 sec: 1.15x faster                                                |
| sqlalchemy_declarative     | 218 ms                                                 | 190 ms: 1.15x faster                                                  |
| richards_super             | 72.8 ms                                                | 63.6 ms: 1.15x faster                                                 |
| pyflate                    | 727 ms                                                 | 636 ms: 1.14x faster                                                  |
| pylint                     | 465 ms                                                 | 407 ms: 1.14x faster                                                  |
| sympy_str                  | 385 ms                                                 | 338 ms: 1.14x faster                                                  |
| scimark_fft                | 500 ms                                                 | 440 ms: 1.14x faster                                                  |
| chaos                      | 84.9 ms                                                | 75.0 ms: 1.13x faster                                                 |
| regex_compile              | 187 ms                                                 | 165 ms: 1.13x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 95.2 ms: 1.13x faster                                                 |
| docutils                   | 4.00 sec                                               | 3.55 sec: 1.13x faster                                                |
| pathlib                    | 31.6 ms                                                | 28.5 ms: 1.11x faster                                                 |
| dulwich_log                | 100 ms                                                 | 91.0 ms: 1.10x faster                                                 |
| nqueens                    | 117 ms                                                 | 107 ms: 1.10x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 6.05 sec: 1.09x faster                                                |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.20 ms: 1.08x faster                                                 |
| logging_silent             | 139 ns                                                 | 130 ns: 1.07x faster                                                  |
| pprint_safe_repr           | 967 ms                                                 | 904 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.85 sec: 1.07x faster                                                |
| sqlalchemy_imperative      | 24.7 ms                                                | 23.2 ms: 1.06x faster                                                 |
| genshi_xml                 | 67.6 ms                                                | 63.9 ms: 1.06x faster                                                 |
| scimark_sor                | 167 ms                                                 | 158 ms: 1.06x faster                                                  |
| richards                   | 60.3 ms                                                | 57.2 ms: 1.05x faster                                                 |
| genshi_text                | 30.2 ms                                                | 28.7 ms: 1.05x faster                                                 |
| unpickle_pure_python       | 300 us                                                 | 285 us: 1.05x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 717 ms: 1.04x faster                                                  |
| deltablue                  | 4.27 ms                                                | 4.41 ms: 1.03x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 14.9 ms: 1.04x slower                                                 |
| regex_dna                  | 278 ms                                                 | 291 ms: 1.05x slower                                                  |
| nbody                      | 119 ms                                                 | 125 ms: 1.05x slower                                                  |
| coroutines                 | 29.5 ms                                                | 31.3 ms: 1.06x slower                                                 |
| mako                       | 15.7 ms                                                | 16.8 ms: 1.07x slower                                                 |
| generators                 | 41.1 ms                                                | 44.6 ms: 1.08x slower                                                 |
| json_loads                 | 37.9 us                                                | 42.1 us: 1.11x slower                                                 |
| coverage                   | 95.4 ms                                                | 115 ms: 1.20x slower                                                  |
| python_startup             | 23.7 ms                                                | 29.3 ms: 1.24x slower                                                 |
| gc_traversal               | 5.86 ms                                                | 8.36 ms: 1.43x slower                                                 |
| create_gc_cycles           | 1.94 ms                                                | 3.50 ms: 1.80x slower                                                 |
| bench_mp_pool              | 20.7 ms                                                | 90.7 ms: 4.38x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                          |

Benchmark hidden because not significant (20): sympy_integrate, logging_simple, sympy_sum, xml_etree_process, sqlite_synth, meteor_contest, 2to3, hexiom, pickle_pure_python, typing_runtime_protocols, fannkuch, python_startup_no_site, scimark_lu, django_template, telco, pidigits, json, sympy_expand, logging_format, regex_v8
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250408-3.14.0a6+-09d4621/bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.126x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.14x