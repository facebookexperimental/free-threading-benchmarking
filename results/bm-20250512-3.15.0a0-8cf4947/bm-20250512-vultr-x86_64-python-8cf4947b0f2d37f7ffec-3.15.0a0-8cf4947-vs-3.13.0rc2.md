# Results vs. 3.13.0rc2

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: linux-x86_64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.072x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.52 sec: 1.04x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.2 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 311 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 599 ms: 1.46x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 626 ms: 1.46x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 506 ms: 1.32x faster                                                  |
| async_tree_none            | 354 ms                                                       | 271 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                  |
| async_generators           | 377 ms                                                       | 328 ms: 1.15x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                  |
| float          | 77.5 ms                                                      | 70.3 ms: 1.10x faster                                                 |
| nbody          | 85.1 ms                                                      | 87.9 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.14x faster                                                 |
| regex_compile  | 132 ms                                                       | 123 ms: 1.08x faster                                                  |
| regex_dna      | 180 ms                                                       | 174 ms: 1.03x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 82.4 ms: 1.04x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.6 ms: 1.03x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 207 us: 1.02x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.9 us: 1.07x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 12.1 ms: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.33 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.5 ms                                                      | 20.4 ms: 1.06x faster                                                 |
| genshi_xml     | 48.8 ms                                                      | 47.8 ms: 1.02x faster                                                 |
| mako           | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.06x faster                                                |
| async_tree_memoization     | 461 ms                                                       | 311 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 599 ms: 1.46x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 626 ms: 1.46x faster                                                  |
| deepcopy                   | 355 us                                                       | 250 us: 1.42x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 28.5 us: 1.37x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.32x faster                                                  |
| go                         | 141 ms                                                       | 107 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 506 ms: 1.32x faster                                                  |
| async_tree_none            | 354 ms                                                       | 271 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                  |
| scimark_sor                | 134 ms                                                       | 110 ms: 1.23x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.17x faster                                                 |
| spectral_norm              | 111 ms                                                       | 96.3 ms: 1.15x faster                                                 |
| async_generators           | 377 ms                                                       | 328 ms: 1.15x faster                                                  |
| pylint                     | 317 ms                                                       | 278 ms: 1.14x faster                                                  |
| richards                   | 45.2 ms                                                      | 39.8 ms: 1.14x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.14x faster                                                 |
| richards_super             | 51.6 ms                                                      | 45.7 ms: 1.13x faster                                                 |
| pyflate                    | 449 ms                                                       | 398 ms: 1.13x faster                                                  |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.8 ms: 1.10x faster                                                 |
| float                      | 77.5 ms                                                      | 70.3 ms: 1.10x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 61.2 ms: 1.10x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.08 sec: 1.09x faster                                                |
| regex_compile              | 132 ms                                                       | 123 ms: 1.08x faster                                                  |
| generators                 | 28.8 ms                                                      | 26.8 ms: 1.08x faster                                                 |
| scimark_fft                | 349 ms                                                       | 326 ms: 1.07x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.67 ms: 1.06x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.8 ms: 1.06x faster                                                 |
| thrift                     | 778 us                                                       | 737 us: 1.06x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.4 ms: 1.06x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.2 ms: 1.05x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                |
| telco                      | 7.82 ms                                                      | 7.49 ms: 1.04x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.04x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.52 ms: 1.04x faster                                                 |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 708 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.52 sec: 1.04x faster                                                |
| xml_etree_generate         | 85.4 ms                                                      | 82.4 ms: 1.04x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.3 ms: 1.04x faster                                                 |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.6 ms: 1.03x faster                                                 |
| sympy_str                  | 275 ms                                                       | 268 ms: 1.02x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                |
| genshi_xml                 | 48.8 ms                                                      | 47.8 ms: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.7 ms: 1.02x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 207 us: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                  |
| coverage                   | 83.0 ms                                                      | 82.0 ms: 1.01x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.33 ms: 1.01x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| raytrace                   | 253 ms                                                       | 251 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.5 us: 1.01x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.25 us: 1.02x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.5 ms: 1.02x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 69.5 ms: 1.02x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.21 ms: 1.03x slower                                                 |
| nbody                      | 85.1 ms                                                      | 87.9 ms: 1.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                  |
| fannkuch                   | 370 ms                                                       | 385 ms: 1.04x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                 |
| json                       | 4.93 ms                                                      | 5.19 ms: 1.05x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.54 us: 1.06x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.9 us: 1.07x slower                                                 |
| logging_format             | 6.84 us                                                      | 7.44 us: 1.09x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 12.1 ms: 1.15x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.07 ms: 1.29x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.44x slower                                                 |
| logging_silent             | 103 ns                                                       | 465 ns: 4.53x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 98.7 ms: 8.98x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (4): sympy_expand, typing_runtime_protocols, nqueens, django_template
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250512-3.15.0a0-8cf4947/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x