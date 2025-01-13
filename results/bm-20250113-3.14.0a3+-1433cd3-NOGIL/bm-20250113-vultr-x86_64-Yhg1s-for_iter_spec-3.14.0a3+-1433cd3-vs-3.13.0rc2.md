# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: for_iter_spec
- machine: linux-x86_64
- commit hash: 1433cd3
- commit date: 2025-01-13
- overall geometric mean: 1.188x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 343 ms: 1.32x slower                                           |
| docutils       | 2.62 sec                                                     | 3.00 sec: 1.15x slower                                         |
| html5lib       | 67.0 ms                                                      | 88.7 ms: 1.32x slower                                          |
| Geometric mean | (ref)                                                        | 1.26x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 733 ms: 1.25x faster                                           |
| async_tree_io              | 876 ms                                                       | 760 ms: 1.15x faster                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 575 ms: 1.11x faster                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 603 ms: 1.11x faster                                           |
| async_tree_memoization     | 461 ms                                                       | 429 ms: 1.07x faster                                           |
| async_tree_none_tg         | 336 ms                                                       | 314 ms: 1.07x faster                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 395 ms: 1.05x faster                                           |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.01x faster                                           |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                          |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                           |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                   |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 182 ms: 1.19x faster                                           |
| float          | 77.5 ms                                                      | 107 ms: 1.39x slower                                           |
| nbody          | 85.1 ms                                                      | 130 ms: 1.52x slower                                           |
| Geometric mean | (ref)                                                        | 1.21x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.69 ms: 1.14x faster                                          |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                           |
| regex_v8       | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                          |
| regex_compile  | 132 ms                                                       | 166 ms: 1.26x slower                                           |
| Geometric mean | (ref)                                                        | 1.04x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.8 ms: 1.06x faster                                          |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                           |
| json_loads           | 27.0 us                                                      | 28.8 us: 1.07x slower                                          |
| xml_etree_generate   | 85.4 ms                                                      | 98.2 ms: 1.15x slower                                          |
| tomli_loads          | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                         |
| xml_etree_process    | 59.3 ms                                                      | 73.9 ms: 1.25x slower                                          |
| json_dumps           | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                          |
| unpickle_pure_python | 210 us                                                       | 322 us: 1.53x slower                                           |
| pickle_pure_python   | 294 us                                                       | 492 us: 1.67x slower                                           |
| Geometric mean       | (ref)                                                        | 1.21x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.80 ms: 1.33x slower                                          |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                          |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.2 ms: 1.23x slower                                          |
| genshi_text     | 21.5 ms                                                      | 29.4 ms: 1.37x slower                                          |
| django_template | 34.1 ms                                                      | 50.1 ms: 1.47x slower                                          |
| mako            | 11.3 ms                                                      | 17.2 ms: 1.51x slower                                          |
| Geometric mean  | (ref)                                                        | 1.39x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 733 ms: 1.25x faster                                           |
| pidigits                   | 217 ms                                                       | 182 ms: 1.19x faster                                           |
| async_tree_io              | 876 ms                                                       | 760 ms: 1.15x faster                                           |
| regex_effbot               | 3.08 ms                                                      | 2.69 ms: 1.14x faster                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 575 ms: 1.11x faster                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 603 ms: 1.11x faster                                           |
| deepcopy                   | 355 us                                                       | 325 us: 1.09x faster                                           |
| async_tree_memoization     | 461 ms                                                       | 429 ms: 1.07x faster                                           |
| async_tree_none_tg         | 336 ms                                                       | 314 ms: 1.07x faster                                           |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.8 ms: 1.06x faster                                          |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                           |
| sqlite_synth               | 2.21 us                                                      | 2.10 us: 1.05x faster                                          |
| async_tree_memoization_tg  | 414 ms                                                       | 395 ms: 1.05x faster                                           |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.01x faster                                           |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                           |
| pathlib                    | 19.2 ms                                                      | 19.4 ms: 1.01x slower                                          |
| spectral_norm              | 111 ms                                                       | 112 ms: 1.01x slower                                           |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                          |
| json                       | 4.93 ms                                                      | 5.11 ms: 1.04x slower                                          |
| deepcopy_memo              | 39.1 us                                                      | 40.9 us: 1.05x slower                                          |
| regex_v8                   | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                          |
| gc_traversal               | 3.14 ms                                                      | 3.30 ms: 1.05x slower                                          |
| json_loads                 | 27.0 us                                                      | 28.8 us: 1.07x slower                                          |
| pylint                     | 317 ms                                                       | 342 ms: 1.08x slower                                           |
| deepcopy_reduce            | 3.11 us                                                      | 3.38 us: 1.09x slower                                          |
| scimark_fft                | 349 ms                                                       | 380 ms: 1.09x slower                                           |
| telco                      | 7.82 ms                                                      | 8.61 ms: 1.10x slower                                          |
| bpe_tokeniser              | 4.45 sec                                                     | 4.97 sec: 1.12x slower                                         |
| docutils                   | 2.62 sec                                                     | 3.00 sec: 1.15x slower                                         |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.41 ms: 1.15x slower                                          |
| xml_etree_generate         | 85.4 ms                                                      | 98.2 ms: 1.15x slower                                          |
| tomli_loads                | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                         |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                           |
| coverage                   | 83.0 ms                                                      | 98.5 ms: 1.19x slower                                          |
| pycparser                  | 1.12 sec                                                     | 1.33 sec: 1.19x slower                                         |
| dulwich_log                | 74.8 ms                                                      | 89.7 ms: 1.20x slower                                          |
| mdp                        | 2.36 sec                                                     | 2.86 sec: 1.21x slower                                         |
| nqueens                    | 78.6 ms                                                      | 96.6 ms: 1.23x slower                                          |
| genshi_xml                 | 48.8 ms                                                      | 60.2 ms: 1.23x slower                                          |
| xml_etree_process          | 59.3 ms                                                      | 73.9 ms: 1.25x slower                                          |
| sqlglot_normalize          | 106 ms                                                       | 132 ms: 1.25x slower                                           |
| sympy_sum                  | 156 ms                                                       | 194 ms: 1.25x slower                                           |
| regex_compile              | 132 ms                                                       | 166 ms: 1.26x slower                                           |
| sqlglot_optimize           | 52.7 ms                                                      | 66.5 ms: 1.26x slower                                          |
| sympy_integrate            | 19.8 ms                                                      | 25.1 ms: 1.26x slower                                          |
| pprint_safe_repr           | 738 ms                                                       | 936 ms: 1.27x slower                                           |
| sympy_expand               | 457 ms                                                       | 582 ms: 1.27x slower                                           |
| sympy_str                  | 275 ms                                                       | 354 ms: 1.29x slower                                           |
| thrift                     | 778 us                                                       | 1.01 ms: 1.30x slower                                          |
| generators                 | 28.8 ms                                                      | 37.4 ms: 1.30x slower                                          |
| meteor_contest             | 102 ms                                                       | 132 ms: 1.30x slower                                           |
| pprint_pformat             | 1.50 sec                                                     | 1.95 sec: 1.30x slower                                         |
| fannkuch                   | 370 ms                                                       | 486 ms: 1.31x slower                                           |
| crypto_pyaes               | 67.9 ms                                                      | 89.2 ms: 1.31x slower                                          |
| 2to3                       | 260 ms                                                       | 343 ms: 1.32x slower                                           |
| json_dumps                 | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                          |
| html5lib                   | 67.0 ms                                                      | 88.7 ms: 1.32x slower                                          |
| python_startup_no_site     | 7.39 ms                                                      | 9.80 ms: 1.33x slower                                          |
| typing_runtime_protocols   | 155 us                                                       | 205 us: 1.33x slower                                           |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                          |
| genshi_text                | 21.5 ms                                                      | 29.4 ms: 1.37x slower                                          |
| scimark_lu                 | 113 ms                                                       | 154 ms: 1.37x slower                                           |
| float                      | 77.5 ms                                                      | 107 ms: 1.39x slower                                           |
| pyflate                    | 449 ms                                                       | 637 ms: 1.42x slower                                           |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                          |
| richards                   | 45.2 ms                                                      | 65.5 ms: 1.45x slower                                          |
| logging_simple             | 6.16 us                                                      | 9.04 us: 1.47x slower                                          |
| django_template            | 34.1 ms                                                      | 50.1 ms: 1.47x slower                                          |
| richards_super             | 51.6 ms                                                      | 76.5 ms: 1.48x slower                                          |
| logging_format             | 6.84 us                                                      | 10.1 us: 1.48x slower                                          |
| scimark_sor                | 134 ms                                                       | 202 ms: 1.50x slower                                           |
| mako                       | 11.3 ms                                                      | 17.2 ms: 1.51x slower                                          |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.52x slower                                           |
| unpickle_pure_python       | 210 us                                                       | 322 us: 1.53x slower                                           |
| hexiom                     | 5.99 ms                                                      | 9.28 ms: 1.55x slower                                          |
| scimark_monte_carlo        | 65.4 ms                                                      | 102 ms: 1.57x slower                                           |
| go                         | 141 ms                                                       | 231 ms: 1.64x slower                                           |
| chaos                      | 57.3 ms                                                      | 94.7 ms: 1.65x slower                                          |
| pickle_pure_python         | 294 us                                                       | 492 us: 1.67x slower                                           |
| comprehensions             | 16.5 us                                                      | 27.9 us: 1.70x slower                                          |
| sqlglot_transpile          | 1.56 ms                                                      | 2.68 ms: 1.72x slower                                          |
| logging_silent             | 103 ns                                                       | 182 ns: 1.78x slower                                           |
| sqlglot_parse              | 1.25 ms                                                      | 2.32 ms: 1.86x slower                                          |
| raytrace                   | 253 ms                                                       | 490 ms: 1.94x slower                                           |
| deltablue                  | 3.12 ms                                                      | 7.35 ms: 2.35x slower                                          |
| bench_thread_pool          | 919 us                                                       | 3.36 ms: 3.65x slower                                          |
| bench_mp_pool              | 11.0 ms                                                      | 100 ms: 9.11x slower                                           |
| Geometric mean             | (ref)                                                        | 1.28x slower                                                   |

Benchmark hidden because not significant (1): async_tree_none
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250113-3.14.0a3+-1433cd3-NOGIL/bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.188x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.32x