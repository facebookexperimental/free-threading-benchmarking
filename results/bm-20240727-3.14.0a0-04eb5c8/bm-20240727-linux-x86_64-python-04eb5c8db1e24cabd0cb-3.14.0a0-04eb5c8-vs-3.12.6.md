# Results vs. 3.12.6

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 425 ms: 1.07x faster                                                  |
| tornado_http   | 266 ms                                                 | 228 ms: 1.17x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.22 sec: 1.58x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 591 ms: 1.57x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 451 ms: 1.56x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 626 ms: 1.56x faster                                                  |
| async_tree_none            | 741 ms                                                 | 499 ms: 1.49x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.26 sec: 1.47x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 806 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 794 ms: 1.36x faster                                                  |
| coroutines                 | 29.5 ms                                                | 31.6 ms: 1.07x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                          |

Benchmark hidden because not significant (4): asyncio_tcp_ssl, async_generators, asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 112 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.78 ms: 1.07x faster                                                 |
| regex_compile  | 187 ms                                                 | 174 ms: 1.07x faster                                                  |
| regex_v8       | 32.5 ms                                                | 35.8 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|---------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict         | 52.7 us                                                | 46.8 us: 1.13x faster                                                 |
| pickle_list         | 6.97 us                                                | 6.33 us: 1.10x faster                                                 |
| xml_etree_generate  | 127 ms                                                 | 117 ms: 1.09x faster                                                  |
| tomli_loads         | 2.88 sec                                               | 2.66 sec: 1.08x faster                                                |
| xml_etree_iterparse | 169 ms                                                 | 158 ms: 1.07x faster                                                  |
| unpickle            | 21.2 us                                                | 19.8 us: 1.07x faster                                                 |
| xml_etree_parse     | 241 ms                                                 | 230 ms: 1.05x faster                                                  |
| unpickle_list       | 6.83 us                                                | 7.22 us: 1.06x slower                                                 |
| json_dumps          | 14.3 ms                                                | 15.5 ms: 1.08x slower                                                 |
| Geometric mean      | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (5): pickle, xml_etree_process, json_loads, pickle_pure_python, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.0 ms: 1.17x faster                                                 |
| python_startup         | 23.7 ms                                                | 22.1 ms: 1.07x faster                                                 |
| Geometric mean         | (ref)                                                  | 1.12x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml     | 67.6 ms                                                | 73.3 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (3): django_template, genshi_text, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.22 sec: 1.58x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 591 ms: 1.57x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 451 ms: 1.56x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 626 ms: 1.56x faster                                                  |
| async_tree_none            | 741 ms                                                 | 499 ms: 1.49x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.26 sec: 1.47x faster                                                |
| deepcopy_memo              | 52.4 us                                                | 38.4 us: 1.37x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 806 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 794 ms: 1.36x faster                                                  |
| comprehensions             | 27.1 us                                                | 20.9 us: 1.30x faster                                                 |
| deepcopy                   | 468 us                                                 | 372 us: 1.26x faster                                                  |
| raytrace                   | 408 ms                                                 | 338 ms: 1.21x faster                                                  |
| pathlib                    | 31.6 ms                                                | 26.6 ms: 1.19x faster                                                 |
| logging_simple             | 9.45 us                                                | 7.95 us: 1.19x faster                                                 |
| bench_thread_pool          | 3.48 ms                                                | 2.97 ms: 1.17x faster                                                 |
| python_startup_no_site     | 17.6 ms                                                | 15.0 ms: 1.17x faster                                                 |
| tornado_http               | 266 ms                                                 | 228 ms: 1.17x faster                                                  |
| pickle_dict                | 52.7 us                                                | 46.8 us: 1.13x faster                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 5.99 ms: 1.12x faster                                                 |
| sympy_str                  | 385 ms                                                 | 345 ms: 1.12x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.64 us: 1.11x faster                                                 |
| pyflate                    | 727 ms                                                 | 657 ms: 1.11x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 87.1 ms: 1.11x faster                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.12 ms: 1.10x faster                                                 |
| pickle_list                | 6.97 us                                                | 6.33 us: 1.10x faster                                                 |
| richards_super             | 72.8 ms                                                | 66.2 ms: 1.10x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.63 sec: 1.10x faster                                                |
| float                      | 123 ms                                                 | 112 ms: 1.10x faster                                                  |
| logging_silent             | 139 ns                                                 | 128 ns: 1.09x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.64 sec: 1.09x faster                                                |
| bench_mp_pool              | 20.7 ms                                                | 19.0 ms: 1.09x faster                                                 |
| sqlglot_normalize          | 157 ms                                                 | 144 ms: 1.09x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 117 ms: 1.09x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.66 sec: 1.08x faster                                                |
| bpe_tokeniser              | 6.59 sec                                               | 6.13 sec: 1.07x faster                                                |
| crypto_pyaes               | 107 ms                                                 | 99.9 ms: 1.07x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 4.78 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 158 ms: 1.07x faster                                                  |
| logging_format             | 9.59 us                                                | 8.93 us: 1.07x faster                                                 |
| 2to3                       | 456 ms                                                 | 425 ms: 1.07x faster                                                  |
| python_startup             | 23.7 ms                                                | 22.1 ms: 1.07x faster                                                 |
| chaos                      | 84.9 ms                                                | 79.1 ms: 1.07x faster                                                 |
| regex_compile              | 187 ms                                                 | 174 ms: 1.07x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 207 ms: 1.07x faster                                                  |
| unpickle                   | 21.2 us                                                | 19.8 us: 1.07x faster                                                 |
| gc_traversal               | 5.86 ms                                                | 5.48 ms: 1.07x faster                                                 |
| scimark_fft                | 500 ms                                                 | 471 ms: 1.06x faster                                                  |
| meteor_contest             | 146 ms                                                 | 138 ms: 1.06x faster                                                  |
| sqlglot_parse              | 1.79 ms                                                | 1.69 ms: 1.06x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 230 ms: 1.05x faster                                                  |
| generators                 | 41.1 ms                                                | 39.3 ms: 1.05x faster                                                 |
| deltablue                  | 4.27 ms                                                | 4.11 ms: 1.04x faster                                                 |
| richards                   | 60.3 ms                                                | 63.4 ms: 1.05x slower                                                 |
| unpickle_list              | 6.83 us                                                | 7.22 us: 1.06x slower                                                 |
| sqlite_synth               | 3.87 us                                                | 4.13 us: 1.07x slower                                                 |
| coroutines                 | 29.5 ms                                                | 31.6 ms: 1.07x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 15.5 ms: 1.08x slower                                                 |
| genshi_xml                 | 67.6 ms                                                | 73.3 ms: 1.08x slower                                                 |
| go                         | 172 ms                                                 | 188 ms: 1.09x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 35.8 ms: 1.10x slower                                                 |
| unpack_sequence            | 60.2 ns                                                | 67.4 ns: 1.12x slower                                                 |
| telco                      | 9.59 ms                                                | 10.9 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.94 ms                                                | 2.32 ms: 1.20x slower                                                 |
| coverage                   | 95.4 ms                                                | 118 ms: 1.24x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (33): sympy_integrate, pickle, spectral_norm, xml_etree_process, pidigits, asyncio_tcp_ssl, django_template, json_loads, pprint_pformat, json, async_generators, docutils, pickle_pure_python, nbody, fannkuch, asyncio_websockets, dask, genshi_text, pprint_safe_repr, asyncio_tcp, nqueens, scimark_sor, regex_dna, scimark_lu, sympy_expand, sqlglot_optimize, unpickle_pure_python, pylint, hexiom, mako, thrift, typing_runtime_protocols, html5lib
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.02x