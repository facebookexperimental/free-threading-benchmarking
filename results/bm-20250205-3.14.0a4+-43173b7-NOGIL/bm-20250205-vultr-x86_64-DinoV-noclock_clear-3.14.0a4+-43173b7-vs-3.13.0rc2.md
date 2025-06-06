# Results vs. 3.13.0rc2

- fork: DinoV
- ref: noclock_clear
- machine: linux-x86_64
- commit hash: 43173b7
- commit date: 2025-02-05
- overall geometric mean: 1.073x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 302 ms: 1.16x slower                                           |
| docutils       | 2.62 sec                                                     | 2.78 sec: 1.06x slower                                         |
| html5lib       | 67.0 ms                                                      | 68.5 ms: 1.02x slower                                          |
| Geometric mean | (ref)                                                        | 1.08x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 575 ms: 1.59x faster                                           |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                           |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                           |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 536 ms: 1.24x faster                                           |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                           |
| coroutines                 | 23.6 ms                                                      | 23.6 ms: 1.00x slower                                          |
| async_generators           | 377 ms                                                       | 379 ms: 1.00x slower                                           |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                   |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                           |
| nbody          | 85.1 ms                                                      | 134 ms: 1.57x slower                                           |
| Geometric mean | (ref)                                                        | 1.11x slower                                                   |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                          |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                           |
| regex_v8       | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                          |
| regex_compile  | 132 ms                                                       | 147 ms: 1.12x slower                                           |
| Geometric mean | (ref)                                                        | 1.00x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.5 ms: 1.09x faster                                          |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                           |
| xml_etree_generate   | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                          |
| tomli_loads          | 2.01 sec                                                     | 2.28 sec: 1.14x slower                                         |
| json_loads           | 27.0 us                                                      | 31.2 us: 1.16x slower                                          |
| xml_etree_process    | 59.3 ms                                                      | 68.7 ms: 1.16x slower                                          |
| unpickle_pure_python | 210 us                                                       | 245 us: 1.17x slower                                           |
| json_dumps           | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                          |
| pickle_pure_python   | 294 us                                                       | 370 us: 1.26x slower                                           |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.64 ms: 1.30x slower                                          |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.40x slower                                          |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.8 ms: 1.23x slower                                          |
| django_template | 34.1 ms                                                      | 42.8 ms: 1.25x slower                                          |
| genshi_text     | 21.5 ms                                                      | 27.7 ms: 1.29x slower                                          |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                          |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.76 ms: 1.79x faster                                          |
| async_tree_io_tg           | 913 ms                                                       | 575 ms: 1.59x faster                                           |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                           |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                           |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 536 ms: 1.24x faster                                           |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                           |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                           |
| deepcopy                   | 355 us                                                       | 313 us: 1.13x faster                                           |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                          |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.5 ms: 1.09x faster                                          |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                          |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                           |
| deepcopy_memo              | 39.1 us                                                      | 37.6 us: 1.04x faster                                          |
| go                         | 141 ms                                                       | 136 ms: 1.04x faster                                           |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.03x faster                                           |
| scimark_sor                | 134 ms                                                       | 131 ms: 1.03x faster                                           |
| pathlib                    | 19.2 ms                                                      | 18.7 ms: 1.02x faster                                          |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                           |
| create_gc_cycles           | 1.34 ms                                                      | 1.33 ms: 1.01x faster                                          |
| coroutines                 | 23.6 ms                                                      | 23.6 ms: 1.00x slower                                          |
| async_generators           | 377 ms                                                       | 379 ms: 1.00x slower                                           |
| html5lib                   | 67.0 ms                                                      | 68.5 ms: 1.02x slower                                          |
| deepcopy_reduce            | 3.11 us                                                      | 3.20 us: 1.03x slower                                          |
| regex_v8                   | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                          |
| bpe_tokeniser              | 4.45 sec                                                     | 4.67 sec: 1.05x slower                                         |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.05x slower                                         |
| docutils                   | 2.62 sec                                                     | 2.78 sec: 1.06x slower                                         |
| scimark_fft                | 349 ms                                                       | 374 ms: 1.07x slower                                           |
| dulwich_log                | 74.8 ms                                                      | 81.5 ms: 1.09x slower                                          |
| json                       | 4.93 ms                                                      | 5.38 ms: 1.09x slower                                          |
| logging_silent             | 103 ns                                                       | 112 ns: 1.10x slower                                           |
| pprint_safe_repr           | 738 ms                                                       | 816 ms: 1.11x slower                                           |
| pyflate                    | 449 ms                                                       | 498 ms: 1.11x slower                                           |
| telco                      | 7.82 ms                                                      | 8.70 ms: 1.11x slower                                          |
| regex_compile              | 132 ms                                                       | 147 ms: 1.12x slower                                           |
| xml_etree_generate         | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                          |
| sqlglot_normalize          | 106 ms                                                       | 120 ms: 1.13x slower                                           |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.13x slower                                         |
| tomli_loads                | 2.01 sec                                                     | 2.28 sec: 1.14x slower                                         |
| mdp                        | 2.36 sec                                                     | 2.70 sec: 1.15x slower                                         |
| sqlglot_optimize           | 52.7 ms                                                      | 60.7 ms: 1.15x slower                                          |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.43 ms: 1.15x slower                                          |
| json_loads                 | 27.0 us                                                      | 31.2 us: 1.16x slower                                          |
| xml_etree_process          | 59.3 ms                                                      | 68.7 ms: 1.16x slower                                          |
| generators                 | 28.8 ms                                                      | 33.4 ms: 1.16x slower                                          |
| 2to3                       | 260 ms                                                       | 302 ms: 1.16x slower                                           |
| logging_simple             | 6.16 us                                                      | 7.16 us: 1.16x slower                                          |
| thrift                     | 778 us                                                       | 905 us: 1.16x slower                                           |
| unpickle_pure_python       | 210 us                                                       | 245 us: 1.17x slower                                           |
| coverage                   | 83.0 ms                                                      | 98.0 ms: 1.18x slower                                          |
| sympy_sum                  | 156 ms                                                       | 184 ms: 1.18x slower                                           |
| chaos                      | 57.3 ms                                                      | 68.1 ms: 1.19x slower                                          |
| logging_format             | 6.84 us                                                      | 8.16 us: 1.19x slower                                          |
| sympy_expand               | 457 ms                                                       | 548 ms: 1.20x slower                                           |
| comprehensions             | 16.5 us                                                      | 19.8 us: 1.20x slower                                          |
| sympy_integrate            | 19.8 ms                                                      | 24.0 ms: 1.21x slower                                          |
| json_dumps                 | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                          |
| scimark_lu                 | 113 ms                                                       | 137 ms: 1.21x slower                                           |
| sympy_str                  | 275 ms                                                       | 334 ms: 1.22x slower                                           |
| sqlglot_transpile          | 1.56 ms                                                      | 1.90 ms: 1.22x slower                                          |
| genshi_xml                 | 48.8 ms                                                      | 59.8 ms: 1.23x slower                                          |
| hexiom                     | 5.99 ms                                                      | 7.35 ms: 1.23x slower                                          |
| nqueens                    | 78.6 ms                                                      | 96.6 ms: 1.23x slower                                          |
| scimark_monte_carlo        | 65.4 ms                                                      | 80.7 ms: 1.23x slower                                          |
| richards                   | 45.2 ms                                                      | 56.1 ms: 1.24x slower                                          |
| django_template            | 34.1 ms                                                      | 42.8 ms: 1.25x slower                                          |
| pickle_pure_python         | 294 us                                                       | 370 us: 1.26x slower                                           |
| raytrace                   | 253 ms                                                       | 318 ms: 1.26x slower                                           |
| sqlglot_parse              | 1.25 ms                                                      | 1.57 ms: 1.26x slower                                          |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                           |
| richards_super             | 51.6 ms                                                      | 66.0 ms: 1.28x slower                                          |
| genshi_text                | 21.5 ms                                                      | 27.7 ms: 1.29x slower                                          |
| typing_runtime_protocols   | 155 us                                                       | 199 us: 1.29x slower                                           |
| crypto_pyaes               | 67.9 ms                                                      | 87.8 ms: 1.29x slower                                          |
| python_startup_no_site     | 7.39 ms                                                      | 9.64 ms: 1.30x slower                                          |
| fannkuch                   | 370 ms                                                       | 483 ms: 1.31x slower                                           |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.40x slower                                          |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                          |
| deltablue                  | 3.12 ms                                                      | 4.52 ms: 1.45x slower                                          |
| nbody                      | 85.1 ms                                                      | 134 ms: 1.57x slower                                           |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.61x slower                                          |
| bench_mp_pool              | 11.0 ms                                                      | 94.2 ms: 8.57x slower                                          |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                   |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, float
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250205-3.14.0a4+-43173b7-NOGIL/bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-43173b7.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.073x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x