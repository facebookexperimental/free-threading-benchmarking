# Results vs. 3.13.0rc2

- fork: python
- ref: cfeaa992ba9bad9be268
- machine: linux-x86_64
- commit hash: cfeaa99
- commit date: 2024-12-16
- overall geometric mean: 1.072x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.63 sec: 1.10x faster                                                 |
| html5lib       | 92.6 ms                                                      | 83.6 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 869 ms: 1.61x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 877 ms: 1.58x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 460 ms: 1.46x faster                                                   |
| async_tree_none            | 572 ms                                                       | 401 ms: 1.43x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 516 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 378 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 673 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 703 ms: 1.26x faster                                                   |
| async_generators           | 567 ms                                                       | 534 ms: 1.06x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 736 ms: 1.04x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 108 ms: 1.07x faster                                                   |
| pidigits       | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 171 ms: 1.07x faster                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (3): regex_effbot, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 146 ms: 1.22x faster                                                   |
| xml_etree_parse     | 231 ms                                                       | 193 ms: 1.19x faster                                                   |
| xml_etree_process   | 85.9 ms                                                      | 78.9 ms: 1.09x faster                                                  |
| tomli_loads         | 2.78 sec                                                     | 2.68 sec: 1.04x faster                                                 |
| json_dumps          | 14.1 ms                                                      | 15.7 ms: 1.11x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_generate, unpickle_pure_python, json_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 14.4 ms: 1.06x faster                                                  |
| python_startup         | 22.4 ms                                                      | 25.6 ms: 1.14x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.04x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 27.6 ms: 1.15x faster                                                  |
| genshi_xml      | 72.1 ms                                                      | 66.6 ms: 1.08x faster                                                  |
| mako            | 15.9 ms                                                      | 16.5 ms: 1.04x slower                                                  |
| django_template | 44.3 ms                                                      | 46.7 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 869 ms: 1.61x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 877 ms: 1.58x faster                                                   |
| deepcopy                   | 498 us                                                       | 324 us: 1.54x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 460 ms: 1.46x faster                                                   |
| async_tree_none            | 572 ms                                                       | 401 ms: 1.43x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 516 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 378 ms: 1.33x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 39.5 us: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 673 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 703 ms: 1.26x faster                                                   |
| go                         | 191 ms                                                       | 154 ms: 1.24x faster                                                   |
| pylint                     | 470 ms                                                       | 386 ms: 1.22x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 146 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.38 us: 1.21x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.2 ms: 1.20x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 193 ms: 1.19x faster                                                   |
| spectral_norm              | 157 ms                                                       | 135 ms: 1.16x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 27.6 ms: 1.15x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 5.91 ms: 1.14x faster                                                  |
| scimark_sor                | 179 ms                                                       | 156 ms: 1.14x faster                                                   |
| logging_simple             | 8.56 us                                                      | 7.52 us: 1.14x faster                                                  |
| pathlib                    | 29.9 ms                                                      | 26.3 ms: 1.14x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 83.6 ms: 1.11x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.63 sec: 1.10x faster                                                 |
| nqueens                    | 112 ms                                                       | 102 ms: 1.10x faster                                                   |
| crypto_pyaes               | 100 ms                                                       | 91.7 ms: 1.09x faster                                                  |
| xml_etree_process          | 85.9 ms                                                      | 78.9 ms: 1.09x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 66.6 ms: 1.08x faster                                                  |
| scimark_fft                | 473 ms                                                       | 440 ms: 1.08x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.85 sec: 1.07x faster                                                 |
| float                      | 116 ms                                                       | 108 ms: 1.07x faster                                                   |
| sympy_sum                  | 210 ms                                                       | 196 ms: 1.07x faster                                                   |
| regex_compile              | 182 ms                                                       | 171 ms: 1.07x faster                                                   |
| async_generators           | 567 ms                                                       | 534 ms: 1.06x faster                                                   |
| sympy_str                  | 379 ms                                                       | 357 ms: 1.06x faster                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 14.4 ms: 1.06x faster                                                  |
| richards                   | 65.5 ms                                                      | 61.7 ms: 1.06x faster                                                  |
| pidigits                   | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| logging_format             | 9.24 us                                                      | 8.75 us: 1.06x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.81 us: 1.05x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 944 ms: 1.05x faster                                                   |
| fannkuch                   | 547 ms                                                       | 524 ms: 1.04x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 736 ms: 1.04x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.68 sec: 1.04x faster                                                 |
| pycparser                  | 1.57 sec                                                     | 1.52 sec: 1.03x faster                                                 |
| mako                       | 15.9 ms                                                      | 16.5 ms: 1.04x slower                                                  |
| generators                 | 40.0 ms                                                      | 41.7 ms: 1.04x slower                                                  |
| django_template            | 44.3 ms                                                      | 46.7 ms: 1.05x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.7 ms: 1.11x slower                                                  |
| python_startup             | 22.4 ms                                                      | 25.6 ms: 1.14x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.52 ms: 1.32x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.31 ms: 1.37x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 89.1 ms: 4.77x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (35): thrift, coroutines, chaos, 2to3, richards_super, meteor_contest, typing_runtime_protocols, sqlglot_parse, scimark_monte_carlo, regex_effbot, deltablue, comprehensions, sympy_integrate, sqlglot_optimize, json, hexiom, bench_thread_pool, regex_dna, pyflate, mdp, xml_etree_generate, scimark_lu, unpickle_pure_python, sqlglot_normalize, json_loads, sympy_expand, dulwich_log, regex_v8, pickle_pure_python, pprint_pformat, coverage, logging_silent, raytrace, sqlglot_transpile, nbody
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.12x