# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: d72f499
- commit date: 2025-02-18
- overall geometric mean: 1.055x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 305 ms: 1.16x slower                                              |
| docutils       | 2.64 sec                                               | 2.78 sec: 1.05x slower                                            |
| html5lib       | 63.6 ms                                                | 72.5 ms: 1.14x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                              |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.77x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 323 ms: 1.73x faster                                              |
| async_tree_none            | 464 ms                                                 | 290 ms: 1.60x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 356 ms: 1.56x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 511 ms: 1.41x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                              |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                              |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                      |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.4 ms: 1.04x faster                                             |
| pidigits       | 184 ms                                                 | 203 ms: 1.10x slower                                              |
| nbody          | 89.3 ms                                                | 131 ms: 1.46x slower                                              |
| Geometric mean | (ref)                                                  | 1.16x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.09x faster                                             |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                              |
| regex_compile  | 142 ms                                                 | 155 ms: 1.09x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.2 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.05x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.9 ms: 1.09x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.36 sec: 1.12x slower                                            |
| xml_etree_generate   | 85.2 ms                                                | 97.2 ms: 1.14x slower                                             |
| unpickle_pure_python | 221 us                                                 | 255 us: 1.16x slower                                              |
| json_loads           | 26.5 us                                                | 31.3 us: 1.18x slower                                             |
| xml_etree_process    | 59.0 ms                                                | 70.3 ms: 1.19x slower                                             |
| pickle_pure_python   | 308 us                                                 | 367 us: 1.19x slower                                              |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.25x slower                                             |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.70 ms: 1.35x slower                                             |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.56x slower                                             |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.4 ms: 1.18x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.8 ms: 1.22x slower                                             |
| django_template | 34.7 ms                                                | 43.3 ms: 1.25x slower                                             |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                             |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.97x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                              |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.77x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 323 ms: 1.73x faster                                              |
| async_tree_none            | 464 ms                                                 | 290 ms: 1.60x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 356 ms: 1.56x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 511 ms: 1.41x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                              |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.89 ms: 1.09x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 88.9 ms: 1.09x faster                                             |
| pathlib                    | 21.5 ms                                                | 19.9 ms: 1.08x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 38.6 us: 1.04x faster                                             |
| float                      | 80.8 ms                                                | 77.4 ms: 1.04x faster                                             |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.71 sec: 1.01x faster                                            |
| comprehensions             | 19.8 us                                                | 20.0 us: 1.01x slower                                             |
| go                         | 139 ms                                                 | 142 ms: 1.02x slower                                              |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.02x slower                                            |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                              |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.22 us: 1.05x slower                                             |
| dulwich_log                | 78.9 ms                                                | 82.9 ms: 1.05x slower                                             |
| docutils                   | 2.64 sec                                               | 2.78 sec: 1.05x slower                                            |
| logging_silent             | 109 ns                                                 | 116 ns: 1.07x slower                                              |
| json                       | 5.02 ms                                                | 5.40 ms: 1.08x slower                                             |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                              |
| logging_simple             | 6.63 us                                                | 7.21 us: 1.09x slower                                             |
| regex_compile              | 142 ms                                                 | 155 ms: 1.09x slower                                              |
| raytrace                   | 299 ms                                                 | 328 ms: 1.10x slower                                              |
| pidigits                   | 184 ms                                                 | 203 ms: 1.10x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.10x slower                                              |
| thrift                     | 791 us                                                 | 881 us: 1.11x slower                                              |
| pyflate                    | 448 ms                                                 | 499 ms: 1.11x slower                                              |
| logging_format             | 7.35 us                                                | 8.20 us: 1.12x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 831 ms: 1.12x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.4 ms: 1.12x slower                                             |
| tomli_loads                | 2.11 sec                                               | 2.36 sec: 1.12x slower                                            |
| chaos                      | 62.8 ms                                                | 70.4 ms: 1.12x slower                                             |
| regex_v8                   | 20.6 ms                                                | 23.2 ms: 1.13x slower                                             |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                              |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                            |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.13x slower                                              |
| html5lib                   | 63.6 ms                                                | 72.5 ms: 1.14x slower                                             |
| xml_etree_generate         | 85.2 ms                                                | 97.2 ms: 1.14x slower                                             |
| scimark_fft                | 342 ms                                                 | 390 ms: 1.14x slower                                              |
| mdp                        | 2.42 sec                                               | 2.77 sec: 1.15x slower                                            |
| deltablue                  | 3.45 ms                                                | 3.97 ms: 1.15x slower                                             |
| unpickle_pure_python       | 221 us                                                 | 255 us: 1.16x slower                                              |
| 2to3                       | 264 ms                                                 | 305 ms: 1.16x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 61.9 ms: 1.16x slower                                             |
| sympy_str                  | 292 ms                                                 | 339 ms: 1.16x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 89.4 ms: 1.17x slower                                             |
| sqlglot_transpile          | 1.67 ms                                                | 1.96 ms: 1.17x slower                                             |
| json_loads                 | 26.5 us                                                | 31.3 us: 1.18x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 59.4 ms: 1.18x slower                                             |
| sympy_expand               | 468 ms                                                 | 553 ms: 1.18x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 70.3 ms: 1.19x slower                                             |
| pickle_pure_python         | 308 us                                                 | 367 us: 1.19x slower                                              |
| sympy_integrate            | 20.5 ms                                                | 24.6 ms: 1.20x slower                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 82.4 ms: 1.20x slower                                             |
| richards                   | 45.9 ms                                                | 55.4 ms: 1.21x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.64 ms: 1.21x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.48 ms: 1.21x slower                                             |
| genshi_text                | 22.8 ms                                                | 27.8 ms: 1.22x slower                                             |
| nqueens                    | 80.1 ms                                                | 98.0 ms: 1.22x slower                                             |
| scimark_lu                 | 114 ms                                                 | 141 ms: 1.23x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                              |
| richards_super             | 51.9 ms                                                | 64.8 ms: 1.25x slower                                             |
| django_template            | 34.7 ms                                                | 43.3 ms: 1.25x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.25x slower                                             |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.28x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.72 ms: 1.30x slower                                             |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.32x slower                                              |
| telco                      | 6.53 ms                                                | 8.68 ms: 1.33x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.70 ms: 1.35x slower                                             |
| coverage                   | 71.4 ms                                                | 99.3 ms: 1.39x slower                                             |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                             |
| nbody                      | 89.3 ms                                                | 131 ms: 1.46x slower                                              |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.56x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.52x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.6 ms: 8.86x slower                                             |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                      |

Benchmark hidden because not significant (4): generators, coroutines, asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250218-3.14.0a5+-d72f499-NOGIL/bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.055x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.36x