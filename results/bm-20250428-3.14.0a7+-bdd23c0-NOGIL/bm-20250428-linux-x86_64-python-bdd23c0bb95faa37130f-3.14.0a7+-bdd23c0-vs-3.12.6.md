# Results vs. 3.12.6

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: linux-x86_64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.103x faster
- HPT reliability: 89.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 409 ms: 1.12x faster                                                   |
| docutils       | 4.00 sec                                               | 3.86 sec: 1.04x faster                                                 |
| html5lib       | 88.9 ms                                                | 83.5 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 683 ms: 2.83x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 728 ms: 2.54x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 295 ms: 2.38x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 396 ms: 2.35x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 442 ms: 2.21x faster                                                   |
| async_tree_none            | 741 ms                                                 | 345 ms: 2.15x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 582 ms: 1.89x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 636 ms: 1.69x faster                                                   |
| async_generators           | 589 ms                                                 | 534 ms: 1.10x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 682 ms: 1.10x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.82x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 91.7 ms: 1.34x faster                                                  |
| pidigits       | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                 | 147 ms: 1.23x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.87 ms: 1.33x faster                                                  |
| regex_v8       | 32.5 ms                                                | 26.6 ms: 1.22x faster                                                  |
| regex_dna      | 278 ms                                                 | 255 ms: 1.09x faster                                                   |
| Geometric mean | (ref)                                                  | 1.16x faster                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 169 ms                                                 | 123 ms: 1.38x faster                                                   |
| xml_etree_parse     | 241 ms                                                 | 183 ms: 1.32x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.76 sec: 1.05x faster                                                 |
| xml_etree_process   | 83.7 ms                                                | 91.4 ms: 1.09x slower                                                  |
| json_loads          | 37.9 us                                                | 41.4 us: 1.09x slower                                                  |
| json_dumps          | 14.3 ms                                                | 17.1 ms: 1.20x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (3): unpickle_pure_python, pickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.9 ms: 1.18x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 73.4 ms: 1.09x slower                                                  |
| django_template | 44.9 ms                                                | 49.0 ms: 1.09x slower                                                  |
| genshi_text     | 30.2 ms                                                | 33.7 ms: 1.11x slower                                                  |
| mako            | 15.7 ms                                                | 21.0 ms: 1.34x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.15x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 683 ms: 2.83x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 728 ms: 2.54x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 295 ms: 2.38x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 396 ms: 2.35x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 442 ms: 2.21x faster                                                   |
| async_tree_none            | 741 ms                                                 | 345 ms: 2.15x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 582 ms: 1.89x faster                                                   |
| mdp                        | 3.97 sec                                               | 2.27 sec: 1.75x faster                                                 |
| gc_traversal               | 5.86 ms                                                | 3.36 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 636 ms: 1.69x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 123 ms: 1.38x faster                                                   |
| float                      | 123 ms                                                 | 91.7 ms: 1.34x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 2.90 us: 1.34x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 3.87 ms: 1.33x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 183 ms: 1.32x faster                                                   |
| bench_thread_pool          | 3.48 ms                                                | 2.71 ms: 1.28x faster                                                  |
| deepcopy                   | 468 us                                                 | 371 us: 1.26x faster                                                   |
| dulwich_log                | 100 ms                                                 | 79.7 ms: 1.26x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.44 sec: 1.24x faster                                                 |
| regex_v8                   | 32.5 ms                                                | 26.6 ms: 1.22x faster                                                  |
| pathlib                    | 31.6 ms                                                | 25.9 ms: 1.22x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 14.9 ms: 1.18x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 45.8 us: 1.15x faster                                                  |
| pyflate                    | 727 ms                                                 | 651 ms: 1.12x faster                                                   |
| 2to3                       | 456 ms                                                 | 409 ms: 1.12x faster                                                   |
| pylint                     | 465 ms                                                 | 421 ms: 1.10x faster                                                   |
| async_generators           | 589 ms                                                 | 534 ms: 1.10x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 682 ms: 1.10x faster                                                   |
| spectral_norm              | 156 ms                                                 | 142 ms: 1.09x faster                                                   |
| regex_dna                  | 278 ms                                                 | 255 ms: 1.09x faster                                                   |
| scimark_fft                | 500 ms                                                 | 465 ms: 1.08x faster                                                   |
| logging_simple             | 9.45 us                                                | 8.82 us: 1.07x faster                                                  |
| comprehensions             | 27.1 us                                                | 25.4 us: 1.07x faster                                                  |
| raytrace                   | 408 ms                                                 | 382 ms: 1.07x faster                                                   |
| html5lib                   | 88.9 ms                                                | 83.5 ms: 1.07x faster                                                  |
| scimark_sor                | 167 ms                                                 | 156 ms: 1.07x faster                                                   |
| go                         | 172 ms                                                 | 163 ms: 1.06x faster                                                   |
| pidigits                   | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.76 sec: 1.05x faster                                                 |
| chaos                      | 84.9 ms                                                | 81.1 ms: 1.05x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.89 us: 1.04x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.86 sec: 1.04x faster                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 99.2 ms: 1.03x slower                                                  |
| json                       | 6.85 ms                                                | 7.06 ms: 1.03x slower                                                  |
| sympy_str                  | 385 ms                                                 | 400 ms: 1.04x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.11 ms: 1.05x slower                                                  |
| richards_super             | 72.8 ms                                                | 76.4 ms: 1.05x slower                                                  |
| generators                 | 41.1 ms                                                | 43.4 ms: 1.05x slower                                                  |
| hexiom                     | 8.27 ms                                                | 8.78 ms: 1.06x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.10 sec: 1.06x slower                                                 |
| pprint_safe_repr           | 967 ms                                                 | 1.03 sec: 1.07x slower                                                 |
| telco                      | 9.59 ms                                                | 10.2 ms: 1.07x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 73.4 ms: 1.09x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.15 sec: 1.09x slower                                                 |
| django_template            | 44.9 ms                                                | 49.0 ms: 1.09x slower                                                  |
| meteor_contest             | 146 ms                                                 | 160 ms: 1.09x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 91.4 ms: 1.09x slower                                                  |
| deltablue                  | 4.27 ms                                                | 4.66 ms: 1.09x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 245 us: 1.09x slower                                                   |
| json_loads                 | 37.9 us                                                | 41.4 us: 1.09x slower                                                  |
| fannkuch                   | 540 ms                                                 | 596 ms: 1.10x slower                                                   |
| richards                   | 60.3 ms                                                | 66.7 ms: 1.11x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 168 ms: 1.11x slower                                                   |
| genshi_text                | 30.2 ms                                                | 33.7 ms: 1.11x slower                                                  |
| sympy_expand               | 582 ms                                                 | 652 ms: 1.12x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 17.1 ms: 1.20x slower                                                  |
| nbody                      | 119 ms                                                 | 147 ms: 1.23x slower                                                   |
| create_gc_cycles           | 1.94 ms                                                | 2.41 ms: 1.24x slower                                                  |
| mako                       | 15.7 ms                                                | 21.0 ms: 1.34x slower                                                  |
| coverage                   | 95.4 ms                                                | 146 ms: 1.53x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 76.1 ms: 3.68x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (13): nqueens, regex_compile, unpickle_pure_python, sympy_sum, sympy_integrate, pickle_pure_python, scimark_sparse_mat_mult, logging_silent, python_startup, crypto_pyaes, xml_etree_generate, coroutines, logging_format
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 89.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.36x