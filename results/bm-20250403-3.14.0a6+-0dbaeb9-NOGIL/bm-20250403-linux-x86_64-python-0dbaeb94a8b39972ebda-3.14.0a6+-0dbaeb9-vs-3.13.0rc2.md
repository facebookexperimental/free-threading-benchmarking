# Results vs. 3.13.0rc2

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: linux-x86_64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.023x slower
- HPT reliability: 94.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 527 ms: 1.18x slower                                                   |
| html5lib       | 92.6 ms                                                      | 105 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                        | 1.11x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 710 ms: 1.97x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 789 ms: 1.76x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 319 ms: 1.58x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 431 ms: 1.56x faster                                                   |
| async_tree_none            | 572 ms                                                       | 383 ms: 1.49x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 475 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 646 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 691 ms: 1.29x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 731 ms: 1.05x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 35.2 ms: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.36x faster                                                           |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 96.0 ms: 1.21x faster                                                  |
| nbody          | 119 ms                                                       | 159 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 29.6 ms: 1.11x faster                                                  |
| regex_effbot   | 4.74 ms                                                      | 4.39 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.87 sec: 1.03x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 302 us: 1.04x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 95.0 ms: 1.11x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 140 ms: 1.14x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 17.0 ms: 1.21x slower                                                  |
| json_loads           | 34.3 us                                                      | 47.4 us: 1.38x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 26.2 ms: 1.71x slower                                                  |
| python_startup         | 22.4 ms                                                      | 40.9 ms: 1.83x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.77x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.3 ms                                                      | 50.5 ms: 1.14x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 83.9 ms: 1.16x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 41.3 ms: 1.31x slower                                                  |
| mako            | 15.9 ms                                                      | 25.7 ms: 1.61x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 710 ms: 1.97x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 789 ms: 1.76x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 319 ms: 1.58x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 431 ms: 1.56x faster                                                   |
| mdp                        | 3.80 sec                                                     | 2.46 sec: 1.54x faster                                                 |
| async_tree_none            | 572 ms                                                       | 383 ms: 1.49x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 475 ms: 1.49x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 4.15 ms: 1.37x faster                                                  |
| deepcopy                   | 498 us                                                       | 368 us: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 646 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 691 ms: 1.29x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| float                      | 116 ms                                                       | 96.0 ms: 1.21x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 42.8 us: 1.17x faster                                                  |
| go                         | 191 ms                                                       | 168 ms: 1.13x faster                                                   |
| regex_v8                   | 32.8 ms                                                      | 29.6 ms: 1.11x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.62 us: 1.10x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.39 ms: 1.08x faster                                                  |
| scimark_sor                | 179 ms                                                       | 168 ms: 1.06x faster                                                   |
| spectral_norm              | 157 ms                                                       | 148 ms: 1.06x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 731 ms: 1.05x faster                                                   |
| pycparser                  | 1.57 sec                                                     | 1.52 sec: 1.03x faster                                                 |
| tomli_loads                | 2.78 sec                                                     | 2.87 sec: 1.03x slower                                                 |
| scimark_fft                | 473 ms                                                       | 488 ms: 1.03x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.03 sec: 1.04x slower                                                 |
| richards_super             | 73.2 ms                                                      | 76.2 ms: 1.04x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 302 us: 1.04x slower                                                   |
| nqueens                    | 112 ms                                                       | 119 ms: 1.06x slower                                                   |
| chaos                      | 83.6 ms                                                      | 91.0 ms: 1.09x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 4.84 ms: 1.09x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 95.0 ms: 1.11x slower                                                  |
| generators                 | 40.0 ms                                                      | 44.3 ms: 1.11x slower                                                  |
| json                       | 6.51 ms                                                      | 7.22 ms: 1.11x slower                                                  |
| pyflate                    | 664 ms                                                       | 737 ms: 1.11x slower                                                   |
| html5lib                   | 92.6 ms                                                      | 105 ms: 1.14x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.21 sec: 1.14x slower                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.70 ms: 1.14x slower                                                  |
| django_template            | 44.3 ms                                                      | 50.5 ms: 1.14x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 140 ms: 1.14x slower                                                   |
| coroutines                 | 30.9 ms                                                      | 35.2 ms: 1.14x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 34.6 ms: 1.14x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 259 us: 1.15x slower                                                   |
| sympy_expand               | 601 ms                                                       | 689 ms: 1.15x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 105 ms: 1.16x slower                                                   |
| fannkuch                   | 547 ms                                                       | 636 ms: 1.16x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 83.9 ms: 1.16x slower                                                  |
| raytrace                   | 344 ms                                                       | 403 ms: 1.17x slower                                                   |
| logging_simple             | 8.56 us                                                      | 10.0 us: 1.17x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 248 ms: 1.18x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 173 ms: 1.18x slower                                                   |
| 2to3                       | 445 ms                                                       | 527 ms: 1.18x slower                                                   |
| logging_format             | 9.24 us                                                      | 11.1 us: 1.21x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 17.0 ms: 1.21x slower                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 7.61 sec: 1.21x slower                                                 |
| hexiom                     | 8.11 ms                                                      | 9.86 ms: 1.22x slower                                                  |
| sympy_str                  | 379 ms                                                       | 466 ms: 1.23x slower                                                   |
| meteor_contest             | 150 ms                                                       | 185 ms: 1.23x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 2.97 ms: 1.23x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 116 ms: 1.24x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 41.3 ms: 1.31x slower                                                  |
| comprehensions             | 22.2 us                                                      | 29.1 us: 1.31x slower                                                  |
| nbody                      | 119 ms                                                       | 159 ms: 1.34x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 138 ms: 1.38x slower                                                   |
| json_loads                 | 34.3 us                                                      | 47.4 us: 1.38x slower                                                  |
| coverage                   | 107 ms                                                       | 158 ms: 1.47x slower                                                   |
| mako                       | 15.9 ms                                                      | 25.7 ms: 1.61x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 26.2 ms: 1.71x slower                                                  |
| python_startup             | 22.4 ms                                                      | 40.9 ms: 1.83x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 5.34 ms: 1.85x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 94.3 ms: 5.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (13): telco, xml_etree_parse, pylint, pidigits, pathlib, richards, regex_compile, regex_dna, async_generators, docutils, logging_silent, pickle_pure_python, deepcopy_reduce
Ignored benchmarks (19) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.023x slower

# HPT report

- Reliability score: 94.50% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x