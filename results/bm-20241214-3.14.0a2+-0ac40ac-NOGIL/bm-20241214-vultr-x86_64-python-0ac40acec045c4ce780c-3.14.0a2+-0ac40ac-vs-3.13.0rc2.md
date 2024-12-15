# Results vs. 3.13.0rc2

- fork: python
- ref: 0ac40acec045c4ce780c
- machine: linux-x86_64
- commit hash: 0ac40ac
- commit date: 2024-12-14
- overall geometric mean: 1.237x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 363 ms: 1.40x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.06 sec: 1.17x slower                                                 |
| html5lib       | 67.0 ms                                                      | 96.7 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                        | 1.33x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 791 ms: 1.15x faster                                                   |
| async_tree_io              | 876 ms                                                       | 807 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 625 ms: 1.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 604 ms: 1.06x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 345 ms: 1.03x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 431 ms: 1.04x slower                                                   |
| async_tree_none            | 354 ms                                                       | 374 ms: 1.06x slower                                                   |
| async_generators           | 377 ms                                                       | 455 ms: 1.21x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (2): async_tree_memoization, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                   |
| nbody          | 85.1 ms                                                      | 131 ms: 1.55x slower                                                   |
| float          | 77.5 ms                                                      | 134 ms: 1.73x slower                                                   |
| Geometric mean | (ref)                                                        | 1.31x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                  |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 25.2 ms: 1.11x slower                                                  |
| regex_compile  | 132 ms                                                       | 175 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.6 ms: 1.06x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.05x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 97.0 ms: 1.14x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.60 sec: 1.29x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 78.8 ms: 1.33x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 14.0 ms: 1.33x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 335 us: 1.60x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 501 us: 1.70x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.1 ms: 1.29x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 31.0 ms: 1.44x slower                                                  |
| django_template | 34.1 ms                                                      | 49.3 ms: 1.45x slower                                                  |
| mako            | 11.3 ms                                                      | 16.9 ms: 1.49x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.42x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 791 ms: 1.15x faster                                                   |
| deepcopy                   | 355 us                                                       | 318 us: 1.12x faster                                                   |
| async_tree_io              | 876 ms                                                       | 807 ms: 1.09x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 625 ms: 1.07x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.6 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 604 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 39.4 us: 1.01x slower                                                  |
| json                       | 4.93 ms                                                      | 5.03 ms: 1.02x slower                                                  |
| spectral_norm              | 111 ms                                                       | 114 ms: 1.03x slower                                                   |
| async_tree_none_tg         | 336 ms                                                       | 345 ms: 1.03x slower                                                   |
| pathlib                    | 19.2 ms                                                      | 19.8 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                                  |
| regex_dna                  | 180 ms                                                       | 187 ms: 1.04x slower                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 431 ms: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.5 us: 1.05x slower                                                  |
| async_tree_none            | 354 ms                                                       | 374 ms: 1.06x slower                                                   |
| scimark_fft                | 349 ms                                                       | 378 ms: 1.08x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.58 ms: 1.10x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.46 us: 1.11x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 25.2 ms: 1.11x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 5.00 sec: 1.12x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 97.0 ms: 1.14x slower                                                  |
| pylint                     | 317 ms                                                       | 369 ms: 1.16x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.51 ms: 1.17x slower                                                  |
| docutils                   | 2.62 sec                                                     | 3.06 sec: 1.17x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.83 sec: 1.20x slower                                                 |
| async_generators           | 377 ms                                                       | 455 ms: 1.21x slower                                                   |
| coverage                   | 83.0 ms                                                      | 101 ms: 1.21x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 65.9 ms: 1.25x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 132 ms: 1.25x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 94.0 ms: 1.26x slower                                                  |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 99.9 ms: 1.27x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 63.1 ms: 1.29x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.60 sec: 1.29x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 202 us: 1.31x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 973 ms: 1.32x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 89.8 ms: 1.32x slower                                                  |
| regex_compile              | 132 ms                                                       | 175 ms: 1.33x slower                                                   |
| generators                 | 28.8 ms                                                      | 38.2 ms: 1.33x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 78.8 ms: 1.33x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 14.0 ms: 1.33x slower                                                  |
| fannkuch                   | 370 ms                                                       | 493 ms: 1.33x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.80 ms: 1.34x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 2.02 sec: 1.35x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.52 sec: 1.36x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| 2to3                       | 260 ms                                                       | 363 ms: 1.40x slower                                                   |
| thrift                     | 778 us                                                       | 1.11 ms: 1.42x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 31.0 ms: 1.44x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 96.7 ms: 1.44x slower                                                  |
| django_template            | 34.1 ms                                                      | 49.3 ms: 1.45x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 29.4 ms: 1.48x slower                                                  |
| pyflate                    | 449 ms                                                       | 668 ms: 1.49x slower                                                   |
| mako                       | 11.3 ms                                                      | 16.9 ms: 1.49x slower                                                  |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.55x slower                                                   |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 335 us: 1.60x slower                                                   |
| logging_simple             | 6.16 us                                                      | 9.93 us: 1.61x slower                                                  |
| logging_format             | 6.84 us                                                      | 11.1 us: 1.62x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 183 ms: 1.62x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 9.82 ms: 1.64x slower                                                  |
| richards_super             | 51.6 ms                                                      | 85.4 ms: 1.65x slower                                                  |
| comprehensions             | 16.5 us                                                      | 27.6 us: 1.68x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 501 us: 1.70x slower                                                   |
| richards                   | 45.2 ms                                                      | 77.3 ms: 1.71x slower                                                  |
| sympy_str                  | 275 ms                                                       | 475 ms: 1.73x slower                                                   |
| float                      | 77.5 ms                                                      | 134 ms: 1.73x slower                                                   |
| scimark_sor                | 134 ms                                                       | 234 ms: 1.74x slower                                                   |
| logging_silent             | 103 ns                                                       | 183 ns: 1.79x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 118 ms: 1.81x slower                                                   |
| chaos                      | 57.3 ms                                                      | 104 ms: 1.81x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 2.91 ms: 1.87x slower                                                  |
| go                         | 141 ms                                                       | 268 ms: 1.91x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 2.56 ms: 2.05x slower                                                  |
| sympy_expand               | 457 ms                                                       | 951 ms: 2.08x slower                                                   |
| raytrace                   | 253 ms                                                       | 552 ms: 2.19x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 348 ms: 2.24x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 8.25 ms: 2.64x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.40 ms: 3.70x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.81x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.36x slower                                                           |

Benchmark hidden because not significant (4): async_tree_memoization, sqlite_synth, asyncio_websockets, gc_traversal
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.237x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.32x