# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.030x slower
- HPT reliability: 99.11%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 506 ms: 1.14x slower                                                   |
| docutils       | 4.01 sec                                                     | 3.91 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 730 ms: 1.92x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 803 ms: 1.73x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 441 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 331 ms: 1.52x faster                                                   |
| async_tree_none            | 572 ms                                                       | 384 ms: 1.49x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 509 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 633 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 679 ms: 1.31x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 712 ms: 1.08x faster                                                   |
| asyncio_tcp                | 948 ms                                                       | 1.02 sec: 1.08x slower                                                 |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.21 sec: 1.16x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmark hidden because not significant (2): coroutines, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 101 ms: 1.14x faster                                                   |
| pidigits       | 251 ms                                                       | 226 ms: 1.11x faster                                                   |
| nbody          | 119 ms                                                       | 167 ms: 1.41x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.37 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (3): regex_dna, regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 137 ms: 1.29x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 207 ms: 1.11x faster                                                   |
| pickle_dict          | 47.2 us                                                      | 43.2 us: 1.09x faster                                                  |
| pickle               | 15.1 us                                                      | 16.1 us: 1.06x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 136 ms: 1.11x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.11 sec: 1.12x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 96.9 ms: 1.13x slower                                                  |
| unpickle             | 20.5 us                                                      | 23.9 us: 1.16x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 16.5 ms: 1.17x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 506 us: 1.21x slower                                                   |
| unpickle_list        | 6.68 us                                                      | 8.15 us: 1.22x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 358 us: 1.23x slower                                                   |
| json_loads           | 34.3 us                                                      | 43.6 us: 1.27x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 29.4 ms: 1.31x slower                                                  |
| python_startup_no_site | 15.3 ms                                                      | 21.4 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 76.8 ms: 1.06x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 36.8 ms: 1.16x slower                                                  |
| django_template | 44.3 ms                                                      | 52.4 ms: 1.18x slower                                                  |
| mako            | 15.9 ms                                                      | 23.1 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.21x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 730 ms: 1.92x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 803 ms: 1.73x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.51 ms: 1.62x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 441 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 331 ms: 1.52x faster                                                   |
| async_tree_none            | 572 ms                                                       | 384 ms: 1.49x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 509 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 633 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 679 ms: 1.31x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 137 ms: 1.29x faster                                                   |
| deepcopy                   | 498 us                                                       | 403 us: 1.24x faster                                                   |
| float                      | 116 ms                                                       | 101 ms: 1.14x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 207 ms: 1.11x faster                                                   |
| pidigits                   | 251 ms                                                       | 226 ms: 1.11x faster                                                   |
| pylint                     | 470 ms                                                       | 428 ms: 1.10x faster                                                   |
| pickle_dict                | 47.2 us                                                      | 43.2 us: 1.09x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.37 ms: 1.08x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 712 ms: 1.08x faster                                                   |
| spectral_norm              | 157 ms                                                       | 147 ms: 1.07x faster                                                   |
| scimark_sor                | 179 ms                                                       | 171 ms: 1.05x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.91 sec: 1.02x faster                                                 |
| mdp                        | 3.80 sec                                                     | 3.92 sec: 1.03x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.27 us: 1.04x slower                                                  |
| unpack_sequence            | 74.3 ns                                                      | 78.0 ns: 1.05x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 31.8 ms: 1.05x slower                                                  |
| chaos                      | 83.6 ms                                                      | 88.0 ms: 1.05x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 2.55 ms: 1.06x slower                                                  |
| pyflate                    | 664 ms                                                       | 704 ms: 1.06x slower                                                   |
| logging_simple             | 8.56 us                                                      | 9.08 us: 1.06x slower                                                  |
| pickle                     | 15.1 us                                                      | 16.1 us: 1.06x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 76.8 ms: 1.06x slower                                                  |
| asyncio_tcp                | 948 ms                                                       | 1.02 sec: 1.08x slower                                                 |
| logging_silent             | 130 ns                                                       | 141 ns: 1.09x slower                                                   |
| richards                   | 65.5 ms                                                      | 71.3 ms: 1.09x slower                                                  |
| generators                 | 40.0 ms                                                      | 43.6 ms: 1.09x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.08 sec: 1.09x slower                                                 |
| meteor_contest             | 150 ms                                                       | 164 ms: 1.09x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 110 ms: 1.10x slower                                                   |
| nqueens                    | 112 ms                                                       | 123 ms: 1.10x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 6.95 sec: 1.11x slower                                                 |
| telco                      | 12.2 ms                                                      | 13.5 ms: 1.11x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 136 ms: 1.11x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.16 sec: 1.11x slower                                                 |
| tomli_loads                | 2.78 sec                                                     | 3.11 sec: 1.12x slower                                                 |
| json                       | 6.51 ms                                                      | 7.31 ms: 1.12x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 96.9 ms: 1.13x slower                                                  |
| 2to3                       | 445 ms                                                       | 506 ms: 1.14x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 241 ms: 1.15x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 9.33 ms: 1.15x slower                                                  |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.21 sec: 1.16x slower                                                 |
| genshi_text                | 31.7 ms                                                      | 36.8 ms: 1.16x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.36 ms: 1.16x slower                                                  |
| sympy_expand               | 601 ms                                                       | 699 ms: 1.16x slower                                                   |
| unpickle                   | 20.5 us                                                      | 23.9 us: 1.16x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.28 ms: 1.17x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 16.5 ms: 1.17x slower                                                  |
| comprehensions             | 22.2 us                                                      | 26.1 us: 1.17x slower                                                  |
| scimark_fft                | 473 ms                                                       | 556 ms: 1.17x slower                                                   |
| richards_super             | 73.2 ms                                                      | 86.6 ms: 1.18x slower                                                  |
| django_template            | 44.3 ms                                                      | 52.4 ms: 1.18x slower                                                  |
| fannkuch                   | 547 ms                                                       | 648 ms: 1.19x slower                                                   |
| sympy_str                  | 379 ms                                                       | 449 ms: 1.19x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 506 us: 1.21x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 5.40 ms: 1.22x slower                                                  |
| unpickle_list              | 6.68 us                                                      | 8.15 us: 1.22x slower                                                  |
| logging_format             | 9.24 us                                                      | 11.3 us: 1.22x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 358 us: 1.23x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 181 ms: 1.24x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 113 ms: 1.24x slower                                                   |
| raytrace                   | 344 ms                                                       | 428 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.47 ms: 1.25x slower                                                  |
| json_loads                 | 34.3 us                                                      | 43.6 us: 1.27x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 289 us: 1.28x slower                                                   |
| python_startup             | 22.4 ms                                                      | 29.4 ms: 1.31x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 21.4 ms: 1.39x slower                                                  |
| nbody                      | 119 ms                                                       | 167 ms: 1.41x slower                                                   |
| mako                       | 15.9 ms                                                      | 23.1 ms: 1.45x slower                                                  |
| coverage                   | 107 ms                                                       | 156 ms: 1.45x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 82.2 ms: 4.40x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x slower                                                           |

Benchmark hidden because not significant (13): coroutines, pathlib, go, pickle_list, deepcopy_memo, sqlite_synth, regex_dna, async_generators, regex_compile, pycparser, dulwich_log, html5lib, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.030x slower

# HPT report

- Reliability score: 99.11% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x