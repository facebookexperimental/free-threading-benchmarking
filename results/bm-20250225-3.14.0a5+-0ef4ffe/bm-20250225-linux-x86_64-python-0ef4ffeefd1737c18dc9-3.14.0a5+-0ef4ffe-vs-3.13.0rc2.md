# Results vs. 3.13.0rc2

- fork: python
- ref: 0ef4ffeefd1737c18dc9
- machine: linux-x86_64
- commit hash: 0ef4ffe
- commit date: 2025-02-25
- overall geometric mean: 1.063x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 469 ms: 1.05x slower                                                   |
| docutils       | 4.01 sec                                                     | 3.74 sec: 1.07x faster                                                 |
| html5lib       | 92.6 ms                                                      | 83.7 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 885 ms: 1.57x faster                                                   |
| async_tree_none            | 572 ms                                                       | 383 ms: 1.49x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 967 ms: 1.45x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 502 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 485 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 368 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 675 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 667 ms: 1.28x faster                                                   |
| async_generators           | 567 ms                                                       | 507 ms: 1.12x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 103 ms: 1.12x faster                                                   |
| nbody          | 119 ms                                                       | 125 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 164 ms: 1.11x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 37.0 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 231 ms                                                       | 192 ms: 1.20x faster                                                   |
| xml_etree_iterparse | 177 ms                                                       | 150 ms: 1.18x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.51 sec: 1.11x faster                                                 |
| xml_etree_generate  | 122 ms                                                       | 118 ms: 1.04x faster                                                   |
| json_dumps          | 14.1 ms                                                      | 15.2 ms: 1.08x slower                                                  |
| pickle_pure_python  | 416 us                                                       | 475 us: 1.14x slower                                                   |
| json_loads          | 34.3 us                                                      | 40.3 us: 1.17x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_process, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 16.1 ms: 1.05x slower                                                  |
| python_startup         | 22.4 ms                                                      | 27.8 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_xml, genshi_text, mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 885 ms: 1.57x faster                                                   |
| async_tree_none            | 572 ms                                                       | 383 ms: 1.49x faster                                                   |
| deepcopy                   | 498 us                                                       | 341 us: 1.46x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 967 ms: 1.45x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 502 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 485 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 368 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 675 ms: 1.32x faster                                                   |
| spectral_norm              | 157 ms                                                       | 123 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 667 ms: 1.28x faster                                                   |
| go                         | 191 ms                                                       | 156 ms: 1.22x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 192 ms: 1.20x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.2 ms: 1.19x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 150 ms: 1.18x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 43.2 us: 1.16x faster                                                  |
| pylint                     | 470 ms                                                       | 410 ms: 1.15x faster                                                   |
| richards_super             | 73.2 ms                                                      | 64.4 ms: 1.14x faster                                                  |
| chaos                      | 83.6 ms                                                      | 74.1 ms: 1.13x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 201 us: 1.12x faster                                                   |
| float                      | 116 ms                                                       | 103 ms: 1.12x faster                                                   |
| async_generators           | 567 ms                                                       | 507 ms: 1.12x faster                                                   |
| logging_simple             | 8.56 us                                                      | 7.65 us: 1.12x faster                                                  |
| scimark_sor                | 179 ms                                                       | 160 ms: 1.12x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.51 sec: 1.11x faster                                                 |
| pyflate                    | 664 ms                                                       | 599 ms: 1.11x faster                                                   |
| regex_compile              | 182 ms                                                       | 164 ms: 1.11x faster                                                   |
| sympy_integrate            | 30.2 ms                                                      | 27.3 ms: 1.11x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 83.7 ms: 1.11x faster                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 2.00 ms: 1.10x faster                                                  |
| scimark_fft                | 473 ms                                                       | 431 ms: 1.10x faster                                                   |
| thrift                     | 1.10 ms                                                      | 1.00 ms: 1.10x faster                                                  |
| deltablue                  | 4.44 ms                                                      | 4.10 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 84.1 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.86 sec: 1.07x faster                                                 |
| docutils                   | 4.01 sec                                                     | 3.74 sec: 1.07x faster                                                 |
| sympy_sum                  | 210 ms                                                       | 197 ms: 1.07x faster                                                   |
| logging_format             | 9.24 us                                                      | 8.69 us: 1.06x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 94.4 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 931 ms: 1.06x faster                                                   |
| sympy_str                  | 379 ms                                                       | 359 ms: 1.06x faster                                                   |
| nqueens                    | 112 ms                                                       | 106 ms: 1.05x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.62 sec: 1.05x faster                                                 |
| pprint_pformat             | 1.94 sec                                                     | 1.87 sec: 1.04x faster                                                 |
| xml_etree_generate         | 122 ms                                                       | 118 ms: 1.04x faster                                                   |
| fannkuch                   | 547 ms                                                       | 528 ms: 1.04x faster                                                   |
| scimark_lu                 | 146 ms                                                       | 152 ms: 1.04x slower                                                   |
| logging_silent             | 130 ns                                                       | 136 ns: 1.04x slower                                                   |
| nbody                      | 119 ms                                                       | 125 ms: 1.05x slower                                                   |
| 2to3                       | 445 ms                                                       | 469 ms: 1.05x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 16.1 ms: 1.05x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 148 ms: 1.06x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 15.2 ms: 1.08x slower                                                  |
| coverage                   | 107 ms                                                       | 116 ms: 1.08x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.17 ms: 1.10x slower                                                  |
| json                       | 6.51 ms                                                      | 7.15 ms: 1.10x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 105 ms: 1.12x slower                                                   |
| regex_v8                   | 32.8 ms                                                      | 37.0 ms: 1.13x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 475 us: 1.14x slower                                                   |
| json_loads                 | 34.3 us                                                      | 40.3 us: 1.17x slower                                                  |
| python_startup             | 22.4 ms                                                      | 27.8 ms: 1.24x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 7.80 ms: 1.37x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 4.16 ms: 1.72x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 96.3 ms: 5.15x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (25): genshi_xml, richards, coroutines, deepcopy_reduce, xml_etree_process, pidigits, sqlite_synth, sqlglot_parse, sympy_expand, genshi_text, meteor_contest, pycparser, mako, django_template, sqlglot_optimize, scimark_sparse_mat_mult, raytrace, asyncio_websockets, hexiom, generators, pathlib, unpickle_pure_python, comprehensions, regex_dna, regex_effbot
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.063x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.13x