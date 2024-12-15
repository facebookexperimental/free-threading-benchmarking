# Results vs. 3.13.0rc2

- fork: python
- ref: 0ac40acec045c4ce780c
- machine: linux-x86_64
- commit hash: 0ac40ac
- commit date: 2024-12-14
- overall geometric mean: 1.084x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 418 ms: 1.07x faster                                                   |
| docutils       | 4.01 sec                                                     | 3.55 sec: 1.13x faster                                                 |
| html5lib       | 92.6 ms                                                      | 82.9 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.10x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 862 ms: 1.61x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 888 ms: 1.58x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 444 ms: 1.51x faster                                                   |
| async_tree_none            | 572 ms                                                       | 383 ms: 1.49x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 478 ms: 1.49x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 362 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 677 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 670 ms: 1.27x faster                                                   |
| async_generators           | 567 ms                                                       | 543 ms: 1.04x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 109 ms: 1.07x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 163 ms: 1.12x faster                                                   |
| regex_effbot   | 4.74 ms                                                      | 4.29 ms: 1.10x faster                                                  |
| regex_dna      | 282 ms                                                       | 269 ms: 1.05x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 34.8 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 231 ms                                                       | 189 ms: 1.22x faster                                                   |
| xml_etree_iterparse | 177 ms                                                       | 147 ms: 1.20x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.56 sec: 1.09x faster                                                 |
| xml_etree_process   | 85.9 ms                                                      | 80.0 ms: 1.07x faster                                                  |
| xml_etree_generate  | 122 ms                                                       | 115 ms: 1.06x faster                                                   |
| json_dumps          | 14.1 ms                                                      | 15.4 ms: 1.09x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (3): pickle_pure_python, json_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 14.3 ms: 1.07x faster                                                  |
| python_startup         | 22.4 ms                                                      | 24.4 ms: 1.09x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 72.1 ms                                                      | 66.3 ms: 1.09x faster                                                  |
| genshi_text    | 31.7 ms                                                      | 29.6 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 862 ms: 1.61x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 888 ms: 1.58x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 444 ms: 1.51x faster                                                   |
| async_tree_none            | 572 ms                                                       | 383 ms: 1.49x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 478 ms: 1.49x faster                                                   |
| deepcopy                   | 498 us                                                       | 336 us: 1.48x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 362 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 677 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 670 ms: 1.27x faster                                                   |
| go                         | 191 ms                                                       | 153 ms: 1.25x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 189 ms: 1.22x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.0 ms: 1.21x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 147 ms: 1.20x faster                                                   |
| pylint                     | 470 ms                                                       | 398 ms: 1.18x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 42.7 us: 1.18x faster                                                  |
| spectral_norm              | 157 ms                                                       | 134 ms: 1.17x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 5.79 ms: 1.17x faster                                                  |
| pathlib                    | 29.9 ms                                                      | 25.7 ms: 1.16x faster                                                  |
| scimark_sor                | 179 ms                                                       | 154 ms: 1.16x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.55 sec: 1.13x faster                                                 |
| html5lib                   | 92.6 ms                                                      | 82.9 ms: 1.12x faster                                                  |
| regex_compile              | 182 ms                                                       | 163 ms: 1.12x faster                                                   |
| meteor_contest             | 150 ms                                                       | 135 ms: 1.11x faster                                                   |
| richards                   | 65.5 ms                                                      | 59.2 ms: 1.11x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.29 ms: 1.10x faster                                                  |
| deltablue                  | 4.44 ms                                                      | 4.06 ms: 1.09x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.66 us: 1.09x faster                                                  |
| richards_super             | 73.2 ms                                                      | 67.3 ms: 1.09x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 66.3 ms: 1.09x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.56 sec: 1.09x faster                                                 |
| crypto_pyaes               | 100 ms                                                       | 92.5 ms: 1.08x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 28.0 ms: 1.08x faster                                                  |
| fannkuch                   | 547 ms                                                       | 507 ms: 1.08x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.85 sec: 1.07x faster                                                 |
| xml_etree_process          | 85.9 ms                                                      | 80.0 ms: 1.07x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.82 us: 1.07x faster                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 69.7 ms: 1.07x faster                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 14.3 ms: 1.07x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 29.6 ms: 1.07x faster                                                  |
| float                      | 116 ms                                                       | 109 ms: 1.07x faster                                                   |
| 2to3                       | 445 ms                                                       | 418 ms: 1.07x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 115 ms: 1.06x faster                                                   |
| pycparser                  | 1.57 sec                                                     | 1.48 sec: 1.06x faster                                                 |
| logging_simple             | 8.56 us                                                      | 8.08 us: 1.06x faster                                                  |
| nqueens                    | 112 ms                                                       | 106 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 935 ms: 1.06x faster                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.09 ms: 1.05x faster                                                  |
| pyflate                    | 664 ms                                                       | 633 ms: 1.05x faster                                                   |
| regex_dna                  | 282 ms                                                       | 269 ms: 1.05x faster                                                   |
| sympy_expand               | 601 ms                                                       | 574 ms: 1.05x faster                                                   |
| logging_format             | 9.24 us                                                      | 8.84 us: 1.05x faster                                                  |
| async_generators           | 567 ms                                                       | 543 ms: 1.04x faster                                                   |
| comprehensions             | 22.2 us                                                      | 21.3 us: 1.04x faster                                                  |
| generators                 | 40.0 ms                                                      | 38.4 ms: 1.04x faster                                                  |
| scimark_fft                | 473 ms                                                       | 454 ms: 1.04x faster                                                   |
| hexiom                     | 8.11 ms                                                      | 7.85 ms: 1.03x faster                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 87.8 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 1.89 sec: 1.03x faster                                                 |
| logging_silent             | 130 ns                                                       | 138 ns: 1.06x slower                                                   |
| regex_v8                   | 32.8 ms                                                      | 34.8 ms: 1.06x slower                                                  |
| coverage                   | 107 ms                                                       | 117 ms: 1.09x slower                                                   |
| python_startup             | 22.4 ms                                                      | 24.4 ms: 1.09x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.4 ms: 1.09x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.90 ms: 1.39x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.35 ms: 1.39x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 89.8 ms: 4.80x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (22): pidigits, chaos, pickle_pure_python, sympy_sum, thrift, sqlglot_parse, sqlglot_normalize, json, json_loads, mako, mdp, sympy_str, asyncio_websockets, bench_thread_pool, unpickle_pure_python, nbody, scimark_lu, raytrace, django_template, typing_runtime_protocols, dulwich_log, coroutines
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.12x