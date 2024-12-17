# Results vs. 3.13.0rc2

- fork: python
- ref: cfeaa992ba9bad9be268
- machine: linux-x86_64
- commit hash: cfeaa99
- commit date: 2024-12-16
- overall geometric mean: 1.186x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 583 ms: 1.31x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.37 sec: 1.09x slower                                                 |
| html5lib       | 92.6 ms                                                      | 123 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                        | 1.24x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.01 sec: 1.38x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 1.05 sec: 1.32x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 572 ms: 1.17x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 444 ms: 1.13x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 641 ms: 1.11x faster                                                   |
| async_tree_none            | 572 ms                                                       | 521 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 828 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 810 ms: 1.05x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 730 ms: 1.05x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 35.3 ms: 1.14x slower                                                  |
| async_generators           | 567 ms                                                       | 651 ms: 1.15x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 231 ms: 1.09x faster                                                   |
| float          | 116 ms                                                       | 167 ms: 1.44x slower                                                   |
| nbody          | 119 ms                                                       | 173 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                        | 1.25x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.09 ms: 1.16x faster                                                  |
| regex_dna      | 282 ms                                                       | 290 ms: 1.03x slower                                                   |
| regex_v8       | 32.8 ms                                                      | 34.6 ms: 1.05x slower                                                  |
| regex_compile  | 182 ms                                                       | 214 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 137 ms: 1.29x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 205 ms: 1.13x faster                                                   |
| json_loads           | 34.3 us                                                      | 36.0 us: 1.05x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 137 ms: 1.12x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.31 sec: 1.19x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 103 ms: 1.19x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 17.5 ms: 1.24x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 414 us: 1.43x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 679 us: 1.63x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.14x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.3 ms: 1.26x slower                                                  |
| python_startup         | 22.4 ms                                                      | 31.2 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.32x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 88.9 ms: 1.23x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 39.9 ms: 1.26x slower                                                  |
| django_template | 44.3 ms                                                      | 61.0 ms: 1.38x slower                                                  |
| mako            | 15.9 ms                                                      | 25.3 ms: 1.59x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.36x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.01 sec: 1.38x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 1.05 sec: 1.32x faster                                                 |
| xml_etree_iterparse        | 177 ms                                                       | 137 ms: 1.29x faster                                                   |
| deepcopy                   | 498 us                                                       | 401 us: 1.24x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 572 ms: 1.17x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.09 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 444 ms: 1.13x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 205 ms: 1.13x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 641 ms: 1.11x faster                                                   |
| async_tree_none            | 572 ms                                                       | 521 ms: 1.10x faster                                                   |
| pidigits                   | 251 ms                                                       | 231 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 828 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 810 ms: 1.05x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 730 ms: 1.05x faster                                                   |
| regex_dna                  | 282 ms                                                       | 290 ms: 1.03x slower                                                   |
| deepcopy_memo              | 50.1 us                                                      | 51.8 us: 1.03x slower                                                  |
| json_loads                 | 34.3 us                                                      | 36.0 us: 1.05x slower                                                  |
| telco                      | 12.2 ms                                                      | 12.8 ms: 1.05x slower                                                  |
| regex_v8                   | 32.8 ms                                                      | 34.6 ms: 1.05x slower                                                  |
| json                       | 6.51 ms                                                      | 6.95 ms: 1.07x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.35 ms: 1.09x slower                                                  |
| docutils                   | 4.01 sec                                                     | 4.37 sec: 1.09x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.47 us: 1.09x slower                                                  |
| pylint                     | 470 ms                                                       | 522 ms: 1.11x slower                                                   |
| xml_etree_generate         | 122 ms                                                       | 137 ms: 1.12x slower                                                   |
| scimark_fft                | 473 ms                                                       | 536 ms: 1.13x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 85.0 ms: 1.14x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 35.3 ms: 1.14x slower                                                  |
| async_generators           | 567 ms                                                       | 651 ms: 1.15x slower                                                   |
| nqueens                    | 112 ms                                                       | 129 ms: 1.15x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.46 sec: 1.17x slower                                                 |
| regex_compile              | 182 ms                                                       | 214 ms: 1.17x slower                                                   |
| meteor_contest             | 150 ms                                                       | 178 ms: 1.19x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.31 sec: 1.19x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 103 ms: 1.19x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 113 ms: 1.20x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.55 sec: 1.20x slower                                                 |
| gc_traversal               | 5.70 ms                                                      | 6.93 ms: 1.22x slower                                                  |
| pycparser                  | 1.57 sec                                                     | 1.93 sec: 1.23x slower                                                 |
| genshi_xml                 | 72.1 ms                                                      | 88.9 ms: 1.23x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 124 ms: 1.23x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 17.5 ms: 1.24x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 279 us: 1.24x slower                                                   |
| coverage                   | 107 ms                                                       | 134 ms: 1.25x slower                                                   |
| fannkuch                   | 547 ms                                                       | 683 ms: 1.25x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 175 ms: 1.25x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 19.3 ms: 1.26x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 39.9 ms: 1.26x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 38.3 ms: 1.27x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.29 sec: 1.30x slower                                                 |
| 2to3                       | 445 ms                                                       | 583 ms: 1.31x slower                                                   |
| html5lib                   | 92.6 ms                                                      | 123 ms: 1.32x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.47 ms: 1.33x slower                                                  |
| generators                 | 40.0 ms                                                      | 54.3 ms: 1.36x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.65 sec: 1.36x slower                                                 |
| django_template            | 44.3 ms                                                      | 61.0 ms: 1.38x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.99 ms: 1.38x slower                                                  |
| python_startup             | 22.4 ms                                                      | 31.2 ms: 1.39x slower                                                  |
| richards                   | 65.5 ms                                                      | 92.4 ms: 1.41x slower                                                  |
| pyflate                    | 664 ms                                                       | 943 ms: 1.42x slower                                                   |
| logging_format             | 9.24 us                                                      | 13.2 us: 1.42x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 414 us: 1.43x slower                                                   |
| logging_simple             | 8.56 us                                                      | 12.3 us: 1.44x slower                                                  |
| float                      | 116 ms                                                       | 167 ms: 1.44x slower                                                   |
| richards_super             | 73.2 ms                                                      | 106 ms: 1.45x slower                                                   |
| nbody                      | 119 ms                                                       | 173 ms: 1.46x slower                                                   |
| comprehensions             | 22.2 us                                                      | 32.6 us: 1.47x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 222 ms: 1.52x slower                                                   |
| chaos                      | 83.6 ms                                                      | 129 ms: 1.54x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 3.72 ms: 1.54x slower                                                  |
| sympy_str                  | 379 ms                                                       | 586 ms: 1.55x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 12.8 ms: 1.58x slower                                                  |
| mako                       | 15.9 ms                                                      | 25.3 ms: 1.59x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 679 us: 1.63x slower                                                   |
| go                         | 191 ms                                                       | 315 ms: 1.65x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 151 ms: 1.67x slower                                                   |
| scimark_sor                | 179 ms                                                       | 302 ms: 1.69x slower                                                   |
| logging_silent             | 130 ns                                                       | 221 ns: 1.70x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 3.99 ms: 1.82x slower                                                  |
| sympy_expand               | 601 ms                                                       | 1.09 sec: 1.82x slower                                                 |
| raytrace                   | 344 ms                                                       | 635 ms: 1.85x slower                                                   |
| sqlglot_parse              | 1.76 ms                                                      | 3.30 ms: 1.88x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 400 ms: 1.90x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 11.4 ms: 2.57x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 92.3 ms: 4.94x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.26x slower                                                           |

Benchmark hidden because not significant (3): sqlite_synth, spectral_norm, pathlib
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.186x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.33x