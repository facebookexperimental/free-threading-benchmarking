# Results vs. 3.13.0rc2

- fork: python
- ref: fda056e64bdfcac3dd3d
- machine: linux-x86_64
- commit hash: fda056e
- commit date: 2025-02-26
- overall geometric mean: 1.033x slower
- HPT reliability: 99.94%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 500 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x slower                                                           |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 745 ms: 1.88x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 805 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 332 ms: 1.52x faster                                                   |
| async_tree_none            | 572 ms                                                       | 391 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 476 ms: 1.41x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 525 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 639 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 734 ms: 1.21x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 805 ms: 1.05x slower                                                   |
| coroutines                 | 30.9 ms                                                      | 32.5 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 105 ms: 1.10x faster                                                   |
| pidigits       | 251 ms                                                       | 233 ms: 1.08x faster                                                   |
| nbody          | 119 ms                                                       | 171 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.15 ms: 1.14x faster                                                  |
| regex_dna      | 282 ms                                                       | 295 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 134 ms: 1.32x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 201 ms: 1.15x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.01 sec: 1.08x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 319 us: 1.10x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 490 us: 1.18x slower                                                   |
| json_loads           | 34.3 us                                                      | 42.0 us: 1.23x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 17.6 ms: 1.25x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                                  |
| python_startup         | 22.4 ms                                                      | 30.5 ms: 1.36x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.33x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 80.1 ms: 1.11x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 35.6 ms: 1.12x slower                                                  |
| django_template | 44.3 ms                                                      | 50.8 ms: 1.15x slower                                                  |
| mako            | 15.9 ms                                                      | 22.1 ms: 1.38x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.19x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 745 ms: 1.88x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 805 ms: 1.72x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.62 ms: 1.57x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 332 ms: 1.52x faster                                                   |
| async_tree_none            | 572 ms                                                       | 391 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 476 ms: 1.41x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 525 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 639 ms: 1.33x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 134 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 734 ms: 1.21x faster                                                   |
| deepcopy                   | 498 us                                                       | 415 us: 1.20x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 201 ms: 1.15x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.15 ms: 1.14x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 3.58 us: 1.12x faster                                                  |
| float                      | 116 ms                                                       | 105 ms: 1.10x faster                                                   |
| pidigits                   | 251 ms                                                       | 233 ms: 1.08x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 47.0 us: 1.07x faster                                                  |
| spectral_norm              | 157 ms                                                       | 148 ms: 1.06x faster                                                   |
| go                         | 191 ms                                                       | 183 ms: 1.04x faster                                                   |
| pycparser                  | 1.57 sec                                                     | 1.52 sec: 1.03x faster                                                 |
| thrift                     | 1.10 ms                                                      | 1.13 ms: 1.03x slower                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 4.25 us: 1.04x slower                                                  |
| regex_dna                  | 282 ms                                                       | 295 ms: 1.05x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 78.1 ms: 1.05x slower                                                  |
| asyncio_websockets         | 766 ms                                                       | 805 ms: 1.05x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.01 sec: 1.05x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 32.5 ms: 1.05x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 99.7 ms: 1.06x slower                                                  |
| richards                   | 65.5 ms                                                      | 70.0 ms: 1.07x slower                                                  |
| generators                 | 40.0 ms                                                      | 43.1 ms: 1.08x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 2.61 ms: 1.08x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.01 sec: 1.08x slower                                                 |
| sympy_integrate            | 30.2 ms                                                      | 33.1 ms: 1.09x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 319 us: 1.10x slower                                                   |
| chaos                      | 83.6 ms                                                      | 92.1 ms: 1.10x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.09 sec: 1.10x slower                                                 |
| genshi_xml                 | 72.1 ms                                                      | 80.1 ms: 1.11x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.58 ms: 1.12x slower                                                  |
| logging_silent             | 130 ns                                                       | 146 ns: 1.12x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.06 sec: 1.12x slower                                                 |
| 2to3                       | 445 ms                                                       | 500 ms: 1.12x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 35.6 ms: 1.12x slower                                                  |
| sympy_expand               | 601 ms                                                       | 677 ms: 1.13x slower                                                   |
| richards_super             | 73.2 ms                                                      | 82.5 ms: 1.13x slower                                                  |
| sympy_str                  | 379 ms                                                       | 429 ms: 1.13x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 5.02 ms: 1.13x slower                                                  |
| scimark_fft                | 473 ms                                                       | 540 ms: 1.14x slower                                                   |
| django_template            | 44.3 ms                                                      | 50.8 ms: 1.15x slower                                                  |
| pyflate                    | 664 ms                                                       | 762 ms: 1.15x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 161 ms: 1.15x slower                                                   |
| comprehensions             | 22.2 us                                                      | 25.6 us: 1.15x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 263 us: 1.17x slower                                                   |
| meteor_contest             | 150 ms                                                       | 175 ms: 1.17x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.28 sec: 1.17x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 490 us: 1.18x slower                                                   |
| json                       | 6.51 ms                                                      | 7.68 ms: 1.18x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 2.60 ms: 1.19x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 254 ms: 1.21x slower                                                   |
| fannkuch                   | 547 ms                                                       | 664 ms: 1.21x slower                                                   |
| nqueens                    | 112 ms                                                       | 136 ms: 1.21x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 110 ms: 1.22x slower                                                   |
| raytrace                   | 344 ms                                                       | 420 ms: 1.22x slower                                                   |
| json_loads                 | 34.3 us                                                      | 42.0 us: 1.23x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.16 ms: 1.23x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 17.6 ms: 1.25x slower                                                  |
| logging_format             | 9.24 us                                                      | 11.5 us: 1.25x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 125 ms: 1.25x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.61 ms: 1.25x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 183 ms: 1.25x slower                                                   |
| coverage                   | 107 ms                                                       | 138 ms: 1.28x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 10.4 ms: 1.28x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                                  |
| python_startup             | 22.4 ms                                                      | 30.5 ms: 1.36x slower                                                  |
| mako                       | 15.9 ms                                                      | 22.1 ms: 1.38x slower                                                  |
| nbody                      | 119 ms                                                       | 171 ms: 1.44x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 81.5 ms: 4.36x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (12): pylint, pathlib, telco, async_generators, regex_v8, docutils, html5lib, logging_simple, xml_etree_process, xml_etree_generate, scimark_sor, regex_compile
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.033x slower

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.35x