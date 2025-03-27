# Results vs. 3.13.0rc2

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: linux-x86_64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.070x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 469 ms: 1.05x slower                                                   |
| docutils       | 4.01 sec                                                     | 3.58 sec: 1.12x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 357 ms: 1.60x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 893 ms: 1.55x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 922 ms: 1.52x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 491 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 361 ms: 1.40x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 491 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 659 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 647 ms: 1.32x faster                                                   |
| async_generators           | 567 ms                                                       | 519 ms: 1.09x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 105 ms: 1.10x faster                                                   |
| pidigits       | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| nbody          | 119 ms                                                       | 126 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 168 ms: 1.08x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 30.8 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 157 ms: 1.13x faster                                                   |
| xml_etree_parse     | 231 ms                                                       | 207 ms: 1.12x faster                                                   |
| xml_etree_generate  | 122 ms                                                       | 111 ms: 1.10x faster                                                   |
| tomli_loads         | 2.78 sec                                                     | 2.53 sec: 1.10x faster                                                 |
| json_dumps          | 14.1 ms                                                      | 15.4 ms: 1.09x slower                                                  |
| json_loads          | 34.3 us                                                      | 38.7 us: 1.13x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_process, unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 18.0 ms: 1.18x slower                                                  |
| python_startup         | 22.4 ms                                                      | 29.9 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml     | 72.1 ms                                                      | 64.3 ms: 1.12x faster                                                  |
| genshi_text    | 31.7 ms                                                      | 28.6 ms: 1.11x faster                                                  |
| mako           | 15.9 ms                                                      | 16.6 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 572 ms                                                       | 357 ms: 1.60x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 893 ms: 1.55x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 922 ms: 1.52x faster                                                   |
| deepcopy                   | 498 us                                                       | 330 us: 1.51x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 491 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 361 ms: 1.40x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 491 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 659 ms: 1.35x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 37.8 us: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 647 ms: 1.32x faster                                                   |
| go                         | 191 ms                                                       | 155 ms: 1.23x faster                                                   |
| spectral_norm              | 157 ms                                                       | 129 ms: 1.22x faster                                                   |
| scimark_sor                | 179 ms                                                       | 151 ms: 1.18x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.53 us: 1.16x faster                                                  |
| pylint                     | 470 ms                                                       | 415 ms: 1.13x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.7 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 157 ms: 1.13x faster                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.01 ms: 1.12x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 64.3 ms: 1.12x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.58 sec: 1.12x faster                                                 |
| xml_etree_parse            | 231 ms                                                       | 207 ms: 1.12x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 28.6 ms: 1.11x faster                                                  |
| float                      | 116 ms                                                       | 105 ms: 1.10x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 111 ms: 1.10x faster                                                   |
| dulwich_log                | 93.7 ms                                                      | 85.2 ms: 1.10x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.53 sec: 1.10x faster                                                 |
| sympy_integrate            | 30.2 ms                                                      | 27.5 ms: 1.10x faster                                                  |
| async_generators           | 567 ms                                                       | 519 ms: 1.09x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.65 us: 1.09x faster                                                  |
| richards                   | 65.5 ms                                                      | 60.1 ms: 1.09x faster                                                  |
| pathlib                    | 29.9 ms                                                      | 27.6 ms: 1.08x faster                                                  |
| deltablue                  | 4.44 ms                                                      | 4.10 ms: 1.08x faster                                                  |
| regex_compile              | 182 ms                                                       | 168 ms: 1.08x faster                                                   |
| chaos                      | 83.6 ms                                                      | 77.3 ms: 1.08x faster                                                  |
| thrift                     | 1.10 ms                                                      | 1.03 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 922 ms: 1.07x faster                                                   |
| pyflate                    | 664 ms                                                       | 623 ms: 1.07x faster                                                   |
| regex_v8                   | 32.8 ms                                                      | 30.8 ms: 1.06x faster                                                  |
| logging_silent             | 130 ns                                                       | 122 ns: 1.06x faster                                                   |
| mdp                        | 3.80 sec                                                     | 3.57 sec: 1.06x faster                                                 |
| comprehensions             | 22.2 us                                                      | 21.0 us: 1.06x faster                                                  |
| pidigits                   | 251 ms                                                       | 237 ms: 1.06x faster                                                   |
| typing_runtime_protocols   | 226 us                                                       | 214 us: 1.06x faster                                                   |
| sympy_str                  | 379 ms                                                       | 359 ms: 1.05x faster                                                   |
| scimark_fft                | 473 ms                                                       | 449 ms: 1.05x faster                                                   |
| meteor_contest             | 150 ms                                                       | 143 ms: 1.05x faster                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 6.06 sec: 1.04x faster                                                 |
| pprint_pformat             | 1.94 sec                                                     | 1.90 sec: 1.02x faster                                                 |
| mako                       | 15.9 ms                                                      | 16.6 ms: 1.04x slower                                                  |
| 2to3                       | 445 ms                                                       | 469 ms: 1.05x slower                                                   |
| nbody                      | 119 ms                                                       | 126 ms: 1.06x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 156 ms: 1.07x slower                                                   |
| json                       | 6.51 ms                                                      | 6.95 ms: 1.07x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.4 ms: 1.09x slower                                                  |
| json_loads                 | 34.3 us                                                      | 38.7 us: 1.13x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 18.0 ms: 1.18x slower                                                  |
| coverage                   | 107 ms                                                       | 127 ms: 1.18x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.57 ms: 1.24x slower                                                  |
| python_startup             | 22.4 ms                                                      | 29.9 ms: 1.34x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.37 ms: 1.47x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.76 ms: 1.56x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 94.5 ms: 5.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (21): richards_super, logging_simple, nqueens, sympy_sum, xml_etree_process, django_template, asyncio_websockets, regex_effbot, logging_format, fannkuch, scimark_monte_carlo, crypto_pyaes, unpickle_pure_python, hexiom, sympy_expand, pycparser, raytrace, regex_dna, generators, coroutines, pickle_pure_python
Ignored benchmarks (19) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x