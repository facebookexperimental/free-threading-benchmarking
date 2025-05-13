# Results vs. 3.13.0rc2

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: linux-x86_64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.169x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 335 ms: 1.33x faster                                                  |
| docutils       | 4.01 sec                                                     | 3.39 sec: 1.18x faster                                                |
| html5lib       | 92.6 ms                                                      | 76.1 ms: 1.22x faster                                                 |
| Geometric mean | (ref)                                                        | 1.24x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 709 ms                                                       | 406 ms: 1.75x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 795 ms: 1.74x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 828 ms: 1.69x faster                                                  |
| async_tree_none            | 572 ms                                                       | 344 ms: 1.66x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 413 ms: 1.62x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 327 ms: 1.54x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 612 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 619 ms: 1.38x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 645 ms: 1.19x faster                                                  |
| async_generators           | 567 ms                                                       | 497 ms: 1.14x faster                                                  |
| coroutines                 | 30.9 ms                                                      | 28.7 ms: 1.07x faster                                                 |
| Geometric mean             | (ref)                                                        | 1.46x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 95.0 ms: 1.22x faster                                                 |
| pidigits       | 251 ms                                                       | 232 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                        | 1.10x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 3.93 ms: 1.21x faster                                                 |
| regex_compile  | 182 ms                                                       | 153 ms: 1.19x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 29.0 ms: 1.13x faster                                                 |
| regex_dna      | 282 ms                                                       | 253 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.16x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 125 ms: 1.42x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 173 ms: 1.33x faster                                                  |
| xml_etree_process    | 85.9 ms                                                      | 74.6 ms: 1.15x faster                                                 |
| tomli_loads          | 2.78 sec                                                     | 2.49 sec: 1.12x faster                                                |
| xml_etree_generate   | 122 ms                                                       | 110 ms: 1.12x faster                                                  |
| unpickle_pure_python | 290 us                                                       | 270 us: 1.07x faster                                                  |
| pickle_pure_python   | 416 us                                                       | 391 us: 1.06x faster                                                  |
| json_dumps           | 14.1 ms                                                      | 14.9 ms: 1.06x slower                                                 |
| json_loads           | 34.3 us                                                      | 37.6 us: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 10.5 ms: 1.46x faster                                                 |
| python_startup         | 22.4 ms                                                      | 17.7 ms: 1.27x faster                                                 |
| Geometric mean         | (ref)                                                        | 1.36x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 26.1 ms: 1.21x faster                                                 |
| genshi_xml      | 72.1 ms                                                      | 60.7 ms: 1.19x faster                                                 |
| django_template | 44.3 ms                                                      | 42.5 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                        | 1.10x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 3.80 sec                                                     | 1.68 sec: 2.26x faster                                                |
| async_tree_memoization     | 709 ms                                                       | 406 ms: 1.75x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 795 ms: 1.74x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 828 ms: 1.69x faster                                                  |
| async_tree_none            | 572 ms                                                       | 344 ms: 1.66x faster                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 1.73 ms: 1.66x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 413 ms: 1.62x faster                                                  |
| deepcopy                   | 498 us                                                       | 321 us: 1.55x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 327 ms: 1.54x faster                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 10.5 ms: 1.46x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 612 ms: 1.45x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 125 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 619 ms: 1.38x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 36.5 us: 1.37x faster                                                 |
| go                         | 191 ms                                                       | 140 ms: 1.36x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 173 ms: 1.33x faster                                                  |
| 2to3                       | 445 ms                                                       | 335 ms: 1.33x faster                                                  |
| telco                      | 12.2 ms                                                      | 9.34 ms: 1.30x faster                                                 |
| pylint                     | 470 ms                                                       | 366 ms: 1.28x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 23.6 ms: 1.28x faster                                                 |
| dulwich_log                | 93.7 ms                                                      | 73.2 ms: 1.28x faster                                                 |
| python_startup             | 22.4 ms                                                      | 17.7 ms: 1.27x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 24.2 ms: 1.24x faster                                                 |
| richards                   | 65.5 ms                                                      | 53.4 ms: 1.23x faster                                                 |
| scimark_sor                | 179 ms                                                       | 146 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.35 us: 1.22x faster                                                 |
| sqlite_synth               | 3.99 us                                                      | 3.27 us: 1.22x faster                                                 |
| float                      | 116 ms                                                       | 95.0 ms: 1.22x faster                                                 |
| html5lib                   | 92.6 ms                                                      | 76.1 ms: 1.22x faster                                                 |
| genshi_text                | 31.7 ms                                                      | 26.1 ms: 1.21x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 3.93 ms: 1.21x faster                                                 |
| spectral_norm              | 157 ms                                                       | 130 ms: 1.20x faster                                                  |
| richards_super             | 73.2 ms                                                      | 61.2 ms: 1.20x faster                                                 |
| regex_compile              | 182 ms                                                       | 153 ms: 1.19x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 645 ms: 1.19x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 60.7 ms: 1.19x faster                                                 |
| docutils                   | 4.01 sec                                                     | 3.39 sec: 1.18x faster                                                |
| meteor_contest             | 150 ms                                                       | 128 ms: 1.18x faster                                                  |
| thrift                     | 1.10 ms                                                      | 941 us: 1.17x faster                                                  |
| sympy_str                  | 379 ms                                                       | 325 ms: 1.17x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.45 sec: 1.15x faster                                                |
| xml_etree_process          | 85.9 ms                                                      | 74.6 ms: 1.15x faster                                                 |
| typing_runtime_protocols   | 226 us                                                       | 196 us: 1.15x faster                                                  |
| async_generators           | 567 ms                                                       | 497 ms: 1.14x faster                                                  |
| nqueens                    | 112 ms                                                       | 98.3 ms: 1.14x faster                                                 |
| chaos                      | 83.6 ms                                                      | 73.6 ms: 1.14x faster                                                 |
| regex_v8                   | 32.8 ms                                                      | 29.0 ms: 1.13x faster                                                 |
| sympy_sum                  | 210 ms                                                       | 186 ms: 1.13x faster                                                  |
| pyflate                    | 664 ms                                                       | 588 ms: 1.13x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.02 ms: 1.12x faster                                                 |
| tomli_loads                | 2.78 sec                                                     | 2.49 sec: 1.12x faster                                                |
| xml_etree_generate         | 122 ms                                                       | 110 ms: 1.12x faster                                                  |
| regex_dna                  | 282 ms                                                       | 253 ms: 1.12x faster                                                  |
| pycparser                  | 1.57 sec                                                     | 1.42 sec: 1.11x faster                                                |
| scimark_monte_carlo        | 90.6 ms                                                      | 81.8 ms: 1.11x faster                                                 |
| crypto_pyaes               | 100 ms                                                       | 91.7 ms: 1.09x faster                                                 |
| fannkuch                   | 547 ms                                                       | 501 ms: 1.09x faster                                                  |
| sympy_expand               | 601 ms                                                       | 551 ms: 1.09x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 906 ms: 1.09x faster                                                  |
| hexiom                     | 8.11 ms                                                      | 7.47 ms: 1.09x faster                                                 |
| pidigits                   | 251 ms                                                       | 232 ms: 1.08x faster                                                  |
| coroutines                 | 30.9 ms                                                      | 28.7 ms: 1.07x faster                                                 |
| unpickle_pure_python       | 290 us                                                       | 270 us: 1.07x faster                                                  |
| scimark_fft                | 473 ms                                                       | 443 ms: 1.07x faster                                                  |
| pickle_pure_python         | 416 us                                                       | 391 us: 1.06x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 1.84 sec: 1.06x faster                                                |
| deltablue                  | 4.44 ms                                                      | 4.22 ms: 1.05x faster                                                 |
| comprehensions             | 22.2 us                                                      | 21.2 us: 1.05x faster                                                 |
| django_template            | 44.3 ms                                                      | 42.5 ms: 1.04x faster                                                 |
| coverage                   | 107 ms                                                       | 105 ms: 1.03x faster                                                  |
| raytrace                   | 344 ms                                                       | 337 ms: 1.02x faster                                                  |
| json                       | 6.51 ms                                                      | 6.83 ms: 1.05x slower                                                 |
| json_dumps                 | 14.1 ms                                                      | 14.9 ms: 1.06x slower                                                 |
| json_loads                 | 34.3 us                                                      | 37.6 us: 1.10x slower                                                 |
| gc_traversal               | 5.70 ms                                                      | 6.41 ms: 1.12x slower                                                 |
| create_gc_cycles           | 2.41 ms                                                      | 3.15 ms: 1.30x slower                                                 |
| bench_mp_pool              | 18.7 ms                                                      | 82.0 ms: 4.39x slower                                                 |
| logging_silent             | 130 ns                                                       | 606 ns: 4.66x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                          |

Benchmark hidden because not significant (6): logging_simple, logging_format, nbody, generators, scimark_lu, mako
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.169x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.16x