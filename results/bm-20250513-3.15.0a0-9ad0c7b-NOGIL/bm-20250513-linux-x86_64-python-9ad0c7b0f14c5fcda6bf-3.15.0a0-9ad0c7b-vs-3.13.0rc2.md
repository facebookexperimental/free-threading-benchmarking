# Results vs. 3.13.0rc2

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: linux-x86_64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.073x faster
- HPT reliability: 82.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 378 ms: 1.18x faster                                                  |
| docutils       | 4.01 sec                                                     | 3.68 sec: 1.09x faster                                                |
| html5lib       | 92.6 ms                                                      | 82.2 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                        | 1.13x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 662 ms: 2.12x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 711 ms: 1.95x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 387 ms: 1.73x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 293 ms: 1.72x faster                                                  |
| async_tree_none            | 572 ms                                                       | 340 ms: 1.68x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 434 ms: 1.63x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 579 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 630 ms: 1.41x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 674 ms: 1.14x faster                                                  |
| async_generators           | 567 ms                                                       | 535 ms: 1.06x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.50x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 91.6 ms: 1.26x faster                                                 |
| pidigits       | 251 ms                                                       | 216 ms: 1.16x faster                                                  |
| nbody          | 119 ms                                                       | 154 ms: 1.29x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 27.0 ms: 1.22x faster                                                 |
| regex_effbot   | 4.74 ms                                                      | 3.97 ms: 1.19x faster                                                 |
| regex_dna      | 282 ms                                                       | 249 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                        | 1.14x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 116 ms: 1.53x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 172 ms: 1.35x faster                                                  |
| unpickle_pure_python | 290 us                                                       | 301 us: 1.04x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 435 us: 1.05x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 129 ms: 1.05x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 90.7 ms: 1.06x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 15.6 ms: 1.10x slower                                                 |
| json_loads           | 34.3 us                                                      | 42.2 us: 1.23x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 13.9 ms: 1.10x faster                                                 |
| Geometric mean         | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 33.8 ms: 1.07x slower                                                 |
| django_template | 44.3 ms                                                      | 49.2 ms: 1.11x slower                                                 |
| mako            | 15.9 ms                                                      | 20.6 ms: 1.29x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.12x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 662 ms: 2.12x faster                                                  |
| gc_traversal               | 5.70 ms                                                      | 2.91 ms: 1.96x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 711 ms: 1.95x faster                                                  |
| mdp                        | 3.80 sec                                                     | 2.16 sec: 1.76x faster                                                |
| async_tree_memoization_tg  | 670 ms                                                       | 387 ms: 1.73x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 293 ms: 1.72x faster                                                  |
| async_tree_none            | 572 ms                                                       | 340 ms: 1.68x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 434 ms: 1.63x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 116 ms: 1.53x faster                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 1.93 ms: 1.50x faster                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 579 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 630 ms: 1.41x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 172 ms: 1.35x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 2.99 us: 1.33x faster                                                 |
| deepcopy                   | 498 us                                                       | 373 us: 1.33x faster                                                  |
| float                      | 116 ms                                                       | 91.6 ms: 1.26x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 24.6 ms: 1.22x faster                                                 |
| regex_v8                   | 32.8 ms                                                      | 27.0 ms: 1.22x faster                                                 |
| dulwich_log                | 93.7 ms                                                      | 78.1 ms: 1.20x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 3.97 ms: 1.19x faster                                                 |
| go                         | 191 ms                                                       | 161 ms: 1.18x faster                                                  |
| 2to3                       | 445 ms                                                       | 378 ms: 1.18x faster                                                  |
| pylint                     | 470 ms                                                       | 404 ms: 1.16x faster                                                  |
| pidigits                   | 251 ms                                                       | 216 ms: 1.16x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.7 ms: 1.14x faster                                                 |
| asyncio_websockets         | 766 ms                                                       | 674 ms: 1.14x faster                                                  |
| regex_dna                  | 282 ms                                                       | 249 ms: 1.13x faster                                                  |
| html5lib                   | 92.6 ms                                                      | 82.2 ms: 1.13x faster                                                 |
| scimark_sor                | 179 ms                                                       | 160 ms: 1.12x faster                                                  |
| spectral_norm              | 157 ms                                                       | 141 ms: 1.11x faster                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 13.9 ms: 1.10x faster                                                 |
| deepcopy_memo              | 50.1 us                                                      | 46.0 us: 1.09x faster                                                 |
| docutils                   | 4.01 sec                                                     | 3.68 sec: 1.09x faster                                                |
| create_gc_cycles           | 2.41 ms                                                      | 2.21 ms: 1.09x faster                                                 |
| pycparser                  | 1.57 sec                                                     | 1.46 sec: 1.08x faster                                                |
| deepcopy_reduce            | 4.10 us                                                      | 3.82 us: 1.07x faster                                                 |
| sympy_integrate            | 30.2 ms                                                      | 28.3 ms: 1.07x faster                                                 |
| async_generators           | 567 ms                                                       | 535 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 6.20 sec: 1.01x faster                                                |
| richards_super             | 73.2 ms                                                      | 75.4 ms: 1.03x slower                                                 |
| scimark_fft                | 473 ms                                                       | 488 ms: 1.03x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 218 ms: 1.04x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 301 us: 1.04x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 435 us: 1.05x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 129 ms: 1.05x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 90.7 ms: 1.06x slower                                                 |
| meteor_contest             | 150 ms                                                       | 159 ms: 1.06x slower                                                  |
| generators                 | 40.0 ms                                                      | 42.7 ms: 1.07x slower                                                 |
| genshi_text                | 31.7 ms                                                      | 33.8 ms: 1.07x slower                                                 |
| pprint_pformat             | 1.94 sec                                                     | 2.08 sec: 1.07x slower                                                |
| sympy_expand               | 601 ms                                                       | 646 ms: 1.08x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.28 ms: 1.08x slower                                                 |
| hexiom                     | 8.11 ms                                                      | 8.83 ms: 1.09x slower                                                 |
| logging_simple             | 8.56 us                                                      | 9.38 us: 1.10x slower                                                 |
| typing_runtime_protocols   | 226 us                                                       | 248 us: 1.10x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 15.6 ms: 1.10x slower                                                 |
| fannkuch                   | 547 ms                                                       | 606 ms: 1.11x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 100 ms: 1.11x slower                                                  |
| json                       | 6.51 ms                                                      | 7.22 ms: 1.11x slower                                                 |
| crypto_pyaes               | 100 ms                                                       | 111 ms: 1.11x slower                                                  |
| django_template            | 44.3 ms                                                      | 49.2 ms: 1.11x slower                                                 |
| raytrace                   | 344 ms                                                       | 387 ms: 1.12x slower                                                  |
| comprehensions             | 22.2 us                                                      | 25.2 us: 1.13x slower                                                 |
| logging_format             | 9.24 us                                                      | 10.5 us: 1.14x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 167 ms: 1.14x slower                                                  |
| json_loads                 | 34.3 us                                                      | 42.2 us: 1.23x slower                                                 |
| nbody                      | 119 ms                                                       | 154 ms: 1.29x slower                                                  |
| mako                       | 15.9 ms                                                      | 20.6 ms: 1.29x slower                                                 |
| coverage                   | 107 ms                                                       | 145 ms: 1.35x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 76.4 ms: 4.09x slower                                                 |
| logging_silent             | 130 ns                                                       | 701 ns: 5.39x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (13): coroutines, chaos, thrift, regex_compile, pyflate, richards, tomli_loads, nqueens, python_startup, deltablue, pprint_safe_repr, genshi_xml, sympy_str
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 82.89% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.41x