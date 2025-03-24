# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.095x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.70 sec: 1.08x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 863 ms: 1.61x faster                                                   |
| async_tree_none            | 572 ms                                                       | 360 ms: 1.59x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 889 ms: 1.58x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 471 ms: 1.51x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 460 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 354 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 645 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 695 ms: 1.28x faster                                                   |
| async_generators           | 567 ms                                                       | 518 ms: 1.10x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 705 ms: 1.09x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 29.4 ms: 1.05x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 89.9 ms: 1.29x faster                                                  |
| nbody          | 119 ms                                                       | 111 ms: 1.07x faster                                                   |
| pidigits       | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                        | 1.14x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 171 ms: 1.07x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 30.8 ms: 1.06x faster                                                  |
| regex_effbot   | 4.74 ms                                                      | 4.50 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 136 ms: 1.31x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 193 ms: 1.20x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.39 sec: 1.16x faster                                                 |
| pickle_dict          | 47.2 us                                                      | 41.0 us: 1.15x faster                                                  |
| pickle_list          | 6.86 us                                                      | 6.11 us: 1.12x faster                                                  |
| xml_etree_process    | 85.9 ms                                                      | 76.6 ms: 1.12x faster                                                  |
| xml_etree_generate   | 122 ms                                                       | 116 ms: 1.06x faster                                                   |
| unpickle_pure_python | 290 us                                                       | 281 us: 1.03x faster                                                   |
| json_dumps           | 14.1 ms                                                      | 14.9 ms: 1.05x slower                                                  |
| unpickle_list        | 6.68 us                                                      | 7.32 us: 1.10x slower                                                  |
| json_loads           | 34.3 us                                                      | 37.8 us: 1.10x slower                                                  |
| pickle               | 15.1 us                                                      | 17.2 us: 1.14x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (2): unpickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 16.7 ms: 1.09x slower                                                  |
| python_startup         | 22.4 ms                                                      | 28.1 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 28.3 ms: 1.12x faster                                                  |
| django_template | 44.3 ms                                                      | 46.1 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 863 ms: 1.61x faster                                                   |
| async_tree_none            | 572 ms                                                       | 360 ms: 1.59x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 889 ms: 1.58x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 471 ms: 1.51x faster                                                   |
| deepcopy                   | 498 us                                                       | 334 us: 1.49x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 460 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 354 ms: 1.42x faster                                                   |
| richards                   | 65.5 ms                                                      | 47.2 ms: 1.39x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 37.8 us: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 645 ms: 1.32x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 136 ms: 1.31x faster                                                   |
| float                      | 116 ms                                                       | 89.9 ms: 1.29x faster                                                  |
| spectral_norm              | 157 ms                                                       | 122 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 695 ms: 1.28x faster                                                   |
| scimark_fft                | 473 ms                                                       | 392 ms: 1.21x faster                                                   |
| richards_super             | 73.2 ms                                                      | 61.1 ms: 1.20x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.2 ms: 1.20x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 193 ms: 1.20x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.44 us: 1.19x faster                                                  |
| scimark_sor                | 179 ms                                                       | 151 ms: 1.18x faster                                                   |
| pylint                     | 470 ms                                                       | 403 ms: 1.17x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.39 sec: 1.16x faster                                                 |
| go                         | 191 ms                                                       | 165 ms: 1.16x faster                                                   |
| sympy_integrate            | 30.2 ms                                                      | 26.1 ms: 1.16x faster                                                  |
| deltablue                  | 4.44 ms                                                      | 3.84 ms: 1.16x faster                                                  |
| pickle_dict                | 47.2 us                                                      | 41.0 us: 1.15x faster                                                  |
| dulwich_log                | 93.7 ms                                                      | 82.2 ms: 1.14x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.50 us: 1.14x faster                                                  |
| logging_simple             | 8.56 us                                                      | 7.62 us: 1.12x faster                                                  |
| pickle_list                | 6.86 us                                                      | 6.11 us: 1.12x faster                                                  |
| xml_etree_process          | 85.9 ms                                                      | 76.6 ms: 1.12x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 28.3 ms: 1.12x faster                                                  |
| async_generators           | 567 ms                                                       | 518 ms: 1.10x faster                                                   |
| meteor_contest             | 150 ms                                                       | 138 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.20 ms: 1.09x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 705 ms: 1.09x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 5.78 sec: 1.09x faster                                                 |
| logging_silent             | 130 ns                                                       | 120 ns: 1.08x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.70 sec: 1.08x faster                                                 |
| mdp                        | 3.80 sec                                                     | 3.53 sec: 1.07x faster                                                 |
| chaos                      | 83.6 ms                                                      | 77.8 ms: 1.07x faster                                                  |
| nbody                      | 119 ms                                                       | 111 ms: 1.07x faster                                                   |
| regex_compile              | 182 ms                                                       | 171 ms: 1.07x faster                                                   |
| sympy_str                  | 379 ms                                                       | 355 ms: 1.07x faster                                                   |
| regex_v8                   | 32.8 ms                                                      | 30.8 ms: 1.06x faster                                                  |
| pyflate                    | 664 ms                                                       | 626 ms: 1.06x faster                                                   |
| pidigits                   | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 116 ms: 1.06x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.50 ms: 1.05x faster                                                  |
| fannkuch                   | 547 ms                                                       | 521 ms: 1.05x faster                                                   |
| sympy_sum                  | 210 ms                                                       | 200 ms: 1.05x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 29.4 ms: 1.05x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 95.9 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 957 ms: 1.03x faster                                                   |
| unpickle_pure_python       | 290 us                                                       | 281 us: 1.03x faster                                                   |
| json                       | 6.51 ms                                                      | 6.72 ms: 1.03x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.01 sec: 1.03x slower                                                 |
| comprehensions             | 22.2 us                                                      | 23.0 us: 1.03x slower                                                  |
| django_template            | 44.3 ms                                                      | 46.1 ms: 1.04x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 14.9 ms: 1.05x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 16.7 ms: 1.09x slower                                                  |
| unpickle_list              | 6.68 us                                                      | 7.32 us: 1.10x slower                                                  |
| json_loads                 | 34.3 us                                                      | 37.8 us: 1.10x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.25 ms: 1.13x slower                                                  |
| pickle                     | 15.1 us                                                      | 17.2 us: 1.14x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 9.43 ms: 1.16x slower                                                  |
| python_startup             | 22.4 ms                                                      | 28.1 ms: 1.25x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.00 ms: 1.40x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.62 ms: 1.50x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 93.5 ms: 5.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (21): asyncio_tcp, unpickle, thrift, unpack_sequence, pycparser, pathlib, 2to3, asyncio_tcp_ssl, typing_runtime_protocols, scimark_monte_carlo, coverage, logging_format, mako, regex_dna, nqueens, genshi_xml, sympy_expand, pickle_pure_python, scimark_lu, raytrace, generators
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.095x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x