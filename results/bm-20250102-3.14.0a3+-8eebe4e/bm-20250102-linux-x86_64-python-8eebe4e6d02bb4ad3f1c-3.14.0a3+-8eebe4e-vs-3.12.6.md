# Results vs. 3.12.6

- fork: python
- ref: 8eebe4e6d02bb4ad3f1c
- machine: linux-x86_64
- commit hash: 8eebe4e
- commit date: 2025-01-02
- overall geometric mean: 1.145x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 410 ms: 1.11x faster                                                   |
| docutils       | 4.00 sec                                               | 3.51 sec: 1.14x faster                                                 |
| html5lib       | 88.9 ms                                                | 81.3 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 820 ms: 2.36x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 838 ms: 2.21x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 432 ms: 2.16x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 336 ms: 2.10x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 466 ms: 2.10x faster                                                   |
| async_tree_none            | 741 ms                                                 | 383 ms: 1.93x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 643 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 683 ms: 1.58x faster                                                   |
| async_generators           | 589 ms                                                 | 538 ms: 1.10x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 707 ms: 1.06x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.68x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 100 ms: 1.22x faster                                                   |
| pidigits       | 250 ms                                                 | 231 ms: 1.08x faster                                                   |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.17 ms: 1.23x faster                                                  |
| regex_compile  | 187 ms                                                 | 161 ms: 1.16x faster                                                   |
| regex_dna      | 278 ms                                                 | 268 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 204 ms: 1.18x faster                                                   |
| xml_etree_generate  | 127 ms                                                 | 109 ms: 1.16x faster                                                   |
| xml_etree_iterparse | 169 ms                                                 | 147 ms: 1.15x faster                                                   |
| json_loads          | 37.9 us                                                | 33.5 us: 1.13x faster                                                  |
| tomli_loads         | 2.88 sec                                               | 2.61 sec: 1.10x faster                                                 |
| xml_etree_process   | 83.7 ms                                                | 78.3 ms: 1.07x faster                                                  |
| Geometric mean      | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (3): unpickle_pure_python, pickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.7 ms: 1.20x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 67.6 ms                                                | 60.0 ms: 1.13x faster                                                  |
| genshi_text    | 30.2 ms                                                | 28.3 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 820 ms: 2.36x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 838 ms: 2.21x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 432 ms: 2.16x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 336 ms: 2.10x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 466 ms: 2.10x faster                                                   |
| async_tree_none            | 741 ms                                                 | 383 ms: 1.93x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 643 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 683 ms: 1.58x faster                                                   |
| deepcopy                   | 468 us                                                 | 321 us: 1.46x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 37.1 us: 1.41x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.4 us: 1.27x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.17 ms: 1.23x faster                                                  |
| pylint                     | 465 ms                                                 | 378 ms: 1.23x faster                                                   |
| float                      | 123 ms                                                 | 100 ms: 1.22x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 179 ms: 1.22x faster                                                   |
| raytrace                   | 408 ms                                                 | 336 ms: 1.21x faster                                                   |
| pathlib                    | 31.6 ms                                                | 26.2 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.35 us: 1.20x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 14.7 ms: 1.20x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 2.94 ms: 1.18x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 204 ms: 1.18x faster                                                   |
| pyflate                    | 727 ms                                                 | 621 ms: 1.17x faster                                                   |
| spectral_norm              | 156 ms                                                 | 133 ms: 1.17x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 109 ms: 1.16x faster                                                   |
| regex_compile              | 187 ms                                                 | 161 ms: 1.16x faster                                                   |
| logging_simple             | 9.45 us                                                | 8.15 us: 1.16x faster                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.03 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 147 ms: 1.15x faster                                                   |
| json                       | 6.85 ms                                                | 5.97 ms: 1.15x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 5.75 sec: 1.14x faster                                                 |
| docutils                   | 4.00 sec                                               | 3.51 sec: 1.14x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.58 sec: 1.14x faster                                                 |
| sqlglot_normalize          | 157 ms                                                 | 138 ms: 1.14x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.50 sec: 1.14x faster                                                 |
| json_loads                 | 37.9 us                                                | 33.5 us: 1.13x faster                                                  |
| nqueens                    | 117 ms                                                 | 103 ms: 1.13x faster                                                   |
| genshi_xml                 | 67.6 ms                                                | 60.0 ms: 1.13x faster                                                  |
| richards_super             | 72.8 ms                                                | 65.0 ms: 1.12x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 96.1 ms: 1.12x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 86.3 ms: 1.12x faster                                                  |
| 2to3                       | 456 ms                                                 | 410 ms: 1.11x faster                                                   |
| scimark_fft                | 500 ms                                                 | 451 ms: 1.11x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.61 sec: 1.10x faster                                                 |
| chaos                      | 84.9 ms                                                | 77.2 ms: 1.10x faster                                                  |
| go                         | 172 ms                                                 | 157 ms: 1.10x faster                                                   |
| async_generators           | 589 ms                                                 | 538 ms: 1.10x faster                                                   |
| html5lib                   | 88.9 ms                                                | 81.3 ms: 1.09x faster                                                  |
| sympy_integrate            | 29.8 ms                                                | 27.3 ms: 1.09x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 206 us: 1.09x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.82 sec: 1.09x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 3.57 us: 1.08x faster                                                  |
| pidigits                   | 250 ms                                                 | 231 ms: 1.08x faster                                                   |
| generators                 | 41.1 ms                                                | 38.1 ms: 1.08x faster                                                  |
| thrift                     | 1.06 ms                                                | 984 us: 1.08x faster                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 23.1 ms: 1.07x faster                                                  |
| genshi_text                | 30.2 ms                                                | 28.3 ms: 1.07x faster                                                  |
| xml_etree_process          | 83.7 ms                                                | 78.3 ms: 1.07x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 208 ms: 1.07x faster                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 71.3 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 967 ms                                                 | 908 ms: 1.06x faster                                                   |
| dulwich_log                | 100 ms                                                 | 94.2 ms: 1.06x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 707 ms: 1.06x faster                                                   |
| sympy_str                  | 385 ms                                                 | 364 ms: 1.06x faster                                                   |
| meteor_contest             | 146 ms                                                 | 139 ms: 1.05x faster                                                   |
| fannkuch                   | 540 ms                                                 | 517 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.42 ms: 1.04x faster                                                  |
| scimark_sor                | 167 ms                                                 | 160 ms: 1.04x faster                                                   |
| logging_silent             | 139 ns                                                 | 134 ns: 1.04x faster                                                   |
| regex_dna                  | 278 ms                                                 | 268 ms: 1.04x faster                                                   |
| deltablue                  | 4.27 ms                                                | 4.13 ms: 1.03x faster                                                  |
| telco                      | 9.59 ms                                                | 10.5 ms: 1.10x slower                                                  |
| coverage                   | 95.4 ms                                                | 110 ms: 1.16x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.96 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.57 ms: 1.84x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 89.3 ms: 4.31x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.12x faster                                                           |

Benchmark hidden because not significant (15): richards, unpickle_pure_python, django_template, pickle_pure_python, regex_v8, scimark_lu, python_startup, logging_format, sympy_expand, nbody, sqlglot_parse, coroutines, mako, json_dumps, hexiom
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250102-3.14.0a3+-8eebe4e/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.145x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.13x