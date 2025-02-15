# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 627b63e
- commit date: 2025-02-14
- overall geometric mean: 1.053x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 307 ms: 1.16x slower                                              |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                            |
| html5lib       | 63.6 ms                                                | 71.6 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 578 ms: 1.92x faster                                              |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.78x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                              |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                              |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                             |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                              |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.1 ms: 1.05x faster                                             |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                              |
| nbody          | 89.3 ms                                                | 133 ms: 1.49x slower                                              |
| Geometric mean | (ref)                                                  | 1.14x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                             |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                              |
| regex_dna      | 168 ms                                                 | 184 ms: 1.09x slower                                              |
| regex_v8       | 20.6 ms                                                | 25.0 ms: 1.21x slower                                             |
| Geometric mean | (ref)                                                  | 1.07x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.8 ms: 1.09x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.36 sec: 1.12x slower                                            |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.13x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 97.0 ms: 1.14x slower                                             |
| json_loads           | 26.5 us                                                | 31.1 us: 1.17x slower                                             |
| pickle_pure_python   | 308 us                                                 | 362 us: 1.18x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 70.3 ms: 1.19x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.25x slower                                             |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.71 ms: 1.36x slower                                             |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                             |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.3 ms: 1.18x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.8 ms: 1.22x slower                                             |
| django_template | 34.7 ms                                                | 43.0 ms: 1.24x slower                                             |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                             |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.74 ms: 1.99x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 578 ms: 1.92x faster                                              |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.78x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                              |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                              |
| deepcopy                   | 352 us                                                 | 310 us: 1.13x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                             |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 88.8 ms: 1.09x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                             |
| float                      | 80.8 ms                                                | 77.1 ms: 1.05x faster                                             |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 38.7 us: 1.04x faster                                             |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.69 sec: 1.01x faster                                            |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                              |
| go                         | 139 ms                                                 | 140 ms: 1.00x slower                                              |
| comprehensions             | 19.8 us                                                | 20.1 us: 1.01x slower                                             |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                              |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                              |
| pycparser                  | 1.17 sec                                               | 1.21 sec: 1.04x slower                                            |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.20 us: 1.04x slower                                             |
| dulwich_log                | 78.9 ms                                                | 83.2 ms: 1.05x slower                                             |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                            |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                             |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                              |
| logging_simple             | 6.63 us                                                | 7.21 us: 1.09x slower                                             |
| raytrace                   | 299 ms                                                 | 326 ms: 1.09x slower                                              |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.09x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                              |
| logging_format             | 7.35 us                                                | 8.21 us: 1.12x slower                                             |
| chaos                      | 62.8 ms                                                | 70.2 ms: 1.12x slower                                             |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.4 ms: 1.12x slower                                             |
| tomli_loads                | 2.11 sec                                               | 2.36 sec: 1.12x slower                                            |
| mdp                        | 2.42 sec                                               | 2.71 sec: 1.12x slower                                            |
| pprint_safe_repr           | 743 ms                                                 | 836 ms: 1.12x slower                                              |
| html5lib                   | 63.6 ms                                                | 71.6 ms: 1.13x slower                                             |
| deltablue                  | 3.45 ms                                                | 3.88 ms: 1.13x slower                                             |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                              |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                              |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                            |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.13x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 97.0 ms: 1.14x slower                                             |
| pyflate                    | 448 ms                                                 | 510 ms: 1.14x slower                                              |
| thrift                     | 791 us                                                 | 911 us: 1.15x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 61.7 ms: 1.16x slower                                             |
| scimark_fft                | 342 ms                                                 | 396 ms: 1.16x slower                                              |
| 2to3                       | 264 ms                                                 | 307 ms: 1.16x slower                                              |
| sympy_str                  | 292 ms                                                 | 340 ms: 1.17x slower                                              |
| json_loads                 | 26.5 us                                                | 31.1 us: 1.17x slower                                             |
| crypto_pyaes               | 76.6 ms                                                | 90.1 ms: 1.18x slower                                             |
| pickle_pure_python         | 308 us                                                 | 362 us: 1.18x slower                                              |
| sqlglot_transpile          | 1.67 ms                                                | 1.97 ms: 1.18x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 59.3 ms: 1.18x slower                                             |
| sympy_expand               | 468 ms                                                 | 556 ms: 1.19x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 70.3 ms: 1.19x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.5 ms: 1.19x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.40 ms: 1.20x slower                                             |
| nqueens                    | 80.1 ms                                                | 96.3 ms: 1.20x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.63 ms: 1.21x slower                                             |
| richards                   | 45.9 ms                                                | 55.7 ms: 1.21x slower                                             |
| regex_v8                   | 20.6 ms                                                | 25.0 ms: 1.21x slower                                             |
| genshi_text                | 22.8 ms                                                | 27.8 ms: 1.22x slower                                             |
| scimark_lu                 | 114 ms                                                 | 139 ms: 1.22x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 83.6 ms: 1.22x slower                                             |
| meteor_contest             | 104 ms                                                 | 127 ms: 1.23x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.23x slower                                              |
| django_template            | 34.7 ms                                                | 43.0 ms: 1.24x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.25x slower                                             |
| richards_super             | 51.9 ms                                                | 64.8 ms: 1.25x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.27x slower                                             |
| fannkuch                   | 372 ms                                                 | 491 ms: 1.32x slower                                              |
| telco                      | 6.53 ms                                                | 8.68 ms: 1.33x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.94 ms: 1.35x slower                                             |
| coverage                   | 71.4 ms                                                | 96.8 ms: 1.36x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.71 ms: 1.36x slower                                             |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                             |
| nbody                      | 89.3 ms                                                | 133 ms: 1.49x slower                                              |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.53x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.0 ms: 8.79x slower                                             |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (3): generators, logging_silent, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250214-3.14.0a5+-627b63e-NOGIL/bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.053x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.37x