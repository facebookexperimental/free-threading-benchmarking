# Results vs. 3.12.6

- fork: python
- ref: 1feaecc2bc42cb96f2d7
- machine: linux-x86_64
- commit hash: 1feaecc
- commit date: 2025-02-10
- overall geometric mean: 1.108x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.70 sec: 1.08x faster                                                 |
| html5lib       | 88.9 ms                                                | 81.6 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 934 ms: 2.07x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 473 ms: 2.06x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 923 ms: 2.00x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 477 ms: 1.95x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 370 ms: 1.90x faster                                                   |
| async_tree_none            | 741 ms                                                 | 404 ms: 1.84x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 700 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 711 ms: 1.52x faster                                                   |
| async_generators           | 589 ms                                                 | 524 ms: 1.12x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.58x faster                                                           |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 105 ms: 1.17x faster                                                   |
| pidigits       | 250 ms                                                 | 239 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.39 ms: 1.17x faster                                                  |
| regex_compile  | 187 ms                                                 | 166 ms: 1.13x faster                                                   |
| regex_v8       | 32.5 ms                                                | 34.7 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 210 ms: 1.15x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.57 sec: 1.12x faster                                                 |
| xml_etree_generate   | 127 ms                                                 | 115 ms: 1.10x faster                                                   |
| xml_etree_process    | 83.7 ms                                                | 77.9 ms: 1.07x faster                                                  |
| unpickle_pure_python | 300 us                                                 | 285 us: 1.05x faster                                                   |
| json_dumps           | 14.3 ms                                                | 16.3 ms: 1.14x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (3): pickle_pure_python, xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 16.0 ms: 1.10x faster                                                  |
| python_startup         | 23.7 ms                                                | 27.0 ms: 1.14x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 62.8 ms: 1.08x faster                                                  |
| django_template | 44.9 ms                                                | 43.0 ms: 1.05x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): mako, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 934 ms: 2.07x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 473 ms: 2.06x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 923 ms: 2.00x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 477 ms: 1.95x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 370 ms: 1.90x faster                                                   |
| async_tree_none            | 741 ms                                                 | 404 ms: 1.84x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 700 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 711 ms: 1.52x faster                                                   |
| deepcopy                   | 468 us                                                 | 340 us: 1.38x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 38.6 us: 1.36x faster                                                  |
| spectral_norm              | 156 ms                                                 | 118 ms: 1.32x faster                                                   |
| comprehensions             | 27.1 us                                                | 20.8 us: 1.30x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 178 ms: 1.23x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 89.7 ms: 1.20x faster                                                  |
| pylint                     | 465 ms                                                 | 390 ms: 1.19x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 5.63 ms: 1.19x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.39 ms: 1.17x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.53 sec: 1.17x faster                                                 |
| float                      | 123 ms                                                 | 105 ms: 1.17x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.67 sec: 1.16x faster                                                 |
| logging_simple             | 9.45 us                                                | 8.19 us: 1.15x faster                                                  |
| sympy_str                  | 385 ms                                                 | 335 ms: 1.15x faster                                                   |
| chaos                      | 84.9 ms                                                | 73.9 ms: 1.15x faster                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 21.5 ms: 1.15x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 210 ms: 1.15x faster                                                   |
| pyflate                    | 727 ms                                                 | 639 ms: 1.14x faster                                                   |
| typing_runtime_protocols   | 224 us                                                 | 199 us: 1.13x faster                                                   |
| regex_compile              | 187 ms                                                 | 166 ms: 1.13x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.53 sec: 1.13x faster                                                 |
| async_generators           | 589 ms                                                 | 524 ms: 1.12x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.57 sec: 1.12x faster                                                 |
| sqlglot_normalize          | 157 ms                                                 | 140 ms: 1.12x faster                                                   |
| fannkuch                   | 540 ms                                                 | 487 ms: 1.11x faster                                                   |
| scimark_fft                | 500 ms                                                 | 452 ms: 1.11x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 115 ms: 1.10x faster                                                   |
| python_startup_no_site     | 17.6 ms                                                | 16.0 ms: 1.10x faster                                                  |
| dulwich_log                | 100 ms                                                 | 91.7 ms: 1.09x faster                                                  |
| html5lib                   | 88.9 ms                                                | 81.6 ms: 1.09x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 204 ms: 1.09x faster                                                   |
| richards_super             | 72.8 ms                                                | 67.1 ms: 1.08x faster                                                  |
| scimark_sor                | 167 ms                                                 | 154 ms: 1.08x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.70 sec: 1.08x faster                                                 |
| go                         | 172 ms                                                 | 160 ms: 1.08x faster                                                   |
| genshi_xml                 | 67.6 ms                                                | 62.8 ms: 1.08x faster                                                  |
| pathlib                    | 31.6 ms                                                | 29.4 ms: 1.08x faster                                                  |
| xml_etree_process          | 83.7 ms                                                | 77.9 ms: 1.07x faster                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.18 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.85 sec: 1.07x faster                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 71.4 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 967 ms                                                 | 911 ms: 1.06x faster                                                   |
| raytrace                   | 408 ms                                                 | 385 ms: 1.06x faster                                                   |
| unpickle_pure_python       | 300 us                                                 | 285 us: 1.05x faster                                                   |
| django_template            | 44.9 ms                                                | 43.0 ms: 1.05x faster                                                  |
| pidigits                   | 250 ms                                                 | 239 ms: 1.05x faster                                                   |
| deltablue                  | 4.27 ms                                                | 4.14 ms: 1.03x faster                                                  |
| regex_v8                   | 32.5 ms                                                | 34.7 ms: 1.07x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 32.1 ms: 1.08x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.3 ms: 1.14x slower                                                  |
| python_startup             | 23.7 ms                                                | 27.0 ms: 1.14x slower                                                  |
| coverage                   | 95.4 ms                                                | 118 ms: 1.24x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 9.97 ms: 1.70x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 5.09 ms: 2.63x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 92.2 ms: 4.45x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (27): nqueens, sqlite_synth, bench_thread_pool, richards, pickle_pure_python, scimark_monte_carlo, xml_etree_iterparse, mako, json, logging_format, generators, coroutines, deepcopy_reduce, 2to3, scimark_lu, hexiom, nbody, sqlglot_parse, sympy_expand, json_loads, meteor_contest, genshi_text, logging_silent, asyncio_websockets, telco, regex_dna, thrift
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x