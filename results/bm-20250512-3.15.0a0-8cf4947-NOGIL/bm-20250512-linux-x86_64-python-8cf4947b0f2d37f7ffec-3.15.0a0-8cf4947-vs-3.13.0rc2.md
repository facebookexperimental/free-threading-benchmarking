# Results vs. 3.13.0rc2

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: linux-x86_64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.079x faster
- HPT reliability: 91.34%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 384 ms: 1.16x faster                                                  |
| docutils       | 4.01 sec                                                     | 3.62 sec: 1.11x faster                                                |
| html5lib       | 92.6 ms                                                      | 82.0 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                        | 1.13x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 677 ms: 2.07x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 727 ms: 1.91x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 294 ms: 1.71x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 395 ms: 1.70x faster                                                  |
| async_tree_none            | 572 ms                                                       | 348 ms: 1.64x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 440 ms: 1.61x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 585 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 638 ms: 1.39x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 674 ms: 1.14x faster                                                  |
| async_generators           | 567 ms                                                       | 538 ms: 1.06x faster                                                  |
| coroutines                 | 30.9 ms                                                      | 29.2 ms: 1.05x faster                                                 |
| Geometric mean             | (ref)                                                        | 1.49x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 90.3 ms: 1.28x faster                                                 |
| pidigits       | 251 ms                                                       | 215 ms: 1.17x faster                                                  |
| nbody          | 119 ms                                                       | 154 ms: 1.30x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 26.8 ms: 1.22x faster                                                 |
| regex_effbot   | 4.74 ms                                                      | 3.92 ms: 1.21x faster                                                 |
| regex_dna      | 282 ms                                                       | 249 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                        | 1.14x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 118 ms: 1.50x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 171 ms: 1.35x faster                                                  |
| unpickle_pure_python | 290 us                                                       | 298 us: 1.03x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 91.1 ms: 1.06x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 130 ms: 1.06x slower                                                  |
| json_loads           | 34.3 us                                                      | 41.2 us: 1.20x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 17.1 ms: 1.21x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (2): tomli_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 13.7 ms: 1.11x faster                                                 |
| Geometric mean         | (ref)                                                        | 1.06x faster                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 33.7 ms: 1.06x slower                                                 |
| django_template | 44.3 ms                                                      | 48.4 ms: 1.09x slower                                                 |
| mako            | 15.9 ms                                                      | 20.7 ms: 1.30x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.11x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 677 ms: 2.07x faster                                                  |
| gc_traversal               | 5.70 ms                                                      | 2.89 ms: 1.97x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 727 ms: 1.91x faster                                                  |
| mdp                        | 3.80 sec                                                     | 2.06 sec: 1.84x faster                                                |
| async_tree_none_tg         | 504 ms                                                       | 294 ms: 1.71x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 395 ms: 1.70x faster                                                  |
| async_tree_none            | 572 ms                                                       | 348 ms: 1.64x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 440 ms: 1.61x faster                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 1.86 ms: 1.55x faster                                                 |
| xml_etree_iterparse        | 177 ms                                                       | 118 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 585 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 638 ms: 1.39x faster                                                  |
| sqlite_synth               | 3.99 us                                                      | 2.95 us: 1.35x faster                                                 |
| xml_etree_parse            | 231 ms                                                       | 171 ms: 1.35x faster                                                  |
| deepcopy                   | 498 us                                                       | 369 us: 1.35x faster                                                  |
| float                      | 116 ms                                                       | 90.3 ms: 1.28x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 24.0 ms: 1.25x faster                                                 |
| regex_v8                   | 32.8 ms                                                      | 26.8 ms: 1.22x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 3.92 ms: 1.21x faster                                                 |
| dulwich_log                | 93.7 ms                                                      | 78.1 ms: 1.20x faster                                                 |
| go                         | 191 ms                                                       | 161 ms: 1.19x faster                                                  |
| pylint                     | 470 ms                                                       | 400 ms: 1.18x faster                                                  |
| pidigits                   | 251 ms                                                       | 215 ms: 1.17x faster                                                  |
| 2to3                       | 445 ms                                                       | 384 ms: 1.16x faster                                                  |
| telco                      | 12.2 ms                                                      | 10.5 ms: 1.15x faster                                                 |
| spectral_norm              | 157 ms                                                       | 136 ms: 1.15x faster                                                  |
| scimark_sor                | 179 ms                                                       | 157 ms: 1.14x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 674 ms: 1.14x faster                                                  |
| pycparser                  | 1.57 sec                                                     | 1.39 sec: 1.13x faster                                                |
| html5lib                   | 92.6 ms                                                      | 82.0 ms: 1.13x faster                                                 |
| regex_dna                  | 282 ms                                                       | 249 ms: 1.13x faster                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 13.7 ms: 1.11x faster                                                 |
| deepcopy_memo              | 50.1 us                                                      | 45.2 us: 1.11x faster                                                 |
| docutils                   | 4.01 sec                                                     | 3.62 sec: 1.11x faster                                                |
| create_gc_cycles           | 2.41 ms                                                      | 2.19 ms: 1.10x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 3.81 us: 1.08x faster                                                 |
| sympy_integrate            | 30.2 ms                                                      | 28.5 ms: 1.06x faster                                                 |
| async_generators           | 567 ms                                                       | 538 ms: 1.06x faster                                                  |
| coroutines                 | 30.9 ms                                                      | 29.2 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 6.07 sec: 1.03x faster                                                |
| pyflate                    | 664 ms                                                       | 645 ms: 1.03x faster                                                  |
| unpickle_pure_python       | 290 us                                                       | 298 us: 1.03x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 218 ms: 1.04x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.08 ms: 1.05x slower                                                 |
| meteor_contest             | 150 ms                                                       | 157 ms: 1.05x slower                                                  |
| generators                 | 40.0 ms                                                      | 42.0 ms: 1.05x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 91.1 ms: 1.06x slower                                                 |
| xml_etree_generate         | 122 ms                                                       | 130 ms: 1.06x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 33.7 ms: 1.06x slower                                                 |
| pprint_pformat             | 1.94 sec                                                     | 2.07 sec: 1.07x slower                                                |
| sympy_expand               | 601 ms                                                       | 644 ms: 1.07x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 97.5 ms: 1.08x slower                                                 |
| hexiom                     | 8.11 ms                                                      | 8.78 ms: 1.08x slower                                                 |
| json                       | 6.51 ms                                                      | 7.06 ms: 1.08x slower                                                 |
| django_template            | 44.3 ms                                                      | 48.4 ms: 1.09x slower                                                 |
| fannkuch                   | 547 ms                                                       | 604 ms: 1.10x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 111 ms: 1.11x slower                                                  |
| raytrace                   | 344 ms                                                       | 383 ms: 1.11x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 251 us: 1.11x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 163 ms: 1.12x slower                                                  |
| logging_simple             | 8.56 us                                                      | 9.59 us: 1.12x slower                                                 |
| logging_format             | 9.24 us                                                      | 10.4 us: 1.12x slower                                                 |
| comprehensions             | 22.2 us                                                      | 24.9 us: 1.12x slower                                                 |
| json_loads                 | 34.3 us                                                      | 41.2 us: 1.20x slower                                                 |
| json_dumps                 | 14.1 ms                                                      | 17.1 ms: 1.21x slower                                                 |
| nbody                      | 119 ms                                                       | 154 ms: 1.30x slower                                                  |
| mako                       | 15.9 ms                                                      | 20.7 ms: 1.30x slower                                                 |
| coverage                   | 107 ms                                                       | 142 ms: 1.32x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 74.3 ms: 3.98x slower                                                 |
| logging_silent             | 130 ns                                                       | 697 ns: 5.36x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                          |

Benchmark hidden because not significant (14): chaos, regex_compile, richards, nqueens, deltablue, tomli_loads, python_startup, thrift, genshi_xml, scimark_fft, pprint_safe_repr, richards_super, sympy_str, pickle_pure_python
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 91.34% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.40x