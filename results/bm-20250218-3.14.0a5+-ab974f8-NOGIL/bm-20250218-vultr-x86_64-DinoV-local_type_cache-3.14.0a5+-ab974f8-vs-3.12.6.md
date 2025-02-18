# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: ab974f8
- commit date: 2025-02-18
- overall geometric mean: 1.053x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 307 ms: 1.16x slower                                              |
| docutils       | 2.64 sec                                               | 2.78 sec: 1.06x slower                                            |
| html5lib       | 63.6 ms                                                | 73.4 ms: 1.15x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                              |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 322 ms: 1.74x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 261 ms: 1.71x faster                                              |
| async_tree_none            | 464 ms                                                 | 291 ms: 1.59x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 359 ms: 1.55x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 507 ms: 1.43x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                              |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                             |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                              |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.4 ms: 1.03x faster                                             |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                              |
| nbody          | 89.3 ms                                                | 130 ms: 1.45x slower                                              |
| Geometric mean | (ref)                                                  | 1.13x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.81 ms: 1.13x faster                                             |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                              |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                             |
| Geometric mean | (ref)                                                  | 1.04x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.2 ms: 1.10x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.36 sec: 1.12x slower                                            |
| unpickle_pure_python | 221 us                                                 | 249 us: 1.13x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 96.8 ms: 1.14x slower                                             |
| json_loads           | 26.5 us                                                | 31.0 us: 1.17x slower                                             |
| pickle_pure_python   | 308 us                                                 | 360 us: 1.17x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 70.1 ms: 1.19x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                             |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.74 ms: 1.36x slower                                             |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.57x slower                                             |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.1 ms: 1.20x slower                                             |
| genshi_text     | 22.8 ms                                                | 28.2 ms: 1.24x slower                                             |
| django_template | 34.7 ms                                                | 43.0 ms: 1.24x slower                                             |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                             |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.97x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                              |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 322 ms: 1.74x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 261 ms: 1.71x faster                                              |
| async_tree_none            | 464 ms                                                 | 291 ms: 1.59x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 359 ms: 1.55x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 507 ms: 1.43x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.81 ms: 1.13x faster                                             |
| deepcopy                   | 352 us                                                 | 315 us: 1.12x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 88.2 ms: 1.10x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                              |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 38.6 us: 1.04x faster                                             |
| float                      | 80.8 ms                                                | 78.4 ms: 1.03x faster                                             |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                             |
| generators                 | 32.2 ms                                                | 32.0 ms: 1.01x faster                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.71 sec: 1.01x faster                                            |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                              |
| comprehensions             | 19.8 us                                                | 20.0 us: 1.01x slower                                             |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                              |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.14 us: 1.02x slower                                             |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                              |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.03x slower                                            |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                              |
| docutils                   | 2.64 sec                                               | 2.78 sec: 1.06x slower                                            |
| dulwich_log                | 78.9 ms                                                | 83.2 ms: 1.06x slower                                             |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                             |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                              |
| mdp                        | 2.42 sec                                               | 2.59 sec: 1.07x slower                                            |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                              |
| raytrace                   | 299 ms                                                 | 326 ms: 1.09x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                              |
| logging_simple             | 6.63 us                                                | 7.29 us: 1.10x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 826 ms: 1.11x slower                                              |
| chaos                      | 62.8 ms                                                | 70.0 ms: 1.11x slower                                             |
| tomli_loads                | 2.11 sec                                               | 2.36 sec: 1.12x slower                                            |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                            |
| logging_format             | 7.35 us                                                | 8.27 us: 1.13x slower                                             |
| unpickle_pure_python       | 221 us                                                 | 249 us: 1.13x slower                                              |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 96.8 ms: 1.14x slower                                             |
| pyflate                    | 448 ms                                                 | 509 ms: 1.14x slower                                              |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.15x slower                                              |
| deltablue                  | 3.45 ms                                                | 3.95 ms: 1.15x slower                                             |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                             |
| thrift                     | 791 us                                                 | 910 us: 1.15x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 25.1 ms: 1.15x slower                                             |
| crypto_pyaes               | 76.6 ms                                                | 88.4 ms: 1.15x slower                                             |
| html5lib                   | 63.6 ms                                                | 73.4 ms: 1.15x slower                                             |
| scimark_fft                | 342 ms                                                 | 395 ms: 1.16x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 61.6 ms: 1.16x slower                                             |
| 2to3                       | 264 ms                                                 | 307 ms: 1.16x slower                                              |
| json_loads                 | 26.5 us                                                | 31.0 us: 1.17x slower                                             |
| pickle_pure_python         | 308 us                                                 | 360 us: 1.17x slower                                              |
| sqlglot_transpile          | 1.67 ms                                                | 1.96 ms: 1.17x slower                                             |
| sympy_str                  | 292 ms                                                 | 342 ms: 1.17x slower                                              |
| sympy_expand               | 468 ms                                                 | 554 ms: 1.19x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 70.1 ms: 1.19x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.6 ms: 1.20x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 60.1 ms: 1.20x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.40 ms: 1.20x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.63 ms: 1.20x slower                                             |
| nqueens                    | 80.1 ms                                                | 96.5 ms: 1.21x slower                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 83.1 ms: 1.21x slower                                             |
| scimark_lu                 | 114 ms                                                 | 140 ms: 1.23x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.23x slower                                              |
| richards                   | 45.9 ms                                                | 56.5 ms: 1.23x slower                                             |
| genshi_text                | 22.8 ms                                                | 28.2 ms: 1.24x slower                                             |
| django_template            | 34.7 ms                                                | 43.0 ms: 1.24x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                             |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                              |
| richards_super             | 51.9 ms                                                | 65.6 ms: 1.27x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.28x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.72 ms: 1.30x slower                                             |
| telco                      | 6.53 ms                                                | 8.51 ms: 1.30x slower                                             |
| fannkuch                   | 372 ms                                                 | 494 ms: 1.33x slower                                              |
| python_startup_no_site     | 7.16 ms                                                | 9.74 ms: 1.36x slower                                             |
| coverage                   | 71.4 ms                                                | 97.4 ms: 1.36x slower                                             |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                             |
| nbody                      | 89.3 ms                                                | 130 ms: 1.45x slower                                              |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.57x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.7 ms: 8.86x slower                                             |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                      |

Benchmark hidden because not significant (2): spectral_norm, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250218-3.14.0a5+-ab974f8-NOGIL/bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.053x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.37x