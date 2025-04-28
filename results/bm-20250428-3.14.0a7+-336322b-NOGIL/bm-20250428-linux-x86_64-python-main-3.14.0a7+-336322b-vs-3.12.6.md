# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 336322b
- commit date: 2025-04-28
- overall geometric mean: 1.099x faster
- HPT reliability: 87.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 404 ms: 1.13x faster                                   |
| docutils       | 4.00 sec                                               | 3.87 sec: 1.03x faster                                 |
| html5lib       | 88.9 ms                                                | 85.7 ms: 1.04x faster                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 670 ms: 2.89x faster                                   |
| async_tree_io              | 1.85 sec                                               | 723 ms: 2.56x faster                                   |
| async_tree_none_tg         | 704 ms                                                 | 294 ms: 2.40x faster                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 395 ms: 2.35x faster                                   |
| async_tree_memoization     | 977 ms                                                 | 440 ms: 2.22x faster                                   |
| async_tree_none            | 741 ms                                                 | 342 ms: 2.17x faster                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 578 ms: 1.90x faster                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 629 ms: 1.71x faster                                   |
| async_generators           | 589 ms                                                 | 538 ms: 1.10x faster                                   |
| asyncio_websockets         | 748 ms                                                 | 689 ms: 1.08x faster                                   |
| Geometric mean             | (ref)                                                  | 1.83x faster                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 123 ms                                                 | 91.2 ms: 1.35x faster                                  |
| pidigits       | 250 ms                                                 | 225 ms: 1.11x faster                                   |
| nbody          | 119 ms                                                 | 150 ms: 1.26x slower                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.77 ms: 1.36x faster                                  |
| regex_v8       | 32.5 ms                                                | 26.3 ms: 1.23x faster                                  |
| regex_dna      | 278 ms                                                 | 248 ms: 1.12x faster                                   |
| regex_compile  | 187 ms                                                 | 180 ms: 1.04x faster                                   |
| Geometric mean | (ref)                                                  | 1.18x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|---------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| xml_etree_iterparse | 169 ms                                                 | 125 ms: 1.36x faster                                   |
| xml_etree_parse     | 241 ms                                                 | 187 ms: 1.29x faster                                   |
| tomli_loads         | 2.88 sec                                               | 2.78 sec: 1.04x faster                                 |
| json_loads          | 37.9 us                                                | 41.0 us: 1.08x slower                                  |
| xml_etree_process   | 83.7 ms                                                | 91.7 ms: 1.10x slower                                  |
| json_dumps          | 14.3 ms                                                | 17.0 ms: 1.19x slower                                  |
| Geometric mean      | (ref)                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (3): unpickle_pure_python, xml_etree_generate, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.8 ms: 1.19x faster                                  |
| Geometric mean         | (ref)                                                  | 1.08x faster                                           |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 44.9 ms                                                | 48.8 ms: 1.09x slower                                  |
| genshi_xml      | 67.6 ms                                                | 76.1 ms: 1.13x slower                                  |
| genshi_text     | 30.2 ms                                                | 34.1 ms: 1.13x slower                                  |
| mako            | 15.7 ms                                                | 22.4 ms: 1.42x slower                                  |
| Geometric mean  | (ref)                                                  | 1.18x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 670 ms: 2.89x faster                                   |
| async_tree_io              | 1.85 sec                                               | 723 ms: 2.56x faster                                   |
| async_tree_none_tg         | 704 ms                                                 | 294 ms: 2.40x faster                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 395 ms: 2.35x faster                                   |
| async_tree_memoization     | 977 ms                                                 | 440 ms: 2.22x faster                                   |
| async_tree_none            | 741 ms                                                 | 342 ms: 2.17x faster                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 578 ms: 1.90x faster                                   |
| mdp                        | 3.97 sec                                               | 2.29 sec: 1.73x faster                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 629 ms: 1.71x faster                                   |
| gc_traversal               | 5.86 ms                                                | 3.58 ms: 1.64x faster                                  |
| bench_thread_pool          | 3.48 ms                                                | 2.50 ms: 1.39x faster                                  |
| regex_effbot               | 5.13 ms                                                | 3.77 ms: 1.36x faster                                  |
| xml_etree_iterparse        | 169 ms                                                 | 125 ms: 1.36x faster                                   |
| float                      | 123 ms                                                 | 91.2 ms: 1.35x faster                                  |
| sqlite_synth               | 3.87 us                                                | 2.95 us: 1.31x faster                                  |
| xml_etree_parse            | 241 ms                                                 | 187 ms: 1.29x faster                                   |
| dulwich_log                | 100 ms                                                 | 79.8 ms: 1.26x faster                                  |
| deepcopy                   | 468 us                                                 | 377 us: 1.24x faster                                   |
| regex_v8                   | 32.5 ms                                                | 26.3 ms: 1.23x faster                                  |
| pycparser                  | 1.79 sec                                               | 1.46 sec: 1.23x faster                                 |
| python_startup_no_site     | 17.6 ms                                                | 14.8 ms: 1.19x faster                                  |
| pathlib                    | 31.6 ms                                                | 27.1 ms: 1.17x faster                                  |
| deepcopy_memo              | 52.4 us                                                | 45.8 us: 1.14x faster                                  |
| 2to3                       | 456 ms                                                 | 404 ms: 1.13x faster                                   |
| regex_dna                  | 278 ms                                                 | 248 ms: 1.12x faster                                   |
| pidigits                   | 250 ms                                                 | 225 ms: 1.11x faster                                   |
| async_generators           | 589 ms                                                 | 538 ms: 1.10x faster                                   |
| pyflate                    | 727 ms                                                 | 667 ms: 1.09x faster                                   |
| spectral_norm              | 156 ms                                                 | 143 ms: 1.09x faster                                   |
| asyncio_websockets         | 748 ms                                                 | 689 ms: 1.08x faster                                   |
| scimark_fft                | 500 ms                                                 | 463 ms: 1.08x faster                                   |
| logging_simple             | 9.45 us                                                | 8.78 us: 1.08x faster                                  |
| pylint                     | 465 ms                                                 | 433 ms: 1.07x faster                                   |
| comprehensions             | 27.1 us                                                | 25.3 us: 1.07x faster                                  |
| raytrace                   | 408 ms                                                 | 381 ms: 1.07x faster                                   |
| scimark_sor                | 167 ms                                                 | 158 ms: 1.06x faster                                   |
| chaos                      | 84.9 ms                                                | 80.7 ms: 1.05x faster                                  |
| html5lib                   | 88.9 ms                                                | 85.7 ms: 1.04x faster                                  |
| regex_compile              | 187 ms                                                 | 180 ms: 1.04x faster                                   |
| tomli_loads                | 2.88 sec                                               | 2.78 sec: 1.04x faster                                 |
| go                         | 172 ms                                                 | 166 ms: 1.04x faster                                   |
| docutils                   | 4.00 sec                                               | 3.87 sec: 1.03x faster                                 |
| deepcopy_reduce            | 4.04 us                                                | 3.94 us: 1.03x faster                                  |
| crypto_pyaes               | 107 ms                                                 | 111 ms: 1.04x slower                                   |
| json                       | 6.85 ms                                                | 7.13 ms: 1.04x slower                                  |
| sympy_str                  | 385 ms                                                 | 401 ms: 1.04x slower                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.06 ms: 1.05x slower                                  |
| richards_super             | 72.8 ms                                                | 76.8 ms: 1.05x slower                                  |
| pprint_pformat             | 1.98 sec                                               | 2.10 sec: 1.06x slower                                 |
| hexiom                     | 8.27 ms                                                | 8.84 ms: 1.07x slower                                  |
| generators                 | 41.1 ms                                                | 44.4 ms: 1.08x slower                                  |
| json_loads                 | 37.9 us                                                | 41.0 us: 1.08x slower                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.05 sec: 1.08x slower                                 |
| django_template            | 44.9 ms                                                | 48.8 ms: 1.09x slower                                  |
| meteor_contest             | 146 ms                                                 | 160 ms: 1.09x slower                                   |
| telco                      | 9.59 ms                                                | 10.5 ms: 1.09x slower                                  |
| xml_etree_process          | 83.7 ms                                                | 91.7 ms: 1.10x slower                                  |
| typing_runtime_protocols   | 224 us                                                 | 246 us: 1.10x slower                                   |
| deltablue                  | 4.27 ms                                                | 4.72 ms: 1.11x slower                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.29 sec: 1.11x slower                                 |
| scimark_lu                 | 152 ms                                                 | 168 ms: 1.11x slower                                   |
| richards                   | 60.3 ms                                                | 67.1 ms: 1.11x slower                                  |
| fannkuch                   | 540 ms                                                 | 601 ms: 1.11x slower                                   |
| genshi_xml                 | 67.6 ms                                                | 76.1 ms: 1.13x slower                                  |
| genshi_text                | 30.2 ms                                                | 34.1 ms: 1.13x slower                                  |
| sympy_expand               | 582 ms                                                 | 658 ms: 1.13x slower                                   |
| json_dumps                 | 14.3 ms                                                | 17.0 ms: 1.19x slower                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.38 ms: 1.23x slower                                  |
| nbody                      | 119 ms                                                 | 150 ms: 1.26x slower                                   |
| mako                       | 15.7 ms                                                | 22.4 ms: 1.42x slower                                  |
| coverage                   | 95.4 ms                                                | 143 ms: 1.50x slower                                   |
| bench_mp_pool              | 20.7 ms                                                | 75.4 ms: 3.64x slower                                  |
| Geometric mean             | (ref)                                                  | 1.09x faster                                           |

Benchmark hidden because not significant (12): nqueens, unpickle_pure_python, sympy_sum, logging_silent, sympy_integrate, python_startup, scimark_monte_carlo, thrift, coroutines, xml_etree_generate, logging_format, pickle_pure_python
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250428-3.14.0a7+-336322b-NOGIL/bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.099x faster

# HPT report

- Reliability score: 87.91% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.36x