# Results vs. 3.12.6

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: linux-x86_64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.120x faster
- HPT reliability: 97.48%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 384 ms: 1.19x faster                                                  |
| docutils       | 4.00 sec                                               | 3.62 sec: 1.10x faster                                                |
| html5lib       | 88.9 ms                                                | 82.0 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                  | 1.12x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 677 ms: 2.86x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 727 ms: 2.54x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 294 ms: 2.40x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 395 ms: 2.36x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 440 ms: 2.22x faster                                                  |
| async_tree_none            | 741 ms                                                 | 348 ms: 2.13x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 585 ms: 1.88x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 638 ms: 1.69x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 674 ms: 1.11x faster                                                  |
| async_generators           | 589 ms                                                 | 538 ms: 1.10x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.83x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 90.3 ms: 1.36x faster                                                 |
| pidigits       | 250 ms                                                 | 215 ms: 1.16x faster                                                  |
| nbody          | 119 ms                                                 | 154 ms: 1.29x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.92 ms: 1.31x faster                                                 |
| regex_v8       | 32.5 ms                                                | 26.8 ms: 1.21x faster                                                 |
| regex_dna      | 278 ms                                                 | 249 ms: 1.12x faster                                                  |
| regex_compile  | 187 ms                                                 | 178 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.17x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|---------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse | 169 ms                                                 | 118 ms: 1.44x faster                                                  |
| xml_etree_parse     | 241 ms                                                 | 171 ms: 1.41x faster                                                  |
| tomli_loads         | 2.88 sec                                               | 2.77 sec: 1.04x faster                                                |
| json_loads          | 37.9 us                                                | 41.2 us: 1.09x slower                                                 |
| xml_etree_process   | 83.7 ms                                                | 91.1 ms: 1.09x slower                                                 |
| json_dumps          | 14.3 ms                                                | 17.1 ms: 1.19x slower                                                 |
| Geometric mean      | (ref)                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (3): pickle_pure_python, unpickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 13.7 ms: 1.28x faster                                                 |
| python_startup         | 23.7 ms                                                | 22.4 ms: 1.06x faster                                                 |
| Geometric mean         | (ref)                                                  | 1.17x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 72.2 ms: 1.07x slower                                                 |
| django_template | 44.9 ms                                                | 48.4 ms: 1.08x slower                                                 |
| genshi_text     | 30.2 ms                                                | 33.7 ms: 1.11x slower                                                 |
| mako            | 15.7 ms                                                | 20.7 ms: 1.32x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.14x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 677 ms: 2.86x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 727 ms: 2.54x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 294 ms: 2.40x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 395 ms: 2.36x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 440 ms: 2.22x faster                                                  |
| async_tree_none            | 741 ms                                                 | 348 ms: 2.13x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 2.89 ms: 2.03x faster                                                 |
| mdp                        | 3.97 sec                                               | 2.06 sec: 1.93x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 585 ms: 1.88x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 1.86 ms: 1.87x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 638 ms: 1.69x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 118 ms: 1.44x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 171 ms: 1.41x faster                                                  |
| float                      | 123 ms                                                 | 90.3 ms: 1.36x faster                                                 |
| pathlib                    | 31.6 ms                                                | 24.0 ms: 1.32x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 2.95 us: 1.31x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 3.92 ms: 1.31x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.39 sec: 1.29x faster                                                |
| dulwich_log                | 100 ms                                                 | 78.1 ms: 1.28x faster                                                 |
| python_startup_no_site     | 17.6 ms                                                | 13.7 ms: 1.28x faster                                                 |
| deepcopy                   | 468 us                                                 | 369 us: 1.27x faster                                                  |
| regex_v8                   | 32.5 ms                                                | 26.8 ms: 1.21x faster                                                 |
| 2to3                       | 456 ms                                                 | 384 ms: 1.19x faster                                                  |
| pylint                     | 465 ms                                                 | 400 ms: 1.16x faster                                                  |
| pidigits                   | 250 ms                                                 | 215 ms: 1.16x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 45.2 us: 1.16x faster                                                 |
| spectral_norm              | 156 ms                                                 | 136 ms: 1.14x faster                                                  |
| pyflate                    | 727 ms                                                 | 645 ms: 1.13x faster                                                  |
| regex_dna                  | 278 ms                                                 | 249 ms: 1.12x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 674 ms: 1.11x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.62 sec: 1.10x faster                                                |
| async_generators           | 589 ms                                                 | 538 ms: 1.10x faster                                                  |
| comprehensions             | 27.1 us                                                | 24.9 us: 1.09x faster                                                 |
| html5lib                   | 88.9 ms                                                | 82.0 ms: 1.08x faster                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 6.07 sec: 1.08x faster                                                |
| go                         | 172 ms                                                 | 161 ms: 1.07x faster                                                  |
| raytrace                   | 408 ms                                                 | 383 ms: 1.07x faster                                                  |
| scimark_sor                | 167 ms                                                 | 157 ms: 1.06x faster                                                  |
| python_startup             | 23.7 ms                                                | 22.4 ms: 1.06x faster                                                 |
| deepcopy_reduce            | 4.04 us                                                | 3.81 us: 1.06x faster                                                 |
| nqueens                    | 117 ms                                                 | 111 ms: 1.05x faster                                                  |
| chaos                      | 84.9 ms                                                | 80.8 ms: 1.05x faster                                                 |
| regex_compile              | 187 ms                                                 | 178 ms: 1.05x faster                                                  |
| scimark_fft                | 500 ms                                                 | 480 ms: 1.04x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.77 sec: 1.04x faster                                                |
| json                       | 6.85 ms                                                | 7.06 ms: 1.03x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 111 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.00 sec: 1.03x slower                                                |
| deltablue                  | 4.27 ms                                                | 4.42 ms: 1.04x slower                                                 |
| thrift                     | 1.06 ms                                                | 1.10 ms: 1.04x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 2.07 sec: 1.05x slower                                                |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.08 ms: 1.06x slower                                                 |
| hexiom                     | 8.27 ms                                                | 8.78 ms: 1.06x slower                                                 |
| genshi_xml                 | 67.6 ms                                                | 72.2 ms: 1.07x slower                                                 |
| richards                   | 60.3 ms                                                | 64.6 ms: 1.07x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 163 ms: 1.07x slower                                                  |
| meteor_contest             | 146 ms                                                 | 157 ms: 1.08x slower                                                  |
| django_template            | 44.9 ms                                                | 48.4 ms: 1.08x slower                                                 |
| logging_format             | 9.59 us                                                | 10.4 us: 1.08x slower                                                 |
| json_loads                 | 37.9 us                                                | 41.2 us: 1.09x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 91.1 ms: 1.09x slower                                                 |
| telco                      | 9.59 ms                                                | 10.5 ms: 1.10x slower                                                 |
| sympy_expand               | 582 ms                                                 | 644 ms: 1.11x slower                                                  |
| genshi_text                | 30.2 ms                                                | 33.7 ms: 1.11x slower                                                 |
| fannkuch                   | 540 ms                                                 | 604 ms: 1.12x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 251 us: 1.12x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.19 ms: 1.13x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 17.1 ms: 1.19x slower                                                 |
| nbody                      | 119 ms                                                 | 154 ms: 1.29x slower                                                  |
| mako                       | 15.7 ms                                                | 20.7 ms: 1.32x slower                                                 |
| coverage                   | 95.4 ms                                                | 142 ms: 1.49x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 74.3 ms: 3.59x slower                                                 |
| logging_silent             | 139 ns                                                 | 697 ns: 5.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                          |

Benchmark hidden because not significant (11): sympy_integrate, pickle_pure_python, sympy_sum, coroutines, unpickle_pure_python, sympy_str, scimark_monte_carlo, logging_simple, generators, xml_etree_generate, richards_super
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 97.48% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.42x