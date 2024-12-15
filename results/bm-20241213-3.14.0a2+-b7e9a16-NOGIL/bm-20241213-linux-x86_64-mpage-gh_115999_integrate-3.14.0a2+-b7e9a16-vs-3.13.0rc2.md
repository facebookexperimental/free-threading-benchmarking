# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.075x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 531 ms: 1.19x slower                                                 |
| docutils       | 4.01 sec                                                     | 4.14 sec: 1.03x slower                                               |
| html5lib       | 92.6 ms                                                      | 101 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                        | 1.11x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 764 ms: 1.83x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 828 ms: 1.68x faster                                                 |
| async_tree_none_tg         | 504 ms                                                       | 315 ms: 1.60x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 462 ms: 1.45x faster                                                 |
| async_tree_none            | 572 ms                                                       | 406 ms: 1.41x faster                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 637 ms: 1.34x faster                                                 |
| async_tree_memoization     | 709 ms                                                       | 536 ms: 1.32x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 718 ms: 1.24x faster                                                 |
| asyncio_websockets         | 766 ms                                                       | 730 ms: 1.05x faster                                                 |
| async_generators           | 567 ms                                                       | 600 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                         |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 116 ms                                                       | 110 ms: 1.06x faster                                                 |
| nbody          | 119 ms                                                       | 174 ms: 1.47x slower                                                 |
| Geometric mean | (ref)                                                        | 1.10x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.15 ms: 1.14x faster                                                |
| regex_compile  | 182 ms                                                       | 209 ms: 1.15x slower                                                 |
| Geometric mean | (ref)                                                        | 1.00x faster                                                         |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 135 ms: 1.31x faster                                                 |
| xml_etree_parse      | 231 ms                                                       | 209 ms: 1.11x faster                                                 |
| json_loads           | 34.3 us                                                      | 36.6 us: 1.07x slower                                                |
| xml_etree_generate   | 122 ms                                                       | 132 ms: 1.08x slower                                                 |
| tomli_loads          | 2.78 sec                                                     | 3.02 sec: 1.09x slower                                               |
| unpickle_pure_python | 290 us                                                       | 328 us: 1.13x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 97.6 ms: 1.14x slower                                                |
| pickle_pure_python   | 416 us                                                       | 486 us: 1.17x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 16.9 ms: 1.20x slower                                                |
| Geometric mean       | (ref)                                                        | 1.05x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                                |
| python_startup         | 22.4 ms                                                      | 31.4 ms: 1.40x slower                                                |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 81.5 ms: 1.13x slower                                                |
| genshi_text     | 31.7 ms                                                      | 36.3 ms: 1.15x slower                                                |
| django_template | 44.3 ms                                                      | 51.7 ms: 1.17x slower                                                |
| mako            | 15.9 ms                                                      | 23.7 ms: 1.49x slower                                                |
| Geometric mean  | (ref)                                                        | 1.22x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 764 ms: 1.83x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 828 ms: 1.68x faster                                                 |
| async_tree_none_tg         | 504 ms                                                       | 315 ms: 1.60x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 462 ms: 1.45x faster                                                 |
| async_tree_none            | 572 ms                                                       | 406 ms: 1.41x faster                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 637 ms: 1.34x faster                                                 |
| async_tree_memoization     | 709 ms                                                       | 536 ms: 1.32x faster                                                 |
| xml_etree_iterparse        | 177 ms                                                       | 135 ms: 1.31x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 718 ms: 1.24x faster                                                 |
| deepcopy                   | 498 us                                                       | 415 us: 1.20x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 4.15 ms: 1.14x faster                                                |
| xml_etree_parse            | 231 ms                                                       | 209 ms: 1.11x faster                                                 |
| sqlite_synth               | 3.99 us                                                      | 3.71 us: 1.08x faster                                                |
| float                      | 116 ms                                                       | 110 ms: 1.06x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 28.4 ms: 1.05x faster                                                |
| asyncio_websockets         | 766 ms                                                       | 730 ms: 1.05x faster                                                 |
| docutils                   | 4.01 sec                                                     | 4.14 sec: 1.03x slower                                               |
| deepcopy_reduce            | 4.10 us                                                      | 4.24 us: 1.03x slower                                                |
| deepcopy_memo              | 50.1 us                                                      | 52.2 us: 1.04x slower                                                |
| scimark_sor                | 179 ms                                                       | 186 ms: 1.04x slower                                                 |
| json                       | 6.51 ms                                                      | 6.80 ms: 1.04x slower                                                |
| async_generators           | 567 ms                                                       | 600 ms: 1.06x slower                                                 |
| generators                 | 40.0 ms                                                      | 42.5 ms: 1.06x slower                                                |
| json_loads                 | 34.3 us                                                      | 36.6 us: 1.07x slower                                                |
| logging_simple             | 8.56 us                                                      | 9.14 us: 1.07x slower                                                |
| sqlglot_optimize           | 74.7 ms                                                      | 80.2 ms: 1.07x slower                                                |
| xml_etree_generate         | 122 ms                                                       | 132 ms: 1.08x slower                                                 |
| pycparser                  | 1.57 sec                                                     | 1.70 sec: 1.08x slower                                               |
| mdp                        | 3.80 sec                                                     | 4.13 sec: 1.09x slower                                               |
| tomli_loads                | 2.78 sec                                                     | 3.02 sec: 1.09x slower                                               |
| html5lib                   | 92.6 ms                                                      | 101 ms: 1.10x slower                                                 |
| richards                   | 65.5 ms                                                      | 71.8 ms: 1.10x slower                                                |
| pyflate                    | 664 ms                                                       | 735 ms: 1.11x slower                                                 |
| sqlglot_normalize          | 140 ms                                                       | 156 ms: 1.11x slower                                                 |
| meteor_contest             | 150 ms                                                       | 167 ms: 1.11x slower                                                 |
| nqueens                    | 112 ms                                                       | 125 ms: 1.12x slower                                                 |
| unpickle_pure_python       | 290 us                                                       | 328 us: 1.13x slower                                                 |
| genshi_xml                 | 72.1 ms                                                      | 81.5 ms: 1.13x slower                                                |
| scimark_fft                | 473 ms                                                       | 535 ms: 1.13x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 97.6 ms: 1.14x slower                                                |
| dulwich_log                | 93.7 ms                                                      | 107 ms: 1.14x slower                                                 |
| pprint_safe_repr           | 987 ms                                                       | 1.13 sec: 1.14x slower                                               |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.75 ms: 1.15x slower                                                |
| genshi_text                | 31.7 ms                                                      | 36.3 ms: 1.15x slower                                                |
| logging_silent             | 130 ns                                                       | 149 ns: 1.15x slower                                                 |
| regex_compile              | 182 ms                                                       | 209 ms: 1.15x slower                                                 |
| fannkuch                   | 547 ms                                                       | 636 ms: 1.16x slower                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 7.32 sec: 1.16x slower                                               |
| pickle_pure_python         | 416 us                                                       | 486 us: 1.17x slower                                                 |
| richards_super             | 73.2 ms                                                      | 85.5 ms: 1.17x slower                                                |
| django_template            | 44.3 ms                                                      | 51.7 ms: 1.17x slower                                                |
| coverage                   | 107 ms                                                       | 126 ms: 1.18x slower                                                 |
| gc_traversal               | 5.70 ms                                                      | 6.76 ms: 1.19x slower                                                |
| comprehensions             | 22.2 us                                                      | 26.4 us: 1.19x slower                                                |
| pprint_pformat             | 1.94 sec                                                     | 2.31 sec: 1.19x slower                                               |
| logging_format             | 9.24 us                                                      | 11.0 us: 1.19x slower                                                |
| 2to3                       | 445 ms                                                       | 531 ms: 1.19x slower                                                 |
| json_dumps                 | 14.1 ms                                                      | 16.9 ms: 1.20x slower                                                |
| crypto_pyaes               | 100 ms                                                       | 121 ms: 1.21x slower                                                 |
| typing_runtime_protocols   | 226 us                                                       | 273 us: 1.21x slower                                                 |
| thrift                     | 1.10 ms                                                      | 1.33 ms: 1.21x slower                                                |
| scimark_monte_carlo        | 90.6 ms                                                      | 110 ms: 1.21x slower                                                 |
| sqlglot_transpile          | 2.20 ms                                                      | 2.66 ms: 1.21x slower                                                |
| sympy_integrate            | 30.2 ms                                                      | 38.0 ms: 1.26x slower                                                |
| chaos                      | 83.6 ms                                                      | 105 ms: 1.26x slower                                                 |
| bench_thread_pool          | 2.89 ms                                                      | 3.63 ms: 1.26x slower                                                |
| raytrace                   | 344 ms                                                       | 435 ms: 1.26x slower                                                 |
| hexiom                     | 8.11 ms                                                      | 10.2 ms: 1.26x slower                                                |
| sqlglot_parse              | 1.76 ms                                                      | 2.27 ms: 1.29x slower                                                |
| python_startup_no_site     | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                                |
| create_gc_cycles           | 2.41 ms                                                      | 3.26 ms: 1.35x slower                                                |
| scimark_lu                 | 146 ms                                                       | 203 ms: 1.38x slower                                                 |
| python_startup             | 22.4 ms                                                      | 31.4 ms: 1.40x slower                                                |
| deltablue                  | 4.44 ms                                                      | 6.28 ms: 1.41x slower                                                |
| nbody                      | 119 ms                                                       | 174 ms: 1.47x slower                                                 |
| mako                       | 15.9 ms                                                      | 23.7 ms: 1.49x slower                                                |
| sympy_str                  | 379 ms                                                       | 565 ms: 1.49x slower                                                 |
| sympy_expand               | 601 ms                                                       | 1.08 sec: 1.80x slower                                               |
| sympy_sum                  | 210 ms                                                       | 395 ms: 1.88x slower                                                 |
| bench_mp_pool              | 18.7 ms                                                      | 88.8 ms: 4.75x slower                                                |
| Geometric mean             | (ref)                                                        | 1.10x slower                                                         |

Benchmark hidden because not significant (8): go, pidigits, spectral_norm, regex_v8, regex_dna, telco, coroutines, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.075x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x