# Results vs. 3.13.0rc2

- fork: python
- ref: 8cf4947b0f2d37f7ffec
- machine: linux-x86_64
- commit hash: 8cf4947
- commit date: 2025-05-12
- overall geometric mean: 1.024x slower
- HPT reliability: 96.36%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 285 ms: 1.10x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 523 ms: 1.75x faster                                                  |
| async_tree_io              | 876 ms                                                       | 551 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 227 ms: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 311 ms: 1.48x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 284 ms: 1.46x faster                                                  |
| async_tree_none            | 354 ms                                                       | 258 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 509 ms: 1.31x faster                                                  |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                 |
| pidigits       | 217 ms                                                       | 200 ms: 1.08x faster                                                  |
| nbody          | 85.1 ms                                                      | 120 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                 |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                  |
| regex_compile  | 132 ms                                                       | 144 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 86.8 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.12 sec: 1.06x slower                                                |
| unpickle_pure_python | 210 us                                                       | 230 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                 |
| json_loads           | 27.0 us                                                      | 30.4 us: 1.13x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 333 us: 1.13x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 68.3 ms: 1.15x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.3 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.61 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 55.3 ms: 1.13x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 25.6 ms: 1.19x slower                                                 |
| django_template | 34.1 ms                                                      | 40.7 ms: 1.19x slower                                                 |
| mako            | 11.3 ms                                                      | 15.4 ms: 1.36x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.77x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 523 ms: 1.75x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 1.93 ms: 1.63x faster                                                 |
| async_tree_io              | 876 ms                                                       | 551 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 227 ms: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 311 ms: 1.48x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 284 ms: 1.46x faster                                                  |
| async_tree_none            | 354 ms                                                       | 258 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 509 ms: 1.31x faster                                                  |
| deepcopy                   | 355 us                                                       | 291 us: 1.22x faster                                                  |
| go                         | 141 ms                                                       | 123 ms: 1.14x faster                                                  |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.10x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 35.6 us: 1.10x faster                                                 |
| float                      | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 86.8 ms: 1.09x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                 |
| pidigits                   | 217 ms                                                       | 200 ms: 1.08x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.08 us: 1.06x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 71.2 ms: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.00 us: 1.04x faster                                                 |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                  |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.39 sec: 1.01x faster                                                |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                  |
| generators                 | 28.8 ms                                                      | 29.4 ms: 1.02x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.6 ms: 1.02x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                |
| json                       | 4.93 ms                                                      | 5.14 ms: 1.04x slower                                                 |
| scimark_fft                | 349 ms                                                       | 365 ms: 1.04x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 773 ms: 1.05x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.12 sec: 1.06x slower                                                |
| pyflate                    | 449 ms                                                       | 481 ms: 1.07x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.61 sec: 1.07x slower                                                |
| chaos                      | 57.3 ms                                                      | 61.7 ms: 1.08x slower                                                 |
| regex_compile              | 132 ms                                                       | 144 ms: 1.09x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 230 us: 1.10x slower                                                  |
| 2to3                       | 260 ms                                                       | 285 ms: 1.10x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.58 ms: 1.10x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 86.9 ms: 1.11x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.66 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 22.2 ms: 1.12x slower                                                 |
| thrift                     | 778 us                                                       | 871 us: 1.12x slower                                                  |
| richards                   | 45.2 ms                                                      | 50.7 ms: 1.12x slower                                                 |
| richards_super             | 51.6 ms                                                      | 58.0 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                 |
| json_loads                 | 27.0 us                                                      | 30.4 us: 1.13x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.51 ms: 1.13x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 333 us: 1.13x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.54 ms: 1.13x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 55.3 ms: 1.13x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 68.3 ms: 1.15x slower                                                 |
| sympy_str                  | 275 ms                                                       | 317 ms: 1.15x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 132 ms: 1.17x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 76.5 ms: 1.17x slower                                                 |
| sympy_expand               | 457 ms                                                       | 536 ms: 1.17x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.53 ms: 1.17x slower                                                 |
| raytrace                   | 253 ms                                                       | 297 ms: 1.18x slower                                                  |
| comprehensions             | 16.5 us                                                      | 19.5 us: 1.18x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 25.6 ms: 1.19x slower                                                 |
| django_template            | 34.1 ms                                                      | 40.7 ms: 1.19x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 84.7 ms: 1.25x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 13.3 ms: 1.26x slower                                                 |
| fannkuch                   | 370 ms                                                       | 467 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 196 us: 1.27x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.81 us: 1.27x slower                                                 |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.78 us: 1.28x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.61 ms: 1.30x slower                                                 |
| coverage                   | 83.0 ms                                                      | 109 ms: 1.31x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.4 ms: 1.36x slower                                                 |
| nbody                      | 85.1 ms                                                      | 120 ms: 1.41x slower                                                  |
| python_startup             | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.12 ms: 3.39x slower                                                 |
| logging_silent             | 103 ns                                                       | 541 ns: 5.28x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.38x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.09x slower                                                          |

Benchmark hidden because not significant (2): pylint, html5lib
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250512-3.15.0a0-8cf4947-NOGIL/bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.024x slower

# HPT report

- Reliability score: 96.36% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x