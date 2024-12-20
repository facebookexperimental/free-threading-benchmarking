# Results vs. 3.13.0rc2

- fork: python
- ref: 78ffba4221dcb2e39fd5
- machine: linux-x86_64
- commit hash: 78ffba4
- commit date: 2024-12-20
- overall geometric mean: 1.215x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 360 ms: 1.39x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.05 sec: 1.16x slower                                                 |
| html5lib       | 67.0 ms                                                      | 91.4 ms: 1.36x slower                                                  |
| Geometric mean | (ref)                                                        | 1.30x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 735 ms: 1.24x faster                                                   |
| async_tree_io              | 876 ms                                                       | 757 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 572 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 598 ms: 1.11x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 430 ms: 1.07x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 318 ms: 1.06x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 402 ms: 1.03x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                  |
| async_generators           | 377 ms                                                       | 445 ms: 1.18x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (2): async_tree_none, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                   |
| float          | 77.5 ms                                                      | 113 ms: 1.46x slower                                                   |
| nbody          | 85.1 ms                                                      | 127 ms: 1.49x slower                                                   |
| Geometric mean | (ref)                                                        | 1.22x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 24.8 ms: 1.09x slower                                                  |
| regex_compile  | 132 ms                                                       | 170 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 97.2 ms: 1.14x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 73.4 ms: 1.24x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.53 sec: 1.26x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 14.3 ms: 1.35x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 330 us: 1.57x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 500 us: 1.70x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| python_startup         | 11.0 ms                                                      | 17.2 ms: 1.57x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.7 ms: 1.31x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 30.7 ms: 1.42x slower                                                  |
| django_template | 34.1 ms                                                      | 49.6 ms: 1.45x slower                                                  |
| mako            | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.42x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 735 ms: 1.24x faster                                                   |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                   |
| async_tree_io              | 876 ms                                                       | 757 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 572 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 598 ms: 1.11x faster                                                   |
| deepcopy                   | 355 us                                                       | 323 us: 1.10x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 430 ms: 1.07x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 318 ms: 1.06x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.14 us: 1.03x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 402 ms: 1.03x faster                                                   |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                  |
| deepcopy_memo              | 39.1 us                                                      | 39.9 us: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.04 ms: 1.02x slower                                                  |
| pathlib                    | 19.2 ms                                                      | 19.8 ms: 1.03x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.26 ms: 1.04x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.04x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.40 us: 1.09x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.8 ms: 1.09x slower                                                  |
| scimark_fft                | 349 ms                                                       | 388 ms: 1.11x slower                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.99 sec: 1.12x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.81 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 97.2 ms: 1.14x slower                                                  |
| pylint                     | 317 ms                                                       | 365 ms: 1.15x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.47 ms: 1.16x slower                                                  |
| docutils                   | 2.62 sec                                                     | 3.05 sec: 1.16x slower                                                 |
| async_generators           | 377 ms                                                       | 445 ms: 1.18x slower                                                   |
| mdp                        | 2.36 sec                                                     | 2.81 sec: 1.19x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 90.1 ms: 1.20x slower                                                  |
| coverage                   | 83.0 ms                                                      | 102 ms: 1.23x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.38 sec: 1.24x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 73.4 ms: 1.24x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 98.0 ms: 1.25x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 65.9 ms: 1.25x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.25x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.53 sec: 1.26x slower                                                 |
| regex_compile              | 132 ms                                                       | 170 ms: 1.28x slower                                                   |
| thrift                     | 778 us                                                       | 1.00 ms: 1.29x slower                                                  |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 956 ms: 1.30x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 63.7 ms: 1.31x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.7 ms: 1.32x slower                                                  |
| fannkuch                   | 370 ms                                                       | 490 ms: 1.33x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 206 us: 1.33x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.99 sec: 1.33x slower                                                 |
| generators                 | 28.8 ms                                                      | 38.4 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.79 ms: 1.34x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 14.3 ms: 1.35x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 91.4 ms: 1.36x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| 2to3                       | 260 ms                                                       | 360 ms: 1.39x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 158 ms: 1.40x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 30.7 ms: 1.42x slower                                                  |
| django_template            | 34.1 ms                                                      | 49.6 ms: 1.45x slower                                                  |
| float                      | 77.5 ms                                                      | 113 ms: 1.46x slower                                                   |
| pyflate                    | 449 ms                                                       | 655 ms: 1.46x slower                                                   |
| richards_super             | 51.6 ms                                                      | 76.4 ms: 1.48x slower                                                  |
| nbody                      | 85.1 ms                                                      | 127 ms: 1.49x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 29.6 ms: 1.49x slower                                                  |
| logging_simple             | 6.16 us                                                      | 9.21 us: 1.49x slower                                                  |
| logging_format             | 6.84 us                                                      | 10.3 us: 1.50x slower                                                  |
| mako                       | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                  |
| richards                   | 45.2 ms                                                      | 69.1 ms: 1.53x slower                                                  |
| python_startup             | 11.0 ms                                                      | 17.2 ms: 1.57x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 330 us: 1.57x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 9.66 ms: 1.61x slower                                                  |
| scimark_sor                | 134 ms                                                       | 219 ms: 1.63x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 107 ms: 1.63x slower                                                   |
| chaos                      | 57.3 ms                                                      | 96.1 ms: 1.68x slower                                                  |
| comprehensions             | 16.5 us                                                      | 27.9 us: 1.69x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 500 us: 1.70x slower                                                   |
| go                         | 141 ms                                                       | 244 ms: 1.73x slower                                                   |
| sympy_str                  | 275 ms                                                       | 478 ms: 1.74x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 2.73 ms: 1.75x slower                                                  |
| logging_silent             | 103 ns                                                       | 184 ns: 1.79x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 2.38 ms: 1.90x slower                                                  |
| raytrace                   | 253 ms                                                       | 497 ms: 1.97x slower                                                   |
| sympy_expand               | 457 ms                                                       | 951 ms: 2.08x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 349 ms: 2.24x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 7.67 ms: 2.45x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.38 ms: 3.68x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.79x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.32x slower                                                           |

Benchmark hidden because not significant (3): async_tree_none, spectral_norm, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241220-3.14.0a3+-78ffba4-NOGIL/bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.215x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.32x