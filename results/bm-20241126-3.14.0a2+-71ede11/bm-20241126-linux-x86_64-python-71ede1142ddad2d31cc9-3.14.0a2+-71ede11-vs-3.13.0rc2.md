# Results vs. 3.13.0rc2

- fork: python
- ref: 71ede1142ddad2d31cc9
- machine: linux-x86_64
- commit hash: 71ede11
- commit date: 2024-11-26
- overall geometric mean: 1.022x faster
- HPT reliability: 99.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.76 sec: 1.07x faster                                                 |
| html5lib       | 92.6 ms                                                      | 84.0 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|---------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none           | 572 ms                                                       | 493 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 804 ms: 1.11x faster                                                   |
| async_tree_memoization    | 709 ms                                                       | 652 ms: 1.09x faster                                                   |
| async_tree_memoization_tg | 670 ms                                                       | 617 ms: 1.09x faster                                                   |
| Geometric mean            | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (7): asyncio_websockets, async_generators, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg, async_tree_io_tg, coroutines

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.32 ms: 1.10x faster                                                  |
| regex_compile  | 182 ms                                                       | 172 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 231 ms                                                       | 199 ms: 1.16x faster                                                   |
| xml_etree_iterparse | 177 ms                                                       | 155 ms: 1.15x faster                                                   |
| xml_etree_generate  | 122 ms                                                       | 116 ms: 1.05x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.65 sec: 1.05x faster                                                 |
| xml_etree_process   | 85.9 ms                                                      | 82.3 ms: 1.04x faster                                                  |
| json_dumps          | 14.1 ms                                                      | 14.7 ms: 1.04x slower                                                  |
| pickle_pure_python  | 416 us                                                       | 435 us: 1.04x slower                                                   |
| Geometric mean      | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (2): unpickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 27.9 ms: 1.25x slower                                                  |
| Geometric mean | (ref)                                                        | 1.12x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 65.8 ms: 1.10x faster                                                  |
| django_template | 44.3 ms                                                      | 46.4 ms: 1.05x slower                                                  |
| mako            | 15.9 ms                                                      | 17.2 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|---------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                  | 498 us                                                       | 337 us: 1.48x faster                                                   |
| go                        | 191 ms                                                       | 152 ms: 1.26x faster                                                   |
| deepcopy_memo             | 50.1 us                                                      | 39.8 us: 1.26x faster                                                  |
| pylint                    | 470 ms                                                       | 376 ms: 1.25x faster                                                   |
| telco                     | 12.2 ms                                                      | 10.0 ms: 1.21x faster                                                  |
| async_tree_none           | 572 ms                                                       | 493 ms: 1.16x faster                                                   |
| xml_etree_parse           | 231 ms                                                       | 199 ms: 1.16x faster                                                   |
| deepcopy_reduce           | 4.10 us                                                      | 3.56 us: 1.15x faster                                                  |
| xml_etree_iterparse       | 177 ms                                                       | 155 ms: 1.15x faster                                                   |
| scimark_sor               | 179 ms                                                       | 157 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 804 ms: 1.11x faster                                                   |
| html5lib                  | 92.6 ms                                                      | 84.0 ms: 1.10x faster                                                  |
| regex_effbot              | 4.74 ms                                                      | 4.32 ms: 1.10x faster                                                  |
| genshi_xml                | 72.1 ms                                                      | 65.8 ms: 1.10x faster                                                  |
| richards                  | 65.5 ms                                                      | 59.9 ms: 1.09x faster                                                  |
| async_tree_memoization    | 709 ms                                                       | 652 ms: 1.09x faster                                                   |
| async_tree_memoization_tg | 670 ms                                                       | 617 ms: 1.09x faster                                                   |
| sympy_str                 | 379 ms                                                       | 350 ms: 1.08x faster                                                   |
| logging_simple            | 8.56 us                                                      | 7.96 us: 1.08x faster                                                  |
| docutils                  | 4.01 sec                                                     | 3.76 sec: 1.07x faster                                                 |
| mdp                       | 3.80 sec                                                     | 3.58 sec: 1.06x faster                                                 |
| regex_compile             | 182 ms                                                       | 172 ms: 1.06x faster                                                   |
| xml_etree_generate        | 122 ms                                                       | 116 ms: 1.05x faster                                                   |
| pprint_pformat            | 1.94 sec                                                     | 1.85 sec: 1.05x faster                                                 |
| tomli_loads               | 2.78 sec                                                     | 2.65 sec: 1.05x faster                                                 |
| fannkuch                  | 547 ms                                                       | 522 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult   | 6.76 ms                                                      | 6.46 ms: 1.05x faster                                                  |
| xml_etree_process         | 85.9 ms                                                      | 82.3 ms: 1.04x faster                                                  |
| sqlite_synth              | 3.99 us                                                      | 3.83 us: 1.04x faster                                                  |
| richards_super            | 73.2 ms                                                      | 70.5 ms: 1.04x faster                                                  |
| logging_silent            | 130 ns                                                       | 135 ns: 1.04x slower                                                   |
| coverage                  | 107 ms                                                       | 112 ms: 1.04x slower                                                   |
| json_dumps                | 14.1 ms                                                      | 14.7 ms: 1.04x slower                                                  |
| pickle_pure_python        | 416 us                                                       | 435 us: 1.04x slower                                                   |
| django_template           | 44.3 ms                                                      | 46.4 ms: 1.05x slower                                                  |
| pycparser                 | 1.57 sec                                                     | 1.67 sec: 1.06x slower                                                 |
| mako                      | 15.9 ms                                                      | 17.2 ms: 1.08x slower                                                  |
| scimark_lu                | 146 ms                                                       | 161 ms: 1.10x slower                                                   |
| dulwich_log               | 93.7 ms                                                      | 104 ms: 1.11x slower                                                   |
| bench_thread_pool         | 2.89 ms                                                      | 3.53 ms: 1.22x slower                                                  |
| python_startup            | 22.4 ms                                                      | 27.9 ms: 1.25x slower                                                  |
| gc_traversal              | 5.70 ms                                                      | 7.58 ms: 1.33x slower                                                  |
| create_gc_cycles          | 2.41 ms                                                      | 3.96 ms: 1.64x slower                                                  |
| bench_mp_pool             | 18.7 ms                                                      | 90.5 ms: 4.84x slower                                                  |
| Geometric mean            | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (44): sympy_sum, pathlib, spectral_norm, typing_runtime_protocols, sympy_integrate, scimark_monte_carlo, genshi_text, asyncio_websockets, sqlglot_parse, sympy_expand, comprehensions, unpickle_pure_python, json, sqlglot_optimize, logging_format, async_generators, deltablue, pprint_safe_repr, nbody, async_tree_cpu_io_mixed_tg, json_loads, crypto_pyaes, scimark_fft, bpe_tokeniser, float, thrift, async_tree_io, pyflate, python_startup_no_site, meteor_contest, regex_v8, pidigits, async_tree_none_tg, chaos, async_tree_io_tg, generators, regex_dna, sqlglot_transpile, hexiom, sqlglot_normalize, raytrace, coroutines, nqueens, 2to3
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 99.67% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x