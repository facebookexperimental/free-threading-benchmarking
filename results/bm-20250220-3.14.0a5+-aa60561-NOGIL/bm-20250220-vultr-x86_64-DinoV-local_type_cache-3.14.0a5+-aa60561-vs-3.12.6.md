# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: aa60561
- commit date: 2025-02-20
- overall geometric mean: 1.046x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.15x slower                                              |
| docutils       | 2.64 sec                                               | 2.79 sec: 1.06x slower                                            |
| html5lib       | 63.6 ms                                                | 73.2 ms: 1.15x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 559 ms: 1.98x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                              |
| async_tree_io              | 1.08 sec                                               | 602 ms: 1.80x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                              |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 344 ms: 1.61x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 501 ms: 1.44x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 532 ms: 1.34x faster                                              |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                              |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                      |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.7 ms: 1.08x faster                                             |
| pidigits       | 184 ms                                                 | 198 ms: 1.08x slower                                              |
| nbody          | 89.3 ms                                                | 128 ms: 1.44x slower                                              |
| Geometric mean | (ref)                                                  | 1.13x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.91 ms: 1.09x faster                                             |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                              |
| regex_compile  | 142 ms                                                 | 155 ms: 1.09x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                             |
| Geometric mean | (ref)                                                  | 1.05x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.7 ms: 1.10x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.31 sec: 1.10x slower                                            |
| unpickle_pure_python | 221 us                                                 | 243 us: 1.10x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 95.2 ms: 1.12x slower                                             |
| xml_etree_process    | 59.0 ms                                                | 69.1 ms: 1.17x slower                                             |
| pickle_pure_python   | 308 us                                                 | 363 us: 1.18x slower                                              |
| json_loads           | 26.5 us                                                | 31.4 us: 1.18x slower                                             |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.26x slower                                             |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.82 ms: 1.37x slower                                             |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                             |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.7 ms: 1.19x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.6 ms: 1.21x slower                                             |
| django_template | 34.7 ms                                                | 43.9 ms: 1.27x slower                                             |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                             |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 559 ms: 1.98x faster                                              |
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.98x faster                                             |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                              |
| async_tree_io              | 1.08 sec                                               | 602 ms: 1.80x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                              |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 344 ms: 1.61x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 501 ms: 1.44x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 532 ms: 1.34x faster                                              |
| deepcopy                   | 352 us                                                 | 308 us: 1.14x faster                                              |
| xml_etree_iterparse        | 96.7 ms                                                | 87.7 ms: 1.10x faster                                             |
| regex_effbot               | 3.17 ms                                                | 2.91 ms: 1.09x faster                                             |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.08x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                             |
| float                      | 80.8 ms                                                | 74.7 ms: 1.08x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 38.0 us: 1.06x faster                                             |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                              |
| generators                 | 32.2 ms                                                | 31.4 ms: 1.03x faster                                             |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                              |
| go                         | 139 ms                                                 | 137 ms: 1.02x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.71 sec: 1.01x faster                                            |
| comprehensions             | 19.8 us                                                | 19.8 us: 1.00x faster                                             |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                              |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                              |
| logging_silent             | 109 ns                                                 | 110 ns: 1.01x slower                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.12 us: 1.01x slower                                             |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.02x slower                                            |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                              |
| dulwich_log                | 78.9 ms                                                | 82.8 ms: 1.05x slower                                             |
| docutils                   | 2.64 sec                                               | 2.79 sec: 1.06x slower                                            |
| json                       | 5.02 ms                                                | 5.35 ms: 1.06x slower                                             |
| raytrace                   | 299 ms                                                 | 319 ms: 1.07x slower                                              |
| pidigits                   | 184 ms                                                 | 198 ms: 1.08x slower                                              |
| regex_compile              | 142 ms                                                 | 155 ms: 1.09x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                              |
| logging_simple             | 6.63 us                                                | 7.26 us: 1.10x slower                                             |
| tomli_loads                | 2.11 sec                                               | 2.31 sec: 1.10x slower                                            |
| logging_format             | 7.35 us                                                | 8.09 us: 1.10x slower                                             |
| deltablue                  | 3.45 ms                                                | 3.79 ms: 1.10x slower                                             |
| chaos                      | 62.8 ms                                                | 69.2 ms: 1.10x slower                                             |
| pyflate                    | 448 ms                                                 | 494 ms: 1.10x slower                                              |
| unpickle_pure_python       | 221 us                                                 | 243 us: 1.10x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 95.2 ms: 1.12x slower                                             |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.5 ms: 1.12x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 836 ms: 1.12x slower                                              |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                              |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                            |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.14x slower                                              |
| thrift                     | 791 us                                                 | 903 us: 1.14x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 87.4 ms: 1.14x slower                                             |
| regex_v8                   | 20.6 ms                                                | 23.5 ms: 1.14x slower                                             |
| mdp                        | 2.42 sec                                               | 2.76 sec: 1.14x slower                                            |
| scimark_fft                | 342 ms                                                 | 391 ms: 1.14x slower                                              |
| html5lib                   | 63.6 ms                                                | 73.2 ms: 1.15x slower                                             |
| 2to3                       | 264 ms                                                 | 304 ms: 1.15x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 61.5 ms: 1.16x slower                                             |
| sympy_str                  | 292 ms                                                 | 340 ms: 1.17x slower                                              |
| hexiom                     | 6.17 ms                                                | 7.22 ms: 1.17x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                             |
| sympy_expand               | 468 ms                                                 | 548 ms: 1.17x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 69.1 ms: 1.17x slower                                             |
| pickle_pure_python         | 308 us                                                 | 363 us: 1.18x slower                                              |
| json_loads                 | 26.5 us                                                | 31.4 us: 1.18x slower                                             |
| nqueens                    | 80.1 ms                                                | 95.0 ms: 1.19x slower                                             |
| richards                   | 45.9 ms                                                | 54.6 ms: 1.19x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 59.7 ms: 1.19x slower                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 82.2 ms: 1.20x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                              |
| genshi_text                | 22.8 ms                                                | 27.6 ms: 1.21x slower                                             |
| richards_super             | 51.9 ms                                                | 63.7 ms: 1.23x slower                                             |
| sqlglot_transpile          | 1.67 ms                                                | 2.06 ms: 1.23x slower                                             |
| scimark_lu                 | 114 ms                                                 | 141 ms: 1.23x slower                                              |
| sqlglot_parse              | 1.36 ms                                                | 1.67 ms: 1.24x slower                                             |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.26x slower                                             |
| django_template            | 34.7 ms                                                | 43.9 ms: 1.27x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.27x slower                                             |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.27x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.71 ms: 1.30x slower                                             |
| fannkuch                   | 372 ms                                                 | 489 ms: 1.31x slower                                              |
| telco                      | 6.53 ms                                                | 8.62 ms: 1.32x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.82 ms: 1.37x slower                                             |
| coverage                   | 71.4 ms                                                | 98.0 ms: 1.37x slower                                             |
| nbody                      | 89.3 ms                                                | 128 ms: 1.44x slower                                              |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                             |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.51x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 96.7 ms: 8.96x slower                                             |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (2): coroutines, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250220-3.14.0a5+-aa60561-NOGIL/bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.046x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.38x