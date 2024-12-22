# Results vs. 3.13.0rc2

- fork: python
- ref: f420bdd29fbc1a97ad20
- machine: linux-x86_64
- commit hash: f420bdd
- commit date: 2024-12-22
- overall geometric mean: 1.213x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 360 ms: 1.39x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.03 sec: 1.16x slower                                                 |
| html5lib       | 67.0 ms                                                      | 94.6 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                        | 1.31x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 734 ms: 1.24x faster                                                   |
| async_tree_io              | 876 ms                                                       | 754 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 593 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 569 ms: 1.12x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 426 ms: 1.08x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 317 ms: 1.06x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 401 ms: 1.03x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                  |
| async_generators           | 377 ms                                                       | 450 ms: 1.19x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (2): async_tree_none, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| float          | 77.5 ms                                                      | 113 ms: 1.46x slower                                                   |
| nbody          | 85.1 ms                                                      | 128 ms: 1.51x slower                                                   |
| Geometric mean | (ref)                                                        | 1.23x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                  |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                  |
| regex_compile  | 132 ms                                                       | 169 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 98.1 ms: 1.15x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 73.8 ms: 1.24x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.56 sec: 1.28x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 14.1 ms: 1.33x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 326 us: 1.55x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 503 us: 1.71x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| python_startup         | 11.0 ms                                                      | 17.2 ms: 1.57x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.4 ms: 1.30x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 30.6 ms: 1.42x slower                                                  |
| django_template | 34.1 ms                                                      | 49.9 ms: 1.46x slower                                                  |
| mako            | 11.3 ms                                                      | 16.9 ms: 1.49x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.42x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 734 ms: 1.24x faster                                                   |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| async_tree_io              | 876 ms                                                       | 754 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 593 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 569 ms: 1.12x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 426 ms: 1.08x faster                                                   |
| deepcopy                   | 355 us                                                       | 329 us: 1.08x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 317 ms: 1.06x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 401 ms: 1.03x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.15 us: 1.03x faster                                                  |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                                   |
| pathlib                    | 19.2 ms                                                      | 19.6 ms: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                  |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.04x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.28 ms: 1.04x slower                                                  |
| deepcopy_memo              | 39.1 us                                                      | 41.0 us: 1.05x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                  |
| scimark_fft                | 349 ms                                                       | 381 ms: 1.09x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.72 ms: 1.11x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.47 us: 1.11x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 5.03 sec: 1.13x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.69 sec: 1.14x slower                                                 |
| pylint                     | 317 ms                                                       | 364 ms: 1.15x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 98.1 ms: 1.15x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.45 ms: 1.16x slower                                                  |
| docutils                   | 2.62 sec                                                     | 3.03 sec: 1.16x slower                                                 |
| async_generators           | 377 ms                                                       | 450 ms: 1.19x slower                                                   |
| coverage                   | 83.0 ms                                                      | 100.0 ms: 1.20x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 91.2 ms: 1.22x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 73.8 ms: 1.24x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 65.8 ms: 1.25x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.40 sec: 1.25x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.25x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 99.9 ms: 1.27x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.56 sec: 1.28x slower                                                 |
| regex_compile              | 132 ms                                                       | 169 ms: 1.28x slower                                                   |
| thrift                     | 778 us                                                       | 999 us: 1.28x slower                                                   |
| meteor_contest             | 102 ms                                                       | 132 ms: 1.30x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 63.4 ms: 1.30x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 961 ms: 1.30x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 205 us: 1.32x slower                                                   |
| fannkuch                   | 370 ms                                                       | 492 ms: 1.33x slower                                                   |
| generators                 | 28.8 ms                                                      | 38.3 ms: 1.33x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 90.4 ms: 1.33x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.99 sec: 1.33x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 14.1 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.81 ms: 1.35x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| 2to3                       | 260 ms                                                       | 360 ms: 1.39x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 158 ms: 1.41x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 94.6 ms: 1.41x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 30.6 ms: 1.42x slower                                                  |
| richards_super             | 51.6 ms                                                      | 74.4 ms: 1.44x slower                                                  |
| pyflate                    | 449 ms                                                       | 653 ms: 1.46x slower                                                   |
| float                      | 77.5 ms                                                      | 113 ms: 1.46x slower                                                   |
| richards                   | 45.2 ms                                                      | 66.1 ms: 1.46x slower                                                  |
| django_template            | 34.1 ms                                                      | 49.9 ms: 1.46x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.9 ms: 1.49x slower                                                  |
| logging_format             | 6.84 us                                                      | 10.2 us: 1.50x slower                                                  |
| logging_simple             | 6.16 us                                                      | 9.23 us: 1.50x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 29.8 ms: 1.50x slower                                                  |
| nbody                      | 85.1 ms                                                      | 128 ms: 1.51x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 326 us: 1.55x slower                                                   |
| python_startup             | 11.0 ms                                                      | 17.2 ms: 1.57x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 9.52 ms: 1.59x slower                                                  |
| scimark_sor                | 134 ms                                                       | 217 ms: 1.61x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 106 ms: 1.63x slower                                                   |
| comprehensions             | 16.5 us                                                      | 27.1 us: 1.65x slower                                                  |
| chaos                      | 57.3 ms                                                      | 96.4 ms: 1.68x slower                                                  |
| go                         | 141 ms                                                       | 239 ms: 1.70x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 503 us: 1.71x slower                                                   |
| logging_silent             | 103 ns                                                       | 177 ns: 1.73x slower                                                   |
| sympy_str                  | 275 ms                                                       | 478 ms: 1.74x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 2.72 ms: 1.75x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 2.34 ms: 1.87x slower                                                  |
| raytrace                   | 253 ms                                                       | 489 ms: 1.93x slower                                                   |
| sympy_expand               | 457 ms                                                       | 961 ms: 2.10x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 351 ms: 2.26x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 7.31 ms: 2.34x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.39 ms: 3.69x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.82x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.32x slower                                                           |

Benchmark hidden because not significant (2): async_tree_none, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241222-3.14.0a3+-f420bdd-NOGIL/bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.213x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.32x