# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.101x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 404 ms: 1.10x faster                                                   |
| docutils       | 4.01 sec                                                     | 3.55 sec: 1.13x faster                                                 |
| Geometric mean | (ref)                                                        | 1.12x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 854 ms: 1.62x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 877 ms: 1.60x faster                                                   |
| async_tree_none            | 572 ms                                                       | 369 ms: 1.55x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 461 ms: 1.54x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 440 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 359 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 664 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 665 ms: 1.28x faster                                                   |
| async_generators           | 567 ms                                                       | 479 ms: 1.19x faster                                                   |
| asyncio_tcp                | 948 ms                                                       | 853 ms: 1.11x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 714 ms: 1.07x faster                                                   |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 2.71 sec: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 95.4 ms: 1.21x faster                                                  |
| nbody          | 119 ms                                                       | 129 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 3.99 ms: 1.19x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 30.2 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 139 ms: 1.27x faster                                                   |
| xml_etree_parse     | 231 ms                                                       | 186 ms: 1.24x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.43 sec: 1.14x faster                                                 |
| unpickle            | 20.5 us                                                      | 18.5 us: 1.11x faster                                                  |
| xml_etree_process   | 85.9 ms                                                      | 77.6 ms: 1.11x faster                                                  |
| xml_etree_generate  | 122 ms                                                       | 113 ms: 1.08x faster                                                   |
| pickle_pure_python  | 416 us                                                       | 399 us: 1.04x faster                                                   |
| pickle_list         | 6.86 us                                                      | 6.61 us: 1.04x faster                                                  |
| unpickle_list       | 6.68 us                                                      | 6.88 us: 1.03x slower                                                  |
| json_dumps          | 14.1 ms                                                      | 15.1 ms: 1.07x slower                                                  |
| pickle              | 15.1 us                                                      | 16.4 us: 1.08x slower                                                  |
| json_loads          | 34.3 us                                                      | 38.1 us: 1.11x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (2): pickle_dict, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 17.0 ms: 1.11x slower                                                  |
| python_startup         | 22.4 ms                                                      | 28.8 ms: 1.29x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 31.7 ms                                                      | 27.0 ms: 1.17x faster                                                  |
| genshi_xml     | 72.1 ms                                                      | 63.7 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 854 ms: 1.62x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 877 ms: 1.60x faster                                                   |
| async_tree_none            | 572 ms                                                       | 369 ms: 1.55x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 461 ms: 1.54x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 440 ms: 1.52x faster                                                   |
| deepcopy                   | 498 us                                                       | 330 us: 1.51x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 359 ms: 1.40x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 36.3 us: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 664 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 665 ms: 1.28x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 139 ms: 1.27x faster                                                   |
| spectral_norm              | 157 ms                                                       | 125 ms: 1.25x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 186 ms: 1.24x faster                                                   |
| go                         | 191 ms                                                       | 156 ms: 1.22x faster                                                   |
| float                      | 116 ms                                                       | 95.4 ms: 1.21x faster                                                  |
| pylint                     | 470 ms                                                       | 391 ms: 1.20x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.2 ms: 1.19x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 3.99 ms: 1.19x faster                                                  |
| unpack_sequence            | 74.3 ns                                                      | 62.7 ns: 1.19x faster                                                  |
| async_generators           | 567 ms                                                       | 479 ms: 1.19x faster                                                   |
| scimark_sor                | 179 ms                                                       | 152 ms: 1.18x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 27.0 ms: 1.17x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.43 sec: 1.14x faster                                                 |
| thrift                     | 1.10 ms                                                      | 965 us: 1.14x faster                                                   |
| richards                   | 65.5 ms                                                      | 57.6 ms: 1.14x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 26.6 ms: 1.14x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.52 us: 1.13x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 63.7 ms: 1.13x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.55 sec: 1.13x faster                                                 |
| sympy_str                  | 379 ms                                                       | 338 ms: 1.12x faster                                                   |
| asyncio_tcp                | 948 ms                                                       | 853 ms: 1.11x faster                                                   |
| unpickle                   | 20.5 us                                                      | 18.5 us: 1.11x faster                                                  |
| logging_silent             | 130 ns                                                       | 117 ns: 1.11x faster                                                   |
| xml_etree_process          | 85.9 ms                                                      | 77.6 ms: 1.11x faster                                                  |
| richards_super             | 73.2 ms                                                      | 66.4 ms: 1.10x faster                                                  |
| 2to3                       | 445 ms                                                       | 404 ms: 1.10x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.46 sec: 1.10x faster                                                 |
| deltablue                  | 4.44 ms                                                      | 4.04 ms: 1.10x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.75 us: 1.09x faster                                                  |
| logging_simple             | 8.56 us                                                      | 7.86 us: 1.09x faster                                                  |
| regex_v8                   | 32.8 ms                                                      | 30.2 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.81 sec: 1.08x faster                                                 |
| scimark_fft                | 473 ms                                                       | 438 ms: 1.08x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 113 ms: 1.08x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 714 ms: 1.07x faster                                                   |
| crypto_pyaes               | 100 ms                                                       | 93.4 ms: 1.07x faster                                                  |
| pyflate                    | 664 ms                                                       | 620 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.32 ms: 1.07x faster                                                  |
| comprehensions             | 22.2 us                                                      | 20.9 us: 1.07x faster                                                  |
| chaos                      | 83.6 ms                                                      | 78.6 ms: 1.06x faster                                                  |
| sympy_sum                  | 210 ms                                                       | 198 ms: 1.06x faster                                                   |
| pathlib                    | 29.9 ms                                                      | 28.3 ms: 1.06x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 214 us: 1.06x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 938 ms: 1.05x faster                                                   |
| logging_format             | 9.24 us                                                      | 8.82 us: 1.05x faster                                                  |
| pycparser                  | 1.57 sec                                                     | 1.50 sec: 1.05x faster                                                 |
| dulwich_log                | 93.7 ms                                                      | 89.6 ms: 1.05x faster                                                  |
| nqueens                    | 112 ms                                                       | 107 ms: 1.05x faster                                                   |
| pickle_pure_python         | 416 us                                                       | 399 us: 1.04x faster                                                   |
| sympy_expand               | 601 ms                                                       | 575 ms: 1.04x faster                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 86.9 ms: 1.04x faster                                                  |
| generators                 | 40.0 ms                                                      | 38.4 ms: 1.04x faster                                                  |
| pickle_list                | 6.86 us                                                      | 6.61 us: 1.04x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 1.88 sec: 1.04x faster                                                 |
| fannkuch                   | 547 ms                                                       | 529 ms: 1.03x faster                                                   |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 2.71 sec: 1.02x faster                                                 |
| unpickle_list              | 6.68 us                                                      | 6.88 us: 1.03x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.1 ms: 1.07x slower                                                  |
| nbody                      | 119 ms                                                       | 129 ms: 1.08x slower                                                   |
| pickle                     | 15.1 us                                                      | 16.4 us: 1.08x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 17.0 ms: 1.11x slower                                                  |
| json_loads                 | 34.3 us                                                      | 38.1 us: 1.11x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.26 ms: 1.13x slower                                                  |
| coverage                   | 107 ms                                                       | 122 ms: 1.13x slower                                                   |
| python_startup             | 22.4 ms                                                      | 28.8 ms: 1.29x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.29 ms: 1.37x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.93 ms: 1.39x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 91.4 ms: 4.89x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (13): pidigits, pickle_dict, meteor_contest, regex_dna, regex_compile, raytrace, django_template, unpickle_pure_python, json, scimark_lu, coroutines, mako, hexiom
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.101x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.15x