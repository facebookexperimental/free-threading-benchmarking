# Results vs. 3.13.0rc2

- fork: python
- ref: bca35f0e782848ae2acd
- machine: linux-x86_64
- commit hash: bca35f0
- commit date: 2025-01-20
- overall geometric mean: 1.029x faster
- HPT reliability: 99.33%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 514 ms: 1.16x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.17 sec: 1.04x slower                                                 |
| html5lib       | 92.6 ms                                                      | 81.4 ms: 1.14x faster                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 867 ms: 1.62x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 927 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 387 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 476 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 653 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 398 ms: 1.26x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 563 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 711 ms: 1.25x faster                                                   |
| async_generators           | 567 ms                                                       | 535 ms: 1.06x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 225 ms: 1.11x faster                                                   |
| float          | 116 ms                                                       | 106 ms: 1.09x faster                                                   |
| nbody          | 119 ms                                                       | 126 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 166 ms: 1.09x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 34.3 ms: 1.05x slower                                                  |
| regex_dna      | 282 ms                                                       | 296 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 231 ms                                                       | 188 ms: 1.23x faster                                                   |
| xml_etree_iterparse | 177 ms                                                       | 152 ms: 1.17x faster                                                   |
| xml_etree_generate  | 122 ms                                                       | 112 ms: 1.09x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.58 sec: 1.08x faster                                                 |
| json_dumps          | 14.1 ms                                                      | 15.1 ms: 1.07x slower                                                  |
| json_loads          | 34.3 us                                                      | 39.5 us: 1.15x slower                                                  |
| pickle_pure_python  | 416 us                                                       | 489 us: 1.17x slower                                                   |
| Geometric mean      | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_process, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 17.2 ms: 1.12x slower                                                  |
| python_startup         | 22.4 ms                                                      | 30.7 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 28.8 ms: 1.10x faster                                                  |
| django_template | 44.3 ms                                                      | 50.2 ms: 1.13x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 867 ms: 1.62x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 927 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 387 ms: 1.48x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 476 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 653 ms: 1.31x faster                                                   |
| deepcopy                   | 498 us                                                       | 381 us: 1.31x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 398 ms: 1.26x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 563 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 711 ms: 1.25x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 188 ms: 1.23x faster                                                   |
| richards                   | 65.5 ms                                                      | 54.3 ms: 1.21x faster                                                  |
| go                         | 191 ms                                                       | 163 ms: 1.18x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 152 ms: 1.17x faster                                                   |
| pylint                     | 470 ms                                                       | 405 ms: 1.16x faster                                                   |
| spectral_norm              | 157 ms                                                       | 136 ms: 1.15x faster                                                   |
| html5lib                   | 92.6 ms                                                      | 81.4 ms: 1.14x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.8 ms: 1.13x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 44.4 us: 1.13x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.06 ms: 1.11x faster                                                  |
| pidigits                   | 251 ms                                                       | 225 ms: 1.11x faster                                                   |
| scimark_sor                | 179 ms                                                       | 161 ms: 1.11x faster                                                   |
| pyflate                    | 664 ms                                                       | 604 ms: 1.10x faster                                                   |
| richards_super             | 73.2 ms                                                      | 66.7 ms: 1.10x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 28.8 ms: 1.10x faster                                                  |
| regex_compile              | 182 ms                                                       | 166 ms: 1.09x faster                                                   |
| typing_runtime_protocols   | 226 us                                                       | 206 us: 1.09x faster                                                   |
| float                      | 116 ms                                                       | 106 ms: 1.09x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 112 ms: 1.09x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.80 sec: 1.08x faster                                                 |
| nqueens                    | 112 ms                                                       | 104 ms: 1.08x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.58 sec: 1.08x faster                                                 |
| mdp                        | 3.80 sec                                                     | 3.54 sec: 1.07x faster                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 84.8 ms: 1.07x faster                                                  |
| async_generators           | 567 ms                                                       | 535 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 940 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.94 sec                                                     | 1.89 sec: 1.03x faster                                                 |
| docutils                   | 4.01 sec                                                     | 4.17 sec: 1.04x slower                                                 |
| regex_v8                   | 32.8 ms                                                      | 34.3 ms: 1.05x slower                                                  |
| regex_dna                  | 282 ms                                                       | 296 ms: 1.05x slower                                                   |
| fannkuch                   | 547 ms                                                       | 577 ms: 1.05x slower                                                   |
| pathlib                    | 29.9 ms                                                      | 31.7 ms: 1.06x slower                                                  |
| nbody                      | 119 ms                                                       | 126 ms: 1.06x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 8.64 ms: 1.07x slower                                                  |
| logging_format             | 9.24 us                                                      | 9.85 us: 1.07x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.1 ms: 1.07x slower                                                  |
| pycparser                  | 1.57 sec                                                     | 1.68 sec: 1.07x slower                                                 |
| logging_silent             | 130 ns                                                       | 139 ns: 1.07x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 107 ms: 1.07x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 158 ms: 1.08x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 102 ms: 1.09x slower                                                   |
| meteor_contest             | 150 ms                                                       | 164 ms: 1.09x slower                                                   |
| chaos                      | 83.6 ms                                                      | 92.3 ms: 1.10x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 156 ms: 1.12x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 17.2 ms: 1.12x slower                                                  |
| django_template            | 44.3 ms                                                      | 50.2 ms: 1.13x slower                                                  |
| comprehensions             | 22.2 us                                                      | 25.2 us: 1.13x slower                                                  |
| json_loads                 | 34.3 us                                                      | 39.5 us: 1.15x slower                                                  |
| 2to3                       | 445 ms                                                       | 514 ms: 1.16x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 5.14 ms: 1.16x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 489 us: 1.17x slower                                                   |
| json                       | 6.51 ms                                                      | 7.75 ms: 1.19x slower                                                  |
| coverage                   | 107 ms                                                       | 134 ms: 1.25x slower                                                   |
| python_startup             | 22.4 ms                                                      | 30.7 ms: 1.37x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.96 ms: 1.37x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.92 ms: 1.57x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 4.60 ms: 1.91x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 100 ms: 5.36x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (21): regex_effbot, deepcopy_reduce, xml_etree_process, scimark_fft, asyncio_websockets, genshi_xml, generators, thrift, coroutines, sympy_integrate, logging_simple, raytrace, sympy_expand, sqlglot_transpile, sqlite_synth, mako, sqlglot_optimize, unpickle_pure_python, sqlglot_parse, sympy_sum, sympy_str
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 99.33% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x