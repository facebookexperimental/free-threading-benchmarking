# Results vs. 3.13.0rc2

- fork: colesbury
- ref: align_32
- machine: linux-x86_64
- commit hash: 83781d1
- commit date: 2024-12-22
- overall geometric mean: 1.203x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 357 ms: 1.38x slower                                          |
| docutils       | 2.62 sec                                                     | 2.99 sec: 1.14x slower                                        |
| html5lib       | 67.0 ms                                                      | 93.0 ms: 1.39x slower                                         |
| Geometric mean | (ref)                                                        | 1.30x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 737 ms: 1.24x faster                                          |
| async_tree_io              | 876 ms                                                       | 766 ms: 1.14x faster                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 563 ms: 1.13x faster                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 591 ms: 1.13x faster                                          |
| async_tree_none_tg         | 336 ms                                                       | 316 ms: 1.06x faster                                          |
| async_tree_memoization     | 461 ms                                                       | 435 ms: 1.06x faster                                          |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                         |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                          |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                  |

Benchmark hidden because not significant (3): async_tree_memoization_tg, asyncio_websockets, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                          |
| float          | 77.5 ms                                                      | 109 ms: 1.40x slower                                          |
| nbody          | 85.1 ms                                                      | 120 ms: 1.42x slower                                          |
| Geometric mean | (ref)                                                        | 1.18x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.63 ms: 1.17x faster                                         |
| regex_v8       | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                         |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                          |
| regex_compile  | 132 ms                                                       | 168 ms: 1.27x slower                                          |
| Geometric mean | (ref)                                                        | 1.01x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.1 ms: 1.05x faster                                         |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                          |
| json_loads           | 27.0 us                                                      | 27.5 us: 1.02x slower                                         |
| xml_etree_generate   | 85.4 ms                                                      | 97.8 ms: 1.15x slower                                         |
| tomli_loads          | 2.01 sec                                                     | 2.47 sec: 1.23x slower                                        |
| xml_etree_process    | 59.3 ms                                                      | 73.5 ms: 1.24x slower                                         |
| json_dumps           | 10.5 ms                                                      | 13.3 ms: 1.27x slower                                         |
| unpickle_pure_python | 210 us                                                       | 327 us: 1.56x slower                                          |
| pickle_pure_python   | 294 us                                                       | 495 us: 1.68x slower                                          |
| Geometric mean       | (ref)                                                        | 1.21x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.1 ms: 1.37x slower                                         |
| python_startup         | 11.0 ms                                                      | 17.0 ms: 1.55x slower                                         |
| Geometric mean         | (ref)                                                        | 1.46x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 64.0 ms: 1.31x slower                                         |
| genshi_text     | 21.5 ms                                                      | 30.2 ms: 1.40x slower                                         |
| mako            | 11.3 ms                                                      | 16.5 ms: 1.46x slower                                         |
| django_template | 34.1 ms                                                      | 51.2 ms: 1.50x slower                                         |
| Geometric mean  | (ref)                                                        | 1.42x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 737 ms: 1.24x faster                                          |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                          |
| regex_effbot               | 3.08 ms                                                      | 2.63 ms: 1.17x faster                                         |
| async_tree_io              | 876 ms                                                       | 766 ms: 1.14x faster                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 563 ms: 1.13x faster                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 591 ms: 1.13x faster                                          |
| deepcopy                   | 355 us                                                       | 326 us: 1.09x faster                                          |
| async_tree_none_tg         | 336 ms                                                       | 316 ms: 1.06x faster                                          |
| async_tree_memoization     | 461 ms                                                       | 435 ms: 1.06x faster                                          |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.1 ms: 1.05x faster                                         |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                          |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.03x faster                                          |
| sqlite_synth               | 2.21 us                                                      | 2.17 us: 1.02x faster                                         |
| regex_v8                   | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                         |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                          |
| deepcopy_memo              | 39.1 us                                                      | 39.4 us: 1.01x slower                                         |
| scimark_fft                | 349 ms                                                       | 355 ms: 1.02x slower                                          |
| json_loads                 | 27.0 us                                                      | 27.5 us: 1.02x slower                                         |
| gc_traversal               | 3.14 ms                                                      | 3.21 ms: 1.02x slower                                         |
| json                       | 4.93 ms                                                      | 5.08 ms: 1.03x slower                                         |
| pathlib                    | 19.2 ms                                                      | 19.9 ms: 1.04x slower                                         |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                         |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.97 ms: 1.05x slower                                         |
| deepcopy_reduce            | 3.11 us                                                      | 3.46 us: 1.11x slower                                         |
| bpe_tokeniser              | 4.45 sec                                                     | 4.97 sec: 1.12x slower                                        |
| telco                      | 7.82 ms                                                      | 8.80 ms: 1.12x slower                                         |
| mdp                        | 2.36 sec                                                     | 2.69 sec: 1.14x slower                                        |
| docutils                   | 2.62 sec                                                     | 2.99 sec: 1.14x slower                                        |
| xml_etree_generate         | 85.4 ms                                                      | 97.8 ms: 1.15x slower                                         |
| pylint                     | 317 ms                                                       | 364 ms: 1.15x slower                                          |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                          |
| coverage                   | 83.0 ms                                                      | 100.0 ms: 1.21x slower                                        |
| tomli_loads                | 2.01 sec                                                     | 2.47 sec: 1.23x slower                                        |
| dulwich_log                | 74.8 ms                                                      | 92.5 ms: 1.24x slower                                         |
| xml_etree_process          | 59.3 ms                                                      | 73.5 ms: 1.24x slower                                         |
| pycparser                  | 1.12 sec                                                     | 1.39 sec: 1.24x slower                                        |
| sqlglot_optimize           | 52.7 ms                                                      | 65.9 ms: 1.25x slower                                         |
| nqueens                    | 78.6 ms                                                      | 98.3 ms: 1.25x slower                                         |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.25x slower                                          |
| json_dumps                 | 10.5 ms                                                      | 13.3 ms: 1.27x slower                                         |
| regex_compile              | 132 ms                                                       | 168 ms: 1.27x slower                                          |
| generators                 | 28.8 ms                                                      | 36.7 ms: 1.27x slower                                         |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                          |
| create_gc_cycles           | 1.34 ms                                                      | 1.74 ms: 1.30x slower                                         |
| thrift                     | 778 us                                                       | 1.01 ms: 1.30x slower                                         |
| pprint_safe_repr           | 738 ms                                                       | 959 ms: 1.30x slower                                          |
| genshi_xml                 | 48.8 ms                                                      | 64.0 ms: 1.31x slower                                         |
| crypto_pyaes               | 67.9 ms                                                      | 89.3 ms: 1.31x slower                                         |
| fannkuch                   | 370 ms                                                       | 492 ms: 1.33x slower                                          |
| pprint_pformat             | 1.50 sec                                                     | 1.99 sec: 1.33x slower                                        |
| typing_runtime_protocols   | 155 us                                                       | 208 us: 1.34x slower                                          |
| python_startup_no_site     | 7.39 ms                                                      | 10.1 ms: 1.37x slower                                         |
| 2to3                       | 260 ms                                                       | 357 ms: 1.38x slower                                          |
| html5lib                   | 67.0 ms                                                      | 93.0 ms: 1.39x slower                                         |
| scimark_lu                 | 113 ms                                                       | 158 ms: 1.40x slower                                          |
| genshi_text                | 21.5 ms                                                      | 30.2 ms: 1.40x slower                                         |
| float                      | 77.5 ms                                                      | 109 ms: 1.40x slower                                          |
| nbody                      | 85.1 ms                                                      | 120 ms: 1.42x slower                                          |
| pyflate                    | 449 ms                                                       | 637 ms: 1.42x slower                                          |
| richards_super             | 51.6 ms                                                      | 73.8 ms: 1.43x slower                                         |
| richards                   | 45.2 ms                                                      | 65.9 ms: 1.46x slower                                         |
| mako                       | 11.3 ms                                                      | 16.5 ms: 1.46x slower                                         |
| django_template            | 34.1 ms                                                      | 51.2 ms: 1.50x slower                                         |
| sympy_integrate            | 19.8 ms                                                      | 29.7 ms: 1.50x slower                                         |
| logging_simple             | 6.16 us                                                      | 9.23 us: 1.50x slower                                         |
| logging_format             | 6.84 us                                                      | 10.4 us: 1.52x slower                                         |
| python_startup             | 11.0 ms                                                      | 17.0 ms: 1.55x slower                                         |
| unpickle_pure_python       | 210 us                                                       | 327 us: 1.56x slower                                          |
| hexiom                     | 5.99 ms                                                      | 9.37 ms: 1.56x slower                                         |
| scimark_sor                | 134 ms                                                       | 211 ms: 1.57x slower                                          |
| scimark_monte_carlo        | 65.4 ms                                                      | 104 ms: 1.59x slower                                          |
| comprehensions             | 16.5 us                                                      | 26.5 us: 1.61x slower                                         |
| chaos                      | 57.3 ms                                                      | 93.6 ms: 1.63x slower                                         |
| go                         | 141 ms                                                       | 231 ms: 1.64x slower                                          |
| pickle_pure_python         | 294 us                                                       | 495 us: 1.68x slower                                          |
| logging_silent             | 103 ns                                                       | 177 ns: 1.73x slower                                          |
| sqlglot_transpile          | 1.56 ms                                                      | 2.69 ms: 1.73x slower                                         |
| sympy_str                  | 275 ms                                                       | 478 ms: 1.74x slower                                          |
| sqlglot_parse              | 1.25 ms                                                      | 2.31 ms: 1.85x slower                                         |
| raytrace                   | 253 ms                                                       | 477 ms: 1.89x slower                                          |
| sympy_expand               | 457 ms                                                       | 957 ms: 2.09x slower                                          |
| sympy_sum                  | 156 ms                                                       | 350 ms: 2.25x slower                                          |
| deltablue                  | 3.12 ms                                                      | 7.15 ms: 2.29x slower                                         |
| bench_thread_pool          | 919 us                                                       | 3.40 ms: 3.70x slower                                         |
| bench_mp_pool              | 11.0 ms                                                      | 107 ms: 9.71x slower                                          |
| Geometric mean             | (ref)                                                        | 1.30x slower                                                  |

Benchmark hidden because not significant (3): async_tree_memoization_tg, asyncio_websockets, async_tree_none
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241222-3.14.0a3+-83781d1-NOGIL/bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.203x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.32x