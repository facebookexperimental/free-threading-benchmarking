# Results vs. 3.12.5+

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 425 ms: 1.07x faster                                                  |
| docutils       | 4.05 sec                                             | 3.95 sec: 1.03x faster                                                |
| tornado_http   | 261 ms                                               | 228 ms: 1.15x faster                                                  |
| Geometric mean | (ref)                                                | 1.08x faster                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 499 ms: 1.64x faster                                                  |
| async_tree_none_tg         | 726 ms                                               | 451 ms: 1.61x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 626 ms: 1.56x faster                                                  |
| async_tree_memoization_tg  | 912 ms                                               | 591 ms: 1.54x faster                                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.22 sec: 1.53x faster                                                |
| async_tree_io              | 1.86 sec                                             | 1.26 sec: 1.48x faster                                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 794 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 806 ms: 1.39x faster                                                  |
| asyncio_tcp                | 988 ms                                               | 928 ms: 1.06x faster                                                  |
| async_generators           | 615 ms                                               | 580 ms: 1.06x faster                                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 2.74 sec: 1.03x faster                                                |
| Geometric mean             | (ref)                                                | 1.31x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 124 ms                                               | 112 ms: 1.11x faster                                                  |
| pidigits       | 256 ms                                               | 243 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                | 1.05x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 186 ms                                               | 174 ms: 1.07x faster                                                  |
| regex_effbot   | 5.02 ms                                              | 4.78 ms: 1.05x faster                                                 |
| regex_dna      | 268 ms                                               | 282 ms: 1.05x slower                                                  |
| regex_v8       | 29.9 ms                                              | 35.8 ms: 1.20x slower                                                 |
| Geometric mean | (ref)                                                | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|---------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_generate  | 138 ms                                               | 117 ms: 1.17x faster                                                  |
| pickle_list         | 7.01 us                                              | 6.33 us: 1.11x faster                                                 |
| xml_etree_iterparse | 173 ms                                               | 158 ms: 1.10x faster                                                  |
| unpickle            | 21.6 us                                              | 19.8 us: 1.09x faster                                                 |
| tomli_loads         | 2.86 sec                                             | 2.66 sec: 1.08x faster                                                |
| xml_etree_parse     | 244 ms                                               | 230 ms: 1.06x faster                                                  |
| pickle_dict         | 45.5 us                                              | 46.8 us: 1.03x slower                                                 |
| unpickle_list       | 6.83 us                                              | 7.22 us: 1.06x slower                                                 |
| json_dumps          | 14.0 ms                                              | 15.5 ms: 1.11x slower                                                 |
| Geometric mean      | (ref)                                                | 1.03x faster                                                          |

Benchmark hidden because not significant (5): xml_etree_process, pickle, pickle_pure_python, unpickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 15.0 ms: 1.08x faster                                                 |
| Geometric mean         | (ref)                                                | 1.05x faster                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|-----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 45.4 ms                                              | 44.0 ms: 1.03x faster                                                 |
| genshi_xml      | 69.1 ms                                              | 73.3 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                | 1.01x slower                                                          |

Benchmark hidden because not significant (2): genshi_text, mako

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 820 ms                                               | 499 ms: 1.64x faster                                                  |
| async_tree_none_tg         | 726 ms                                               | 451 ms: 1.61x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 626 ms: 1.56x faster                                                  |
| async_tree_memoization_tg  | 912 ms                                               | 591 ms: 1.54x faster                                                  |
| async_tree_io_tg           | 1.87 sec                                             | 1.22 sec: 1.53x faster                                                |
| async_tree_io              | 1.86 sec                                             | 1.26 sec: 1.48x faster                                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 794 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 806 ms: 1.39x faster                                                  |
| comprehensions             | 28.6 us                                              | 20.9 us: 1.37x faster                                                 |
| deepcopy_memo              | 51.0 us                                              | 38.4 us: 1.33x faster                                                 |
| deepcopy                   | 486 us                                               | 372 us: 1.31x faster                                                  |
| logging_simple             | 9.68 us                                              | 7.95 us: 1.22x faster                                                 |
| raytrace                   | 405 ms                                               | 338 ms: 1.20x faster                                                  |
| pathlib                    | 31.6 ms                                              | 26.6 ms: 1.19x faster                                                 |
| xml_etree_generate         | 138 ms                                               | 117 ms: 1.17x faster                                                  |
| gc_traversal               | 6.42 ms                                              | 5.48 ms: 1.17x faster                                                 |
| chaos                      | 92.1 ms                                              | 79.1 ms: 1.16x faster                                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 5.99 ms: 1.16x faster                                                 |
| bench_thread_pool          | 3.42 ms                                              | 2.97 ms: 1.15x faster                                                 |
| deepcopy_reduce            | 4.18 us                                              | 3.64 us: 1.15x faster                                                 |
| tornado_http               | 261 ms                                               | 228 ms: 1.15x faster                                                  |
| generators                 | 44.7 ms                                              | 39.3 ms: 1.14x faster                                                 |
| bench_mp_pool              | 21.2 ms                                              | 19.0 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 87.1 ms: 1.11x faster                                                 |
| float                      | 124 ms                                               | 112 ms: 1.11x faster                                                  |
| pickle_list                | 7.01 us                                              | 6.33 us: 1.11x faster                                                 |
| bpe_tokeniser              | 6.76 sec                                             | 6.13 sec: 1.10x faster                                                |
| sympy_str                  | 379 ms                                               | 345 ms: 1.10x faster                                                  |
| crypto_pyaes               | 110 ms                                               | 99.9 ms: 1.10x faster                                                 |
| sqlglot_transpile          | 2.32 ms                                              | 2.12 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 173 ms                                               | 158 ms: 1.10x faster                                                  |
| sqlglot_parse              | 1.85 ms                                              | 1.69 ms: 1.09x faster                                                 |
| logging_silent             | 139 ns                                               | 128 ns: 1.09x faster                                                  |
| unpickle                   | 21.6 us                                              | 19.8 us: 1.09x faster                                                 |
| deltablue                  | 4.45 ms                                              | 4.11 ms: 1.08x faster                                                 |
| python_startup_no_site     | 16.2 ms                                              | 15.0 ms: 1.08x faster                                                 |
| tomli_loads                | 2.86 sec                                             | 2.66 sec: 1.08x faster                                                |
| 2to3                       | 456 ms                                               | 425 ms: 1.07x faster                                                  |
| logging_format             | 9.56 us                                              | 8.93 us: 1.07x faster                                                 |
| regex_compile              | 186 ms                                               | 174 ms: 1.07x faster                                                  |
| asyncio_tcp                | 988 ms                                               | 928 ms: 1.06x faster                                                  |
| json                       | 7.14 ms                                              | 6.72 ms: 1.06x faster                                                 |
| xml_etree_parse            | 244 ms                                               | 230 ms: 1.06x faster                                                  |
| async_generators           | 615 ms                                               | 580 ms: 1.06x faster                                                  |
| meteor_contest             | 146 ms                                               | 138 ms: 1.06x faster                                                  |
| pidigits                   | 256 ms                                               | 243 ms: 1.06x faster                                                  |
| richards_super             | 69.7 ms                                              | 66.2 ms: 1.05x faster                                                 |
| sympy_sum                  | 218 ms                                               | 207 ms: 1.05x faster                                                  |
| regex_effbot               | 5.02 ms                                              | 4.78 ms: 1.05x faster                                                 |
| dask                       | 916 ms                                               | 872 ms: 1.05x faster                                                  |
| mdp                        | 3.77 sec                                             | 3.64 sec: 1.04x faster                                                |
| django_template            | 45.4 ms                                              | 44.0 ms: 1.03x faster                                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 2.74 sec: 1.03x faster                                                |
| docutils                   | 4.05 sec                                             | 3.95 sec: 1.03x faster                                                |
| pickle_dict                | 45.5 us                                              | 46.8 us: 1.03x slower                                                 |
| typing_runtime_protocols   | 224 us                                               | 234 us: 1.05x slower                                                  |
| regex_dna                  | 268 ms                                               | 282 ms: 1.05x slower                                                  |
| unpickle_list              | 6.83 us                                              | 7.22 us: 1.06x slower                                                 |
| genshi_xml                 | 69.1 ms                                              | 73.3 ms: 1.06x slower                                                 |
| go                         | 173 ms                                               | 188 ms: 1.08x slower                                                  |
| sqlite_synth               | 3.77 us                                              | 4.13 us: 1.09x slower                                                 |
| spectral_norm              | 136 ms                                               | 150 ms: 1.10x slower                                                  |
| json_dumps                 | 14.0 ms                                              | 15.5 ms: 1.11x slower                                                 |
| telco                      | 9.53 ms                                              | 10.9 ms: 1.15x slower                                                 |
| create_gc_cycles           | 2.00 ms                                              | 2.32 ms: 1.16x slower                                                 |
| regex_v8                   | 29.9 ms                                              | 35.8 ms: 1.20x slower                                                 |
| coverage                   | 96.9 ms                                              | 118 ms: 1.22x slower                                                  |
| Geometric mean             | (ref)                                                | 1.08x faster                                                          |

Benchmark hidden because not significant (30): html5lib, unpack_sequence, sqlglot_optimize, sympy_integrate, pycparser, python_startup, pprint_pformat, scimark_fft, xml_etree_process, pickle, scimark_sor, pickle_pure_python, pyflate, asyncio_websockets, pylint, genshi_text, scimark_lu, pprint_safe_repr, sympy_expand, thrift, sqlglot_normalize, unpickle_pure_python, richards, mako, nbody, nqueens, fannkuch, coroutines, json_loads, hexiom
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.02x