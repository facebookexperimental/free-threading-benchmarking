# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.076x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 487 ms: 1.09x slower                                                   |
| docutils       | 4.01 sec                                                     | 3.52 sec: 1.14x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 363 ms: 1.58x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 910 ms: 1.53x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 942 ms: 1.49x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 489 ms: 1.37x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 521 ms: 1.36x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 375 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 716 ms: 1.24x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 27.2 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 782 ms: 1.09x faster                                                   |
| async_generators           | 567 ms                                                       | 542 ms: 1.05x faster                                                   |
| asyncio_tcp                | 948 ms                                                       | 906 ms: 1.05x faster                                                   |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 2.86 sec: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 107 ms: 1.08x faster                                                   |
| nbody          | 119 ms                                                       | 114 ms: 1.04x faster                                                   |
| pidigits       | 251 ms                                                       | 274 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 28.9 ms: 1.13x faster                                                  |
| regex_effbot   | 4.74 ms                                                      | 4.21 ms: 1.13x faster                                                  |
| regex_compile  | 182 ms                                                       | 165 ms: 1.10x faster                                                   |
| regex_dna      | 282 ms                                                       | 266 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                        | 1.10x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 154 ms: 1.15x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.50 sec: 1.11x faster                                                 |
| unpickle_list       | 6.68 us                                                      | 6.24 us: 1.07x faster                                                  |
| unpickle            | 20.5 us                                                      | 19.3 us: 1.06x faster                                                  |
| pickle_dict         | 47.2 us                                                      | 44.9 us: 1.05x faster                                                  |
| json_loads          | 34.3 us                                                      | 36.6 us: 1.07x slower                                                  |
| pickle_list         | 6.86 us                                                      | 7.37 us: 1.07x slower                                                  |
| pickle              | 15.1 us                                                      | 18.4 us: 1.22x slower                                                  |
| json_dumps          | 14.1 ms                                                      | 17.4 ms: 1.23x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (5): xml_etree_process, xml_etree_parse, unpickle_pure_python, pickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.4 ms: 1.26x slower                                                  |
| python_startup         | 22.4 ms                                                      | 32.5 ms: 1.45x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 27.9 ms: 1.13x faster                                                  |
| django_template | 44.3 ms                                                      | 47.5 ms: 1.07x slower                                                  |
| mako            | 15.9 ms                                                      | 18.5 ms: 1.16x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 363 ms: 1.58x faster                                                   |
| deepcopy                   | 498 us                                                       | 319 us: 1.56x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 910 ms: 1.53x faster                                                   |
| spectral_norm              | 157 ms                                                       | 105 ms: 1.49x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 942 ms: 1.49x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 489 ms: 1.37x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 521 ms: 1.36x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 375 ms: 1.34x faster                                                   |
| telco                      | 12.2 ms                                                      | 9.47 ms: 1.29x faster                                                  |
| scimark_sor                | 179 ms                                                       | 141 ms: 1.27x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 40.2 us: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 716 ms: 1.24x faster                                                   |
| richards                   | 65.5 ms                                                      | 53.3 ms: 1.23x faster                                                  |
| scimark_fft                | 473 ms                                                       | 390 ms: 1.21x faster                                                   |
| pylint                     | 470 ms                                                       | 396 ms: 1.19x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 5.73 ms: 1.18x faster                                                  |
| go                         | 191 ms                                                       | 163 ms: 1.18x faster                                                   |
| pyflate                    | 664 ms                                                       | 570 ms: 1.16x faster                                                   |
| richards_super             | 73.2 ms                                                      | 63.0 ms: 1.16x faster                                                  |
| deltablue                  | 4.44 ms                                                      | 3.82 ms: 1.16x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 154 ms: 1.15x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.52 sec: 1.14x faster                                                 |
| coroutines                 | 30.9 ms                                                      | 27.2 ms: 1.14x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 27.9 ms: 1.13x faster                                                  |
| regex_v8                   | 32.8 ms                                                      | 28.9 ms: 1.13x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.21 ms: 1.13x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.65 us: 1.12x faster                                                  |
| thrift                     | 1.10 ms                                                      | 983 us: 1.12x faster                                                   |
| comprehensions             | 22.2 us                                                      | 19.9 us: 1.12x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 202 us: 1.12x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.50 sec: 1.11x faster                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 5.65 sec: 1.11x faster                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 81.9 ms: 1.11x faster                                                  |
| sympy_str                  | 379 ms                                                       | 344 ms: 1.10x faster                                                   |
| regex_compile              | 182 ms                                                       | 165 ms: 1.10x faster                                                   |
| crypto_pyaes               | 100 ms                                                       | 91.2 ms: 1.10x faster                                                  |
| dulwich_log                | 93.7 ms                                                      | 85.7 ms: 1.09x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 782 ms: 1.09x faster                                                   |
| float                      | 116 ms                                                       | 107 ms: 1.08x faster                                                   |
| hexiom                     | 8.11 ms                                                      | 7.55 ms: 1.07x faster                                                  |
| logging_silent             | 130 ns                                                       | 121 ns: 1.07x faster                                                   |
| unpickle_list              | 6.68 us                                                      | 6.24 us: 1.07x faster                                                  |
| chaos                      | 83.6 ms                                                      | 78.2 ms: 1.07x faster                                                  |
| unpickle                   | 20.5 us                                                      | 19.3 us: 1.06x faster                                                  |
| pycparser                  | 1.57 sec                                                     | 1.48 sec: 1.06x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 28.2 ms: 1.06x faster                                                  |
| regex_dna                  | 282 ms                                                       | 266 ms: 1.06x faster                                                   |
| logging_simple             | 8.56 us                                                      | 8.10 us: 1.06x faster                                                  |
| generators                 | 40.0 ms                                                      | 38.0 ms: 1.05x faster                                                  |
| pickle_dict                | 47.2 us                                                      | 44.9 us: 1.05x faster                                                  |
| async_generators           | 567 ms                                                       | 542 ms: 1.05x faster                                                   |
| asyncio_tcp                | 948 ms                                                       | 906 ms: 1.05x faster                                                   |
| fannkuch                   | 547 ms                                                       | 524 ms: 1.04x faster                                                   |
| nbody                      | 119 ms                                                       | 114 ms: 1.04x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 948 ms: 1.04x faster                                                   |
| coverage                   | 107 ms                                                       | 104 ms: 1.04x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.71 sec: 1.02x faster                                                 |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 2.86 sec: 1.03x slower                                                 |
| json_loads                 | 34.3 us                                                      | 36.6 us: 1.07x slower                                                  |
| django_template            | 44.3 ms                                                      | 47.5 ms: 1.07x slower                                                  |
| pickle_list                | 6.86 us                                                      | 7.37 us: 1.07x slower                                                  |
| pidigits                   | 251 ms                                                       | 274 ms: 1.09x slower                                                   |
| 2to3                       | 445 ms                                                       | 487 ms: 1.09x slower                                                   |
| json                       | 6.51 ms                                                      | 7.38 ms: 1.13x slower                                                  |
| mako                       | 15.9 ms                                                      | 18.5 ms: 1.16x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.45 ms: 1.19x slower                                                  |
| pickle                     | 15.1 us                                                      | 18.4 us: 1.22x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 17.4 ms: 1.23x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 19.4 ms: 1.26x slower                                                  |
| python_startup             | 22.4 ms                                                      | 32.5 ms: 1.45x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 9.28 ms: 1.63x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 4.37 ms: 1.81x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 91.9 ms: 4.92x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (18): sympy_integrate, xml_etree_process, unpack_sequence, sympy_sum, nqueens, meteor_contest, raytrace, scimark_lu, sqlite_synth, asyncio_websockets, genshi_xml, pprint_pformat, xml_etree_parse, unpickle_pure_python, sympy_expand, logging_format, pickle_pure_python, xml_etree_generate
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.076x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x