# Results vs. 3.13.0rc2

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: linux-x86_64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.043x slower
- HPT reliability: 99.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 530 ms: 1.19x slower                                                   |
| html5lib       | 92.6 ms                                                      | 103 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 734 ms: 1.91x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 830 ms: 1.67x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 445 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 389 ms: 1.47x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 487 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 349 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 646 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 730 ms: 1.22x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 743 ms: 1.03x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                           |

Benchmark hidden because not significant (2): async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 103 ms: 1.13x faster                                                   |
| pidigits       | 251 ms                                                       | 239 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                       | 181 ms: 1.53x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 29.8 ms: 1.10x faster                                                  |
| regex_effbot   | 4.74 ms                                                      | 4.38 ms: 1.08x faster                                                  |
| regex_compile  | 182 ms                                                       | 205 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 143 ms: 1.23x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 219 ms: 1.05x faster                                                   |
| xml_etree_generate   | 122 ms                                                       | 130 ms: 1.07x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 310 us: 1.07x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.04 sec: 1.09x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 458 us: 1.10x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 96.0 ms: 1.12x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 17.4 ms: 1.23x slower                                                  |
| json_loads           | 34.3 us                                                      | 44.5 us: 1.30x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 32.3 ms: 1.44x slower                                                  |
| python_startup_no_site | 15.3 ms                                                      | 23.8 ms: 1.55x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.50x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 84.4 ms: 1.17x slower                                                  |
| django_template | 44.3 ms                                                      | 55.6 ms: 1.26x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 41.9 ms: 1.32x slower                                                  |
| mako            | 15.9 ms                                                      | 22.0 ms: 1.38x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.28x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 734 ms: 1.91x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 830 ms: 1.67x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.64 ms: 1.57x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 445 ms: 1.50x faster                                                   |
| async_tree_none            | 572 ms                                                       | 389 ms: 1.47x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 487 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 349 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 646 ms: 1.32x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 143 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 730 ms: 1.22x faster                                                   |
| deepcopy                   | 498 us                                                       | 427 us: 1.17x faster                                                   |
| float                      | 116 ms                                                       | 103 ms: 1.13x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.61 us: 1.10x faster                                                  |
| regex_v8                   | 32.8 ms                                                      | 29.8 ms: 1.10x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.38 ms: 1.08x faster                                                  |
| spectral_norm              | 157 ms                                                       | 146 ms: 1.08x faster                                                   |
| dulwich_log                | 93.7 ms                                                      | 87.7 ms: 1.07x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 219 ms: 1.05x faster                                                   |
| pidigits                   | 251 ms                                                       | 239 ms: 1.05x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 743 ms: 1.03x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 52.5 us: 1.05x slower                                                  |
| richards                   | 65.5 ms                                                      | 69.3 ms: 1.06x slower                                                  |
| scimark_sor                | 179 ms                                                       | 190 ms: 1.06x slower                                                   |
| xml_etree_generate         | 122 ms                                                       | 130 ms: 1.07x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 310 us: 1.07x slower                                                   |
| pathlib                    | 29.9 ms                                                      | 32.2 ms: 1.08x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 2.62 ms: 1.09x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.04 sec: 1.09x slower                                                 |
| mdp                        | 3.80 sec                                                     | 4.16 sec: 1.09x slower                                                 |
| sympy_str                  | 379 ms                                                       | 415 ms: 1.10x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 458 us: 1.10x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.09 sec: 1.10x slower                                                 |
| html5lib                   | 92.6 ms                                                      | 103 ms: 1.11x slower                                                   |
| pyflate                    | 664 ms                                                       | 741 ms: 1.12x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 33.8 ms: 1.12x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 96.0 ms: 1.12x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.23 ms: 1.12x slower                                                  |
| regex_compile              | 182 ms                                                       | 205 ms: 1.13x slower                                                   |
| chaos                      | 83.6 ms                                                      | 94.2 ms: 1.13x slower                                                  |
| scimark_fft                | 473 ms                                                       | 537 ms: 1.13x slower                                                   |
| json                       | 6.51 ms                                                      | 7.39 ms: 1.14x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.22 sec: 1.14x slower                                                 |
| logging_format             | 9.24 us                                                      | 10.6 us: 1.14x slower                                                  |
| nqueens                    | 112 ms                                                       | 128 ms: 1.15x slower                                                   |
| richards_super             | 73.2 ms                                                      | 84.1 ms: 1.15x slower                                                  |
| comprehensions             | 22.2 us                                                      | 25.9 us: 1.17x slower                                                  |
| sympy_expand               | 601 ms                                                       | 702 ms: 1.17x slower                                                   |
| fannkuch                   | 547 ms                                                       | 640 ms: 1.17x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 84.4 ms: 1.17x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 247 ms: 1.17x slower                                                   |
| generators                 | 40.0 ms                                                      | 47.0 ms: 1.18x slower                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 7.42 sec: 1.18x slower                                                 |
| 2to3                       | 445 ms                                                       | 530 ms: 1.19x slower                                                   |
| logging_simple             | 8.56 us                                                      | 10.3 us: 1.20x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 5.33 ms: 1.20x slower                                                  |
| logging_silent             | 130 ns                                                       | 157 ns: 1.20x slower                                                   |
| meteor_contest             | 150 ms                                                       | 181 ms: 1.20x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 273 us: 1.21x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 179 ms: 1.22x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 17.4 ms: 1.23x slower                                                  |
| raytrace                   | 344 ms                                                       | 428 ms: 1.24x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 124 ms: 1.24x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 10.1 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.44 ms: 1.25x slower                                                  |
| django_template            | 44.3 ms                                                      | 55.6 ms: 1.26x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 118 ms: 1.30x slower                                                   |
| json_loads                 | 34.3 us                                                      | 44.5 us: 1.30x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 41.9 ms: 1.32x slower                                                  |
| mako                       | 15.9 ms                                                      | 22.0 ms: 1.38x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.98 ms: 1.38x slower                                                  |
| python_startup             | 22.4 ms                                                      | 32.3 ms: 1.44x slower                                                  |
| coverage                   | 107 ms                                                       | 160 ms: 1.49x slower                                                   |
| nbody                      | 119 ms                                                       | 181 ms: 1.53x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 23.8 ms: 1.55x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 93.3 ms: 4.99x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (9): pylint, deepcopy_reduce, pycparser, go, async_generators, docutils, telco, regex_dna, coroutines
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.043x slower

# HPT report

- Reliability score: 99.32% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x