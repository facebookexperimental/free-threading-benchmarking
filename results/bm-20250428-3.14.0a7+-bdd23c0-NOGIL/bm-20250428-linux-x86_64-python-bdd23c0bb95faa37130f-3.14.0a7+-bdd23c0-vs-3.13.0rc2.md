# Results vs. 3.13.0rc2

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: linux-x86_64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.061x faster
- HPT reliability: 60.59%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 409 ms: 1.09x faster                                                   |
| docutils       | 4.01 sec                                                     | 3.86 sec: 1.04x faster                                                 |
| html5lib       | 92.6 ms                                                      | 83.5 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 683 ms: 2.05x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 728 ms: 1.91x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 295 ms: 1.71x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 396 ms: 1.69x faster                                                   |
| async_tree_none            | 572 ms                                                       | 345 ms: 1.66x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 442 ms: 1.60x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 582 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 636 ms: 1.40x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 682 ms: 1.12x faster                                                   |
| async_generators           | 567 ms                                                       | 534 ms: 1.06x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.48x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 91.7 ms: 1.26x faster                                                  |
| pidigits       | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| nbody          | 119 ms                                                       | 147 ms: 1.23x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 26.6 ms: 1.23x faster                                                  |
| regex_effbot   | 4.74 ms                                                      | 3.87 ms: 1.22x faster                                                  |
| regex_dna      | 282 ms                                                       | 255 ms: 1.10x faster                                                   |
| Geometric mean | (ref)                                                        | 1.14x faster                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 123 ms: 1.44x faster                                                   |
| xml_etree_parse     | 231 ms                                                       | 183 ms: 1.26x faster                                                   |
| pickle_pure_python  | 416 us                                                       | 437 us: 1.05x slower                                                   |
| xml_etree_generate  | 122 ms                                                       | 130 ms: 1.06x slower                                                   |
| xml_etree_process   | 85.9 ms                                                      | 91.4 ms: 1.06x slower                                                  |
| json_loads          | 34.3 us                                                      | 41.4 us: 1.21x slower                                                  |
| json_dumps          | 14.1 ms                                                      | 17.1 ms: 1.21x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (2): tomli_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 14.9 ms: 1.03x faster                                                  |
| python_startup         | 22.4 ms                                                      | 24.1 ms: 1.08x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 33.7 ms: 1.06x slower                                                  |
| django_template | 44.3 ms                                                      | 49.0 ms: 1.11x slower                                                  |
| mako            | 15.9 ms                                                      | 21.0 ms: 1.32x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.12x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 683 ms: 2.05x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 728 ms: 1.91x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 295 ms: 1.71x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.36 ms: 1.70x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 396 ms: 1.69x faster                                                   |
| mdp                        | 3.80 sec                                                     | 2.27 sec: 1.67x faster                                                 |
| async_tree_none            | 572 ms                                                       | 345 ms: 1.66x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 442 ms: 1.60x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 582 ms: 1.46x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 123 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 636 ms: 1.40x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 2.90 us: 1.38x faster                                                  |
| deepcopy                   | 498 us                                                       | 371 us: 1.34x faster                                                   |
| float                      | 116 ms                                                       | 91.7 ms: 1.26x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 183 ms: 1.26x faster                                                   |
| regex_v8                   | 32.8 ms                                                      | 26.6 ms: 1.23x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 3.87 ms: 1.22x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.2 ms: 1.19x faster                                                  |
| dulwich_log                | 93.7 ms                                                      | 79.7 ms: 1.18x faster                                                  |
| go                         | 191 ms                                                       | 163 ms: 1.18x faster                                                   |
| pathlib                    | 29.9 ms                                                      | 25.9 ms: 1.16x faster                                                  |
| scimark_sor                | 179 ms                                                       | 156 ms: 1.14x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 682 ms: 1.12x faster                                                   |
| pylint                     | 470 ms                                                       | 421 ms: 1.12x faster                                                   |
| html5lib                   | 92.6 ms                                                      | 83.5 ms: 1.11x faster                                                  |
| regex_dna                  | 282 ms                                                       | 255 ms: 1.10x faster                                                   |
| spectral_norm              | 157 ms                                                       | 142 ms: 1.10x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 45.8 us: 1.10x faster                                                  |
| pycparser                  | 1.57 sec                                                     | 1.44 sec: 1.09x faster                                                 |
| 2to3                       | 445 ms                                                       | 409 ms: 1.09x faster                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 2.71 ms: 1.06x faster                                                  |
| async_generators           | 567 ms                                                       | 534 ms: 1.06x faster                                                   |
| pidigits                   | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.89 us: 1.05x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.86 sec: 1.04x faster                                                 |
| python_startup_no_site     | 15.3 ms                                                      | 14.9 ms: 1.03x faster                                                  |
| pyflate                    | 664 ms                                                       | 651 ms: 1.02x faster                                                   |
| scimark_fft                | 473 ms                                                       | 465 ms: 1.02x faster                                                   |
| richards_super             | 73.2 ms                                                      | 76.4 ms: 1.04x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.03 sec: 1.04x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 437 us: 1.05x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 4.66 ms: 1.05x slower                                                  |
| sympy_str                  | 379 ms                                                       | 400 ms: 1.05x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 222 ms: 1.06x slower                                                   |
| meteor_contest             | 150 ms                                                       | 160 ms: 1.06x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 33.7 ms: 1.06x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 130 ms: 1.06x slower                                                   |
| xml_etree_process          | 85.9 ms                                                      | 91.4 ms: 1.06x slower                                                  |
| python_startup             | 22.4 ms                                                      | 24.1 ms: 1.08x slower                                                  |
| logging_format             | 9.24 us                                                      | 9.98 us: 1.08x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 8.78 ms: 1.08x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.10 sec: 1.08x slower                                                 |
| json                       | 6.51 ms                                                      | 7.06 ms: 1.08x slower                                                  |
| generators                 | 40.0 ms                                                      | 43.4 ms: 1.08x slower                                                  |
| logging_silent             | 130 ns                                                       | 141 ns: 1.09x slower                                                   |
| sympy_expand               | 601 ms                                                       | 652 ms: 1.09x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 245 us: 1.09x slower                                                   |
| fannkuch                   | 547 ms                                                       | 596 ms: 1.09x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 110 ms: 1.09x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 99.2 ms: 1.09x slower                                                  |
| django_template            | 44.3 ms                                                      | 49.0 ms: 1.11x slower                                                  |
| raytrace                   | 344 ms                                                       | 382 ms: 1.11x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.15 sec: 1.14x slower                                                 |
| comprehensions             | 22.2 us                                                      | 25.4 us: 1.14x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 168 ms: 1.15x slower                                                   |
| json_loads                 | 34.3 us                                                      | 41.4 us: 1.21x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 17.1 ms: 1.21x slower                                                  |
| nbody                      | 119 ms                                                       | 147 ms: 1.23x slower                                                   |
| mako                       | 15.9 ms                                                      | 21.0 ms: 1.32x slower                                                  |
| coverage                   | 107 ms                                                       | 146 ms: 1.36x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 76.1 ms: 4.07x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (13): chaos, coroutines, sympy_integrate, tomli_loads, regex_compile, scimark_sparse_mat_mult, create_gc_cycles, nqueens, thrift, unpickle_pure_python, genshi_xml, richards, logging_simple
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.061x faster

# HPT report

- Reliability score: 60.59% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x