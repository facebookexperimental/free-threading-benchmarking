# Results vs. 3.13.0rc2

- fork: python
- ref: 9211b3dabeacb92713ac
- machine: linux-x86_64
- commit hash: 9211b3d
- commit date: 2025-02-28
- overall geometric mean: 1.076x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.61 sec: 1.11x faster                                                 |
| html5lib       | 92.6 ms                                                      | 84.6 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 869 ms: 1.60x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 882 ms: 1.59x faster                                                   |
| async_tree_none            | 572 ms                                                       | 378 ms: 1.51x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 475 ms: 1.49x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 469 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 361 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 660 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 686 ms: 1.24x faster                                                   |
| async_generators           | 567 ms                                                       | 495 ms: 1.15x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 724 ms: 1.06x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 106 ms: 1.09x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_compile, regex_effbot, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 201 ms: 1.15x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.53 sec: 1.10x faster                                                 |
| xml_etree_generate   | 122 ms                                                       | 115 ms: 1.06x faster                                                   |
| unpickle_pure_python | 290 us                                                       | 281 us: 1.03x faster                                                   |
| json_dumps           | 14.1 ms                                                      | 14.6 ms: 1.03x slower                                                  |
| json_loads           | 34.3 us                                                      | 38.0 us: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 26.0 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 31.7 ms                                                      | 29.2 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (3): genshi_xml, django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 869 ms: 1.60x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 882 ms: 1.59x faster                                                   |
| async_tree_none            | 572 ms                                                       | 378 ms: 1.51x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 475 ms: 1.49x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 469 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 361 ms: 1.40x faster                                                   |
| deepcopy                   | 498 us                                                       | 361 us: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 660 ms: 1.35x faster                                                   |
| go                         | 191 ms                                                       | 147 ms: 1.30x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 39.1 us: 1.28x faster                                                  |
| telco                      | 12.2 ms                                                      | 9.58 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 686 ms: 1.24x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| pylint                     | 470 ms                                                       | 384 ms: 1.23x faster                                                   |
| spectral_norm              | 157 ms                                                       | 129 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.38 us: 1.21x faster                                                  |
| richards                   | 65.5 ms                                                      | 54.1 ms: 1.21x faster                                                  |
| thrift                     | 1.10 ms                                                      | 927 us: 1.19x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 201 ms: 1.15x faster                                                   |
| async_generators           | 567 ms                                                       | 495 ms: 1.15x faster                                                   |
| scimark_sor                | 179 ms                                                       | 156 ms: 1.14x faster                                                   |
| logging_simple             | 8.56 us                                                      | 7.64 us: 1.12x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.61 sec: 1.11x faster                                                 |
| tomli_loads                | 2.78 sec                                                     | 2.53 sec: 1.10x faster                                                 |
| pyflate                    | 664 ms                                                       | 606 ms: 1.09x faster                                                   |
| deltablue                  | 4.44 ms                                                      | 4.06 ms: 1.09x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 84.6 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.74 sec: 1.09x faster                                                 |
| float                      | 116 ms                                                       | 106 ms: 1.09x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.65 us: 1.09x faster                                                  |
| chaos                      | 83.6 ms                                                      | 76.8 ms: 1.09x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 29.2 ms: 1.08x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 916 ms: 1.08x faster                                                   |
| fannkuch                   | 547 ms                                                       | 510 ms: 1.07x faster                                                   |
| typing_runtime_protocols   | 226 us                                                       | 212 us: 1.07x faster                                                   |
| sympy_sum                  | 210 ms                                                       | 198 ms: 1.06x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 115 ms: 1.06x faster                                                   |
| sympy_str                  | 379 ms                                                       | 357 ms: 1.06x faster                                                   |
| hexiom                     | 8.11 ms                                                      | 7.65 ms: 1.06x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 724 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.94 sec                                                     | 1.84 sec: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.39 ms: 1.06x faster                                                  |
| mdp                        | 3.80 sec                                                     | 3.61 sec: 1.05x faster                                                 |
| meteor_contest             | 150 ms                                                       | 144 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 87.4 ms: 1.04x faster                                                  |
| scimark_fft                | 473 ms                                                       | 457 ms: 1.04x faster                                                   |
| unpickle_pure_python       | 290 us                                                       | 281 us: 1.03x faster                                                   |
| pycparser                  | 1.57 sec                                                     | 1.53 sec: 1.03x faster                                                 |
| json_dumps                 | 14.1 ms                                                      | 14.6 ms: 1.03x slower                                                  |
| logging_silent             | 130 ns                                                       | 135 ns: 1.04x slower                                                   |
| generators                 | 40.0 ms                                                      | 42.1 ms: 1.05x slower                                                  |
| raytrace                   | 344 ms                                                       | 369 ms: 1.07x slower                                                   |
| json                       | 6.51 ms                                                      | 7.02 ms: 1.08x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 158 ms: 1.08x slower                                                   |
| json_loads                 | 34.3 us                                                      | 38.0 us: 1.11x slower                                                  |
| python_startup             | 22.4 ms                                                      | 26.0 ms: 1.16x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.85 ms: 1.38x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.69 ms: 1.53x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 94.8 ms: 5.07x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (29): genshi_xml, regex_compile, sympy_integrate, regex_effbot, xml_etree_process, comprehensions, pathlib, pidigits, richards_super, nqueens, django_template, sympy_expand, dulwich_log, pickle_pure_python, logging_format, crypto_pyaes, 2to3, coroutines, python_startup_no_site, sqlglot_optimize, mako, sqlglot_parse, sqlglot_transpile, sqlglot_normalize, regex_dna, nbody, regex_v8, coverage, bench_thread_pool
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.076x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x