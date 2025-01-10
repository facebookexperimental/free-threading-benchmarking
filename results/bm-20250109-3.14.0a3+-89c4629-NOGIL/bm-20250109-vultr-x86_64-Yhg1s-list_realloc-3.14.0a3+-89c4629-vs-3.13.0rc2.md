# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: list_realloc
- machine: linux-x86_64
- commit hash: 89c4629
- commit date: 2025-01-09
- overall geometric mean: 1.189x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 346 ms: 1.33x slower                                          |
| docutils       | 2.62 sec                                                     | 3.01 sec: 1.15x slower                                        |
| html5lib       | 67.0 ms                                                      | 90.3 ms: 1.35x slower                                         |
| Geometric mean | (ref)                                                        | 1.27x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 737 ms: 1.24x faster                                          |
| async_tree_io              | 876 ms                                                       | 759 ms: 1.15x faster                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 566 ms: 1.13x faster                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 595 ms: 1.12x faster                                          |
| async_tree_memoization     | 461 ms                                                       | 430 ms: 1.07x faster                                          |
| async_tree_none_tg         | 336 ms                                                       | 316 ms: 1.06x faster                                          |
| async_tree_memoization_tg  | 414 ms                                                       | 397 ms: 1.04x faster                                          |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                         |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                          |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                          |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                  |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                          |
| float          | 77.5 ms                                                      | 106 ms: 1.37x slower                                          |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                          |
| Geometric mean | (ref)                                                        | 1.21x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                         |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                          |
| regex_v8       | 22.7 ms                                                      | 25.4 ms: 1.12x slower                                         |
| regex_compile  | 132 ms                                                       | 167 ms: 1.26x slower                                          |
| Geometric mean | (ref)                                                        | 1.08x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.3 ms: 1.06x faster                                         |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                          |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                         |
| xml_etree_generate   | 85.4 ms                                                      | 98.3 ms: 1.15x slower                                         |
| tomli_loads          | 2.01 sec                                                     | 2.37 sec: 1.18x slower                                        |
| xml_etree_process    | 59.3 ms                                                      | 74.1 ms: 1.25x slower                                         |
| json_dumps           | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                         |
| unpickle_pure_python | 210 us                                                       | 324 us: 1.54x slower                                          |
| pickle_pure_python   | 294 us                                                       | 486 us: 1.65x slower                                          |
| Geometric mean       | (ref)                                                        | 1.20x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.79 ms: 1.32x slower                                         |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                         |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.2 ms: 1.30x slower                                         |
| genshi_text     | 21.5 ms                                                      | 30.4 ms: 1.41x slower                                         |
| django_template | 34.1 ms                                                      | 49.7 ms: 1.46x slower                                         |
| mako            | 11.3 ms                                                      | 17.0 ms: 1.50x slower                                         |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 737 ms: 1.24x faster                                          |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                          |
| async_tree_io              | 876 ms                                                       | 759 ms: 1.15x faster                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 566 ms: 1.13x faster                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 595 ms: 1.12x faster                                          |
| deepcopy                   | 355 us                                                       | 325 us: 1.09x faster                                          |
| regex_effbot               | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                         |
| async_tree_memoization     | 461 ms                                                       | 430 ms: 1.07x faster                                          |
| async_tree_none_tg         | 336 ms                                                       | 316 ms: 1.06x faster                                          |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.3 ms: 1.06x faster                                         |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                          |
| sqlite_synth               | 2.21 us                                                      | 2.11 us: 1.05x faster                                         |
| async_tree_memoization_tg  | 414 ms                                                       | 397 ms: 1.04x faster                                          |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.01x faster                                         |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                          |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                          |
| pathlib                    | 19.2 ms                                                      | 19.5 ms: 1.02x slower                                         |
| json                       | 4.93 ms                                                      | 5.09 ms: 1.03x slower                                         |
| regex_dna                  | 180 ms                                                       | 187 ms: 1.04x slower                                          |
| deepcopy_memo              | 39.1 us                                                      | 40.6 us: 1.04x slower                                         |
| gc_traversal               | 3.14 ms                                                      | 3.29 ms: 1.05x slower                                         |
| json_loads                 | 27.0 us                                                      | 28.6 us: 1.06x slower                                         |
| scimark_fft                | 349 ms                                                       | 378 ms: 1.08x slower                                          |
| pylint                     | 317 ms                                                       | 343 ms: 1.08x slower                                          |
| deepcopy_reduce            | 3.11 us                                                      | 3.38 us: 1.09x slower                                         |
| telco                      | 7.82 ms                                                      | 8.58 ms: 1.10x slower                                         |
| bpe_tokeniser              | 4.45 sec                                                     | 4.93 sec: 1.11x slower                                        |
| regex_v8                   | 22.7 ms                                                      | 25.4 ms: 1.12x slower                                         |
| xml_etree_generate         | 85.4 ms                                                      | 98.3 ms: 1.15x slower                                         |
| docutils                   | 2.62 sec                                                     | 3.01 sec: 1.15x slower                                        |
| mdp                        | 2.36 sec                                                     | 2.73 sec: 1.16x slower                                        |
| tomli_loads                | 2.01 sec                                                     | 2.37 sec: 1.18x slower                                        |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                          |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.59 ms: 1.19x slower                                         |
| coverage                   | 83.0 ms                                                      | 98.7 ms: 1.19x slower                                         |
| dulwich_log                | 74.8 ms                                                      | 90.4 ms: 1.21x slower                                         |
| pycparser                  | 1.12 sec                                                     | 1.35 sec: 1.21x slower                                        |
| nqueens                    | 78.6 ms                                                      | 96.4 ms: 1.23x slower                                         |
| sympy_sum                  | 156 ms                                                       | 193 ms: 1.24x slower                                          |
| xml_etree_process          | 59.3 ms                                                      | 74.1 ms: 1.25x slower                                         |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.26x slower                                          |
| regex_compile              | 132 ms                                                       | 167 ms: 1.26x slower                                          |
| sympy_integrate            | 19.8 ms                                                      | 25.0 ms: 1.26x slower                                         |
| sqlglot_optimize           | 52.7 ms                                                      | 66.9 ms: 1.27x slower                                         |
| sympy_expand               | 457 ms                                                       | 582 ms: 1.27x slower                                          |
| pprint_safe_repr           | 738 ms                                                       | 946 ms: 1.28x slower                                          |
| sympy_str                  | 275 ms                                                       | 353 ms: 1.29x slower                                          |
| thrift                     | 778 us                                                       | 1.01 ms: 1.29x slower                                         |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                          |
| genshi_xml                 | 48.8 ms                                                      | 63.2 ms: 1.30x slower                                         |
| fannkuch                   | 370 ms                                                       | 484 ms: 1.31x slower                                          |
| pprint_pformat             | 1.50 sec                                                     | 1.97 sec: 1.31x slower                                        |
| crypto_pyaes               | 67.9 ms                                                      | 89.4 ms: 1.32x slower                                         |
| json_dumps                 | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                         |
| python_startup_no_site     | 7.39 ms                                                      | 9.79 ms: 1.32x slower                                         |
| typing_runtime_protocols   | 155 us                                                       | 205 us: 1.33x slower                                          |
| 2to3                       | 260 ms                                                       | 346 ms: 1.33x slower                                          |
| generators                 | 28.8 ms                                                      | 38.6 ms: 1.34x slower                                         |
| html5lib                   | 67.0 ms                                                      | 90.3 ms: 1.35x slower                                         |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                         |
| float                      | 77.5 ms                                                      | 106 ms: 1.37x slower                                          |
| pyflate                    | 449 ms                                                       | 632 ms: 1.41x slower                                          |
| genshi_text                | 21.5 ms                                                      | 30.4 ms: 1.41x slower                                         |
| scimark_lu                 | 113 ms                                                       | 160 ms: 1.42x slower                                          |
| python_startup             | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                         |
| richards                   | 45.2 ms                                                      | 65.1 ms: 1.44x slower                                         |
| logging_simple             | 6.16 us                                                      | 8.90 us: 1.44x slower                                         |
| logging_format             | 6.84 us                                                      | 9.96 us: 1.46x slower                                         |
| django_template            | 34.1 ms                                                      | 49.7 ms: 1.46x slower                                         |
| mako                       | 11.3 ms                                                      | 17.0 ms: 1.50x slower                                         |
| richards_super             | 51.6 ms                                                      | 77.5 ms: 1.50x slower                                         |
| scimark_sor                | 134 ms                                                       | 202 ms: 1.51x slower                                          |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                          |
| hexiom                     | 5.99 ms                                                      | 9.21 ms: 1.54x slower                                         |
| unpickle_pure_python       | 210 us                                                       | 324 us: 1.54x slower                                          |
| scimark_monte_carlo        | 65.4 ms                                                      | 103 ms: 1.58x slower                                          |
| go                         | 141 ms                                                       | 231 ms: 1.64x slower                                          |
| pickle_pure_python         | 294 us                                                       | 486 us: 1.65x slower                                          |
| comprehensions             | 16.5 us                                                      | 27.3 us: 1.66x slower                                         |
| chaos                      | 57.3 ms                                                      | 95.3 ms: 1.66x slower                                         |
| sqlglot_transpile          | 1.56 ms                                                      | 2.66 ms: 1.70x slower                                         |
| logging_silent             | 103 ns                                                       | 179 ns: 1.75x slower                                          |
| sqlglot_parse              | 1.25 ms                                                      | 2.30 ms: 1.84x slower                                         |
| raytrace                   | 253 ms                                                       | 491 ms: 1.94x slower                                          |
| deltablue                  | 3.12 ms                                                      | 7.13 ms: 2.28x slower                                         |
| bench_thread_pool          | 919 us                                                       | 3.38 ms: 3.68x slower                                         |
| bench_mp_pool              | 11.0 ms                                                      | 100 ms: 9.11x slower                                          |
| Geometric mean             | (ref)                                                        | 1.28x slower                                                  |

Benchmark hidden because not significant (1): async_tree_none
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250109-3.14.0a3+-89c4629-NOGIL/bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.189x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.33x