# Results vs. 3.12.6

- fork: python
- ref: 71ede1142ddad2d31cc9
- machine: linux-x86_64
- commit hash: 71ede11
- commit date: 2024-11-26
- overall geometric mean: 1.064x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.76 sec: 1.06x faster                                                 |
| html5lib       | 88.9 ms                                                | 84.0 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 930 ms                                                 | 617 ms: 1.51x faster                                                   |
| async_tree_none            | 741 ms                                                 | 493 ms: 1.50x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 652 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 512 ms: 1.37x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 1.43 sec: 1.36x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 804 ms: 1.34x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 1.40 sec: 1.32x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 847 ms: 1.30x faster                                                   |
| async_generators           | 589 ms                                                 | 562 ms: 1.05x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.9 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 117 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.32 ms: 1.19x faster                                                  |
| regex_compile  | 187 ms                                                 | 172 ms: 1.09x faster                                                   |
| regex_dna      | 278 ms                                                 | 288 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 199 ms: 1.21x faster                                                   |
| json_loads           | 37.9 us                                                | 34.1 us: 1.11x faster                                                  |
| xml_etree_iterparse  | 169 ms                                                 | 155 ms: 1.10x faster                                                   |
| xml_etree_generate   | 127 ms                                                 | 116 ms: 1.09x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.65 sec: 1.09x faster                                                 |
| unpickle_pure_python | 300 us                                                 | 287 us: 1.05x faster                                                   |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_process, pickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.5 ms: 1.13x faster                                                  |
| python_startup         | 23.7 ms                                                | 27.9 ms: 1.18x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 15.7 ms                                                | 17.2 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (3): genshi_xml, genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 930 ms                                                 | 617 ms: 1.51x faster                                                   |
| async_tree_none            | 741 ms                                                 | 493 ms: 1.50x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 652 ms: 1.50x faster                                                   |
| deepcopy                   | 468 us                                                 | 337 us: 1.39x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 512 ms: 1.37x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 1.43 sec: 1.36x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 804 ms: 1.34x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 1.40 sec: 1.32x faster                                                 |
| deepcopy_memo              | 52.4 us                                                | 39.8 us: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 847 ms: 1.30x faster                                                   |
| comprehensions             | 27.1 us                                                | 21.9 us: 1.24x faster                                                  |
| pylint                     | 465 ms                                                 | 376 ms: 1.24x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 199 ms: 1.21x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.32 ms: 1.19x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 183 ms: 1.19x faster                                                   |
| logging_simple             | 9.45 us                                                | 7.96 us: 1.19x faster                                                  |
| raytrace                   | 408 ms                                                 | 355 ms: 1.15x faster                                                   |
| python_startup_no_site     | 17.6 ms                                                | 15.5 ms: 1.13x faster                                                  |
| go                         | 172 ms                                                 | 152 ms: 1.13x faster                                                   |
| deepcopy_reduce            | 4.04 us                                                | 3.56 us: 1.13x faster                                                  |
| json_loads                 | 37.9 us                                                | 34.1 us: 1.11x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.58 sec: 1.11x faster                                                 |
| sympy_str                  | 385 ms                                                 | 350 ms: 1.10x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 202 ms: 1.10x faster                                                   |
| pathlib                    | 31.6 ms                                                | 28.8 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 155 ms: 1.10x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 116 ms: 1.09x faster                                                   |
| sqlglot_normalize          | 157 ms                                                 | 144 ms: 1.09x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 88.5 ms: 1.09x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.65 sec: 1.09x faster                                                 |
| regex_compile              | 187 ms                                                 | 172 ms: 1.09x faster                                                   |
| pyflate                    | 727 ms                                                 | 671 ms: 1.08x faster                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 22.9 ms: 1.08x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.67 sec: 1.07x faster                                                 |
| crypto_pyaes               | 107 ms                                                 | 100 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.85 sec: 1.07x faster                                                 |
| json                       | 6.85 ms                                                | 6.43 ms: 1.06x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.76 sec: 1.06x faster                                                 |
| scimark_sor                | 167 ms                                                 | 157 ms: 1.06x faster                                                   |
| html5lib                   | 88.9 ms                                                | 84.0 ms: 1.06x faster                                                  |
| scimark_fft                | 500 ms                                                 | 474 ms: 1.06x faster                                                   |
| float                      | 123 ms                                                 | 117 ms: 1.05x faster                                                   |
| async_generators           | 589 ms                                                 | 562 ms: 1.05x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 6.30 sec: 1.05x faster                                                 |
| unpickle_pure_python       | 300 us                                                 | 287 us: 1.05x faster                                                   |
| sqlglot_parse              | 1.79 ms                                                | 1.72 ms: 1.04x faster                                                  |
| deltablue                  | 4.27 ms                                                | 4.41 ms: 1.03x slower                                                  |
| regex_dna                  | 278 ms                                                 | 288 ms: 1.04x slower                                                   |
| telco                      | 9.59 ms                                                | 10.0 ms: 1.05x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 161 ms: 1.06x slower                                                   |
| coroutines                 | 29.5 ms                                                | 31.9 ms: 1.08x slower                                                  |
| mako                       | 15.7 ms                                                | 17.2 ms: 1.09x slower                                                  |
| coverage                   | 95.4 ms                                                | 112 ms: 1.17x slower                                                   |
| python_startup             | 23.7 ms                                                | 27.9 ms: 1.18x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 7.58 ms: 1.29x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.96 ms: 2.04x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 90.5 ms: 4.37x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (33): logging_format, scimark_sparse_mat_mult, sqlglot_transpile, fannkuch, richards_super, logging_silent, sqlglot_optimize, genshi_xml, spectral_norm, typing_runtime_protocols, xml_etree_process, sqlite_synth, nbody, sympy_integrate, richards, generators, nqueens, pickle_pure_python, chaos, asyncio_websockets, hexiom, bench_thread_pool, pprint_safe_repr, sympy_expand, pidigits, genshi_text, regex_v8, json_dumps, 2to3, django_template, meteor_contest, dulwich_log, thrift
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.064x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.13x