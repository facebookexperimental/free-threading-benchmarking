# Results vs. 3.13.0rc2

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.027x slower
- HPT reliability: 98.66%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 516 ms: 1.16x slower                                                  |
| docutils       | 4.01 sec                                                     | 4.30 sec: 1.07x slower                                                |
| html5lib       | 92.6 ms                                                      | 103 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 746 ms: 1.88x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 776 ms: 1.79x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 320 ms: 1.58x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 462 ms: 1.45x faster                                                  |
| async_tree_none            | 572 ms                                                       | 404 ms: 1.41x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 513 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 643 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 688 ms: 1.29x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 720 ms: 1.06x faster                                                  |
| coroutines                 | 30.9 ms                                                      | 32.5 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                          |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 89.0 ms: 1.30x faster                                                 |
| pidigits       | 251 ms                                                       | 273 ms: 1.09x slower                                                  |
| nbody          | 119 ms                                                       | 158 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.19 ms: 1.13x faster                                                 |
| regex_v8       | 32.8 ms                                                      | 29.6 ms: 1.11x faster                                                 |
| regex_compile  | 182 ms                                                       | 222 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 139 ms: 1.27x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 210 ms: 1.10x faster                                                  |
| tomli_loads          | 2.78 sec                                                     | 2.92 sec: 1.05x slower                                                |
| xml_etree_process    | 85.9 ms                                                      | 94.4 ms: 1.10x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 322 us: 1.11x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 483 us: 1.16x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 18.1 ms: 1.28x slower                                                 |
| json_loads           | 34.3 us                                                      | 45.4 us: 1.33x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 33.4 ms: 1.49x slower                                                 |
| python_startup_no_site | 15.3 ms                                                      | 24.8 ms: 1.62x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.55x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 34.6 ms: 1.09x slower                                                 |
| genshi_xml      | 72.1 ms                                                      | 84.5 ms: 1.17x slower                                                 |
| django_template | 44.3 ms                                                      | 59.6 ms: 1.35x slower                                                 |
| mako            | 15.9 ms                                                      | 23.4 ms: 1.47x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.26x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 746 ms: 1.88x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 776 ms: 1.79x faster                                                  |
| mdp                        | 3.80 sec                                                     | 2.31 sec: 1.64x faster                                                |
| async_tree_none_tg         | 504 ms                                                       | 320 ms: 1.58x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 462 ms: 1.45x faster                                                  |
| async_tree_none            | 572 ms                                                       | 404 ms: 1.41x faster                                                  |
| gc_traversal               | 5.70 ms                                                      | 4.07 ms: 1.40x faster                                                 |
| async_tree_memoization     | 709 ms                                                       | 513 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 643 ms: 1.33x faster                                                  |
| float                      | 116 ms                                                       | 89.0 ms: 1.30x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 688 ms: 1.29x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 139 ms: 1.27x faster                                                  |
| deepcopy                   | 498 us                                                       | 401 us: 1.24x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.19 ms: 1.13x faster                                                 |
| sqlite_synth               | 3.99 us                                                      | 3.56 us: 1.12x faster                                                 |
| regex_v8                   | 32.8 ms                                                      | 29.6 ms: 1.11x faster                                                 |
| xml_etree_parse            | 231 ms                                                       | 210 ms: 1.10x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 46.8 us: 1.07x faster                                                 |
| asyncio_websockets         | 766 ms                                                       | 720 ms: 1.06x faster                                                  |
| scimark_sor                | 179 ms                                                       | 172 ms: 1.04x faster                                                  |
| pycparser                  | 1.57 sec                                                     | 1.63 sec: 1.04x slower                                                |
| tomli_loads                | 2.78 sec                                                     | 2.92 sec: 1.05x slower                                                |
| coroutines                 | 30.9 ms                                                      | 32.5 ms: 1.05x slower                                                 |
| pprint_safe_repr           | 987 ms                                                       | 1.04 sec: 1.06x slower                                                |
| pyflate                    | 664 ms                                                       | 706 ms: 1.06x slower                                                  |
| scimark_fft                | 473 ms                                                       | 504 ms: 1.06x slower                                                  |
| docutils                   | 4.01 sec                                                     | 4.30 sec: 1.07x slower                                                |
| richards_super             | 73.2 ms                                                      | 78.7 ms: 1.08x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.43 us: 1.08x slower                                                 |
| logging_silent             | 130 ns                                                       | 141 ns: 1.09x slower                                                  |
| nqueens                    | 112 ms                                                       | 122 ms: 1.09x slower                                                  |
| pidigits                   | 251 ms                                                       | 273 ms: 1.09x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 34.6 ms: 1.09x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 94.4 ms: 1.10x slower                                                 |
| html5lib                   | 92.6 ms                                                      | 103 ms: 1.11x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 322 us: 1.11x slower                                                  |
| meteor_contest             | 150 ms                                                       | 168 ms: 1.12x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 2.70 ms: 1.12x slower                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.65 ms: 1.13x slower                                                 |
| pprint_pformat             | 1.94 sec                                                     | 2.21 sec: 1.13x slower                                                |
| sympy_integrate            | 30.2 ms                                                      | 34.5 ms: 1.14x slower                                                 |
| sympy_str                  | 379 ms                                                       | 433 ms: 1.14x slower                                                  |
| logging_simple             | 8.56 us                                                      | 9.83 us: 1.15x slower                                                 |
| logging_format             | 9.24 us                                                      | 10.7 us: 1.16x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 483 us: 1.16x slower                                                  |
| fannkuch                   | 547 ms                                                       | 634 ms: 1.16x slower                                                  |
| 2to3                       | 445 ms                                                       | 516 ms: 1.16x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 117 ms: 1.17x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 84.5 ms: 1.17x slower                                                 |
| hexiom                     | 8.11 ms                                                      | 9.53 ms: 1.18x slower                                                 |
| sympy_expand               | 601 ms                                                       | 709 ms: 1.18x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 108 ms: 1.19x slower                                                  |
| generators                 | 40.0 ms                                                      | 47.7 ms: 1.19x slower                                                 |
| typing_runtime_protocols   | 226 us                                                       | 270 us: 1.20x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 253 ms: 1.20x slower                                                  |
| chaos                      | 83.6 ms                                                      | 101 ms: 1.21x slower                                                  |
| regex_compile              | 182 ms                                                       | 222 ms: 1.22x slower                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 7.69 sec: 1.22x slower                                                |
| raytrace                   | 344 ms                                                       | 425 ms: 1.24x slower                                                  |
| json                       | 6.51 ms                                                      | 8.12 ms: 1.25x slower                                                 |
| comprehensions             | 22.2 us                                                      | 27.7 us: 1.25x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 183 ms: 1.25x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 18.1 ms: 1.28x slower                                                 |
| deltablue                  | 4.44 ms                                                      | 5.81 ms: 1.31x slower                                                 |
| json_loads                 | 34.3 us                                                      | 45.4 us: 1.33x slower                                                 |
| nbody                      | 119 ms                                                       | 158 ms: 1.33x slower                                                  |
| django_template            | 44.3 ms                                                      | 59.6 ms: 1.35x slower                                                 |
| mako                       | 15.9 ms                                                      | 23.4 ms: 1.47x slower                                                 |
| python_startup             | 22.4 ms                                                      | 33.4 ms: 1.49x slower                                                 |
| coverage                   | 107 ms                                                       | 164 ms: 1.52x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 24.8 ms: 1.62x slower                                                 |
| bench_thread_pool          | 2.89 ms                                                      | 5.16 ms: 1.79x slower                                                 |
| bench_mp_pool              | 18.7 ms                                                      | 98.5 ms: 5.27x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                          |

Benchmark hidden because not significant (10): spectral_norm, telco, pylint, go, richards, async_generators, regex_dna, pathlib, xml_etree_generate, dulwich_log
Ignored benchmarks (19) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250402-3.14.0a6+-ccaa69a-NOGIL/bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.027x slower

# HPT report

- Reliability score: 98.66% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x