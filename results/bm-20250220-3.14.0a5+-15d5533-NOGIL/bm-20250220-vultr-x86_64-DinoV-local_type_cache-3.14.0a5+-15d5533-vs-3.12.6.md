# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 15d5533
- commit date: 2025-02-20
- overall geometric mean: 1.042x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.15x slower                                              |
| docutils       | 2.64 sec                                               | 2.72 sec: 1.03x slower                                            |
| html5lib       | 63.6 ms                                                | 72.1 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 553 ms: 2.01x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                              |
| async_tree_io              | 1.08 sec                                               | 585 ms: 1.85x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                              |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 523 ms: 1.37x faster                                              |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                             |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.4 ms: 1.06x faster                                             |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                              |
| nbody          | 89.3 ms                                                | 128 ms: 1.43x slower                                              |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                             |
| regex_compile  | 142 ms                                                 | 154 ms: 1.08x slower                                              |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.9 ms: 1.16x slower                                             |
| Geometric mean | (ref)                                                  | 1.05x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.6 ms: 1.10x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.33 sec: 1.11x slower                                            |
| xml_etree_generate   | 85.2 ms                                                | 94.9 ms: 1.11x slower                                             |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.13x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 69.2 ms: 1.17x slower                                             |
| json_loads           | 26.5 us                                                | 31.4 us: 1.18x slower                                             |
| pickle_pure_python   | 308 us                                                 | 367 us: 1.19x slower                                              |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                             |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.75 ms: 1.36x slower                                             |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                             |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.0 ms: 1.18x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.8 ms: 1.22x slower                                             |
| django_template | 34.7 ms                                                | 42.3 ms: 1.22x slower                                             |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                             |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 553 ms: 2.01x faster                                              |
| gc_traversal               | 3.46 ms                                                | 1.73 ms: 2.00x faster                                             |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                              |
| async_tree_io              | 1.08 sec                                               | 585 ms: 1.85x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                              |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 523 ms: 1.37x faster                                              |
| deepcopy                   | 352 us                                                 | 308 us: 1.14x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 87.6 ms: 1.10x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.9 ms: 1.08x faster                                             |
| float                      | 80.8 ms                                                | 76.4 ms: 1.06x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 38.6 us: 1.04x faster                                             |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                             |
| generators                 | 32.2 ms                                                | 31.7 ms: 1.02x faster                                             |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.72 sec: 1.00x faster                                            |
| go                         | 139 ms                                                 | 140 ms: 1.01x slower                                              |
| comprehensions             | 19.8 us                                                | 20.0 us: 1.01x slower                                             |
| deepcopy_reduce            | 3.08 us                                                | 3.13 us: 1.02x slower                                             |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                            |
| scimark_sor                | 130 ms                                                 | 133 ms: 1.03x slower                                              |
| docutils                   | 2.64 sec                                               | 2.72 sec: 1.03x slower                                            |
| logging_silent             | 109 ns                                                 | 114 ns: 1.04x slower                                              |
| dulwich_log                | 78.9 ms                                                | 82.8 ms: 1.05x slower                                             |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                              |
| json                       | 5.02 ms                                                | 5.30 ms: 1.05x slower                                             |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.3 ms: 1.07x slower                                             |
| logging_simple             | 6.63 us                                                | 7.15 us: 1.08x slower                                             |
| sqlalchemy_declarative     | 143 ms                                                 | 154 ms: 1.08x slower                                              |
| regex_compile              | 142 ms                                                 | 154 ms: 1.08x slower                                              |
| raytrace                   | 299 ms                                                 | 325 ms: 1.09x slower                                              |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                              |
| mdp                        | 2.42 sec                                               | 2.66 sec: 1.10x slower                                            |
| thrift                     | 791 us                                                 | 875 us: 1.11x slower                                              |
| tomli_loads                | 2.11 sec                                               | 2.33 sec: 1.11x slower                                            |
| pyflate                    | 448 ms                                                 | 496 ms: 1.11x slower                                              |
| logging_format             | 7.35 us                                                | 8.13 us: 1.11x slower                                             |
| sympy_sum                  | 166 ms                                                 | 184 ms: 1.11x slower                                              |
| chaos                      | 62.8 ms                                                | 69.9 ms: 1.11x slower                                             |
| xml_etree_generate         | 85.2 ms                                                | 94.9 ms: 1.11x slower                                             |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.12x slower                                              |
| deltablue                  | 3.45 ms                                                | 3.87 ms: 1.12x slower                                             |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.13x slower                                              |
| pprint_safe_repr           | 743 ms                                                 | 842 ms: 1.13x slower                                              |
| html5lib                   | 63.6 ms                                                | 72.1 ms: 1.13x slower                                             |
| pprint_pformat             | 1.52 sec                                               | 1.73 sec: 1.14x slower                                            |
| crypto_pyaes               | 76.6 ms                                                | 87.0 ms: 1.14x slower                                             |
| sympy_str                  | 292 ms                                                 | 332 ms: 1.14x slower                                              |
| scimark_fft                | 342 ms                                                 | 390 ms: 1.14x slower                                              |
| 2to3                       | 264 ms                                                 | 302 ms: 1.15x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 61.1 ms: 1.15x slower                                             |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                             |
| sympy_expand               | 468 ms                                                 | 539 ms: 1.15x slower                                              |
| sympy_integrate            | 20.5 ms                                                | 23.7 ms: 1.16x slower                                             |
| regex_v8                   | 20.6 ms                                                | 23.9 ms: 1.16x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 69.2 ms: 1.17x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 59.0 ms: 1.18x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                             |
| json_loads                 | 26.5 us                                                | 31.4 us: 1.18x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.34 ms: 1.19x slower                                             |
| pickle_pure_python         | 308 us                                                 | 367 us: 1.19x slower                                              |
| richards                   | 45.9 ms                                                | 54.9 ms: 1.19x slower                                             |
| nqueens                    | 80.1 ms                                                | 96.7 ms: 1.21x slower                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 82.6 ms: 1.21x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 197 us: 1.21x slower                                              |
| genshi_text                | 22.8 ms                                                | 27.8 ms: 1.22x slower                                             |
| django_template            | 34.7 ms                                                | 42.3 ms: 1.22x slower                                             |
| scimark_lu                 | 114 ms                                                 | 140 ms: 1.23x slower                                              |
| richards_super             | 51.9 ms                                                | 64.0 ms: 1.23x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.25x slower                                             |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.73 ms: 1.31x slower                                             |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.32x slower                                              |
| telco                      | 6.53 ms                                                | 8.82 ms: 1.35x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.75 ms: 1.36x slower                                             |
| coverage                   | 71.4 ms                                                | 98.3 ms: 1.38x slower                                             |
| nbody                      | 89.3 ms                                                | 128 ms: 1.43x slower                                              |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                             |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.52x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.9 ms: 8.88x slower                                             |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                      |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250220-3.14.0a5+-15d5533-NOGIL/bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.042x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.37x