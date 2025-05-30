# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 3f7871b
- commit date: 2025-02-13
- overall geometric mean: 1.052x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.16x slower                                              |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                            |
| html5lib       | 63.6 ms                                                | 72.9 ms: 1.15x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                              |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                              |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 356 ms: 1.56x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 559 ms: 1.29x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 591 ms: 1.21x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                             |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                              |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.6 ms: 1.05x faster                                             |
| pidigits       | 184 ms                                                 | 206 ms: 1.12x slower                                              |
| nbody          | 89.3 ms                                                | 129 ms: 1.45x slower                                              |
| Geometric mean | (ref)                                                  | 1.15x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                             |
| regex_compile  | 142 ms                                                 | 153 ms: 1.07x slower                                              |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.1 ms: 1.12x slower                                             |
| Geometric mean | (ref)                                                  | 1.05x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.2 ms: 1.10x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.11x slower                                            |
| unpickle_pure_python | 221 us                                                 | 249 us: 1.13x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 96.9 ms: 1.14x slower                                             |
| pickle_pure_python   | 308 us                                                 | 358 us: 1.16x slower                                              |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                             |
| xml_etree_process    | 59.0 ms                                                | 70.2 ms: 1.19x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                             |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.64 ms: 1.35x slower                                             |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                             |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.7 ms: 1.19x slower                                             |
| django_template | 34.7 ms                                                | 42.4 ms: 1.22x slower                                             |
| genshi_text     | 22.8 ms                                                | 28.4 ms: 1.24x slower                                             |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                             |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.98x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                              |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                              |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 356 ms: 1.56x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 559 ms: 1.29x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 591 ms: 1.21x faster                                              |
| deepcopy                   | 352 us                                                 | 308 us: 1.14x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                             |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 88.2 ms: 1.10x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 38.0 us: 1.06x faster                                             |
| float                      | 80.8 ms                                                | 76.6 ms: 1.05x faster                                             |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                             |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                              |
| generators                 | 32.2 ms                                                | 31.9 ms: 1.01x faster                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.69 sec: 1.01x faster                                            |
| comprehensions             | 19.8 us                                                | 19.8 us: 1.00x faster                                             |
| go                         | 139 ms                                                 | 140 ms: 1.00x slower                                              |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                              |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                            |
| deepcopy_reduce            | 3.08 us                                                | 3.14 us: 1.02x slower                                             |
| logging_silent             | 109 ns                                                 | 111 ns: 1.02x slower                                              |
| dulwich_log                | 78.9 ms                                                | 83.1 ms: 1.05x slower                                             |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                            |
| json                       | 5.02 ms                                                | 5.38 ms: 1.07x slower                                             |
| regex_compile              | 142 ms                                                 | 153 ms: 1.07x slower                                              |
| logging_simple             | 6.63 us                                                | 7.14 us: 1.08x slower                                             |
| raytrace                   | 299 ms                                                 | 326 ms: 1.09x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.10x slower                                              |
| pyflate                    | 448 ms                                                 | 493 ms: 1.10x slower                                              |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                              |
| chaos                      | 62.8 ms                                                | 69.4 ms: 1.10x slower                                             |
| logging_format             | 7.35 us                                                | 8.14 us: 1.11x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 824 ms: 1.11x slower                                              |
| pprint_pformat             | 1.52 sec                                               | 1.69 sec: 1.11x slower                                            |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.11x slower                                            |
| pidigits                   | 184 ms                                                 | 206 ms: 1.12x slower                                              |
| mdp                        | 2.42 sec                                               | 2.71 sec: 1.12x slower                                            |
| regex_v8                   | 20.6 ms                                                | 23.1 ms: 1.12x slower                                             |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.5 ms: 1.12x slower                                             |
| unpickle_pure_python       | 221 us                                                 | 249 us: 1.13x slower                                              |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.13x slower                                              |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                              |
| thrift                     | 791 us                                                 | 897 us: 1.13x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 96.9 ms: 1.14x slower                                             |
| scimark_fft                | 342 ms                                                 | 390 ms: 1.14x slower                                              |
| html5lib                   | 63.6 ms                                                | 72.9 ms: 1.15x slower                                             |
| 2to3                       | 264 ms                                                 | 304 ms: 1.16x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 61.7 ms: 1.16x slower                                             |
| sqlglot_transpile          | 1.67 ms                                                | 1.94 ms: 1.16x slower                                             |
| pickle_pure_python         | 308 us                                                 | 358 us: 1.16x slower                                              |
| sympy_str                  | 292 ms                                                 | 340 ms: 1.17x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 89.7 ms: 1.17x slower                                             |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                             |
| sympy_expand               | 468 ms                                                 | 552 ms: 1.18x slower                                              |
| deltablue                  | 3.45 ms                                                | 4.10 ms: 1.19x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 59.7 ms: 1.19x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 70.2 ms: 1.19x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.6 ms: 1.20x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.38 ms: 1.20x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.63 ms: 1.20x slower                                             |
| nqueens                    | 80.1 ms                                                | 96.6 ms: 1.21x slower                                             |
| richards                   | 45.9 ms                                                | 55.7 ms: 1.21x slower                                             |
| django_template            | 34.7 ms                                                | 42.4 ms: 1.22x slower                                             |
| scimark_lu                 | 114 ms                                                 | 139 ms: 1.22x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 84.5 ms: 1.23x slower                                             |
| genshi_text                | 22.8 ms                                                | 28.4 ms: 1.24x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 203 us: 1.24x slower                                              |
| richards_super             | 51.9 ms                                                | 65.0 ms: 1.25x slower                                             |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.27x slower                                             |
| fannkuch                   | 372 ms                                                 | 487 ms: 1.31x slower                                              |
| telco                      | 6.53 ms                                                | 8.54 ms: 1.31x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.78 ms: 1.31x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.64 ms: 1.35x slower                                             |
| coverage                   | 71.4 ms                                                | 96.7 ms: 1.35x slower                                             |
| nbody                      | 89.3 ms                                                | 129 ms: 1.45x slower                                              |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                             |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.34 ms: 3.55x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 94.9 ms: 8.78x slower                                             |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (3): spectral_norm, asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250213-3.14.0a5+-3f7871b-NOGIL/bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.052x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.36x