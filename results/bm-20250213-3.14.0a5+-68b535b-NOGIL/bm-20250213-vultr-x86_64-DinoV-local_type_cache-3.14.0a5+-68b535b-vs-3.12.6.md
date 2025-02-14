# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 68b535b
- commit date: 2025-02-13
- overall geometric mean: 1.027x slower
- HPT reliability: 99.63%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 297 ms: 1.13x slower                                              |
| docutils       | 2.64 sec                                               | 2.74 sec: 1.04x slower                                            |
| html5lib       | 63.6 ms                                                | 70.3 ms: 1.11x slower                                             |
| Geometric mean | (ref)                                                  | 1.09x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 566 ms: 1.96x faster                                              |
| async_tree_io              | 1.08 sec                                               | 598 ms: 1.81x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                              |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 346 ms: 1.60x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 494 ms: 1.46x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 526 ms: 1.36x faster                                              |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                             |
| async_generators           | 384 ms                                                 | 368 ms: 1.05x faster                                              |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.1 ms: 1.09x faster                                             |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                              |
| nbody          | 89.3 ms                                                | 125 ms: 1.40x slower                                              |
| Geometric mean | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                             |
| regex_compile  | 142 ms                                                 | 145 ms: 1.01x slower                                              |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                             |
| Geometric mean | (ref)                                                  | 1.03x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.3 ms: 1.10x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.23 sec: 1.06x slower                                            |
| unpickle_pure_python | 221 us                                                 | 237 us: 1.07x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 94.9 ms: 1.11x slower                                             |
| pickle_pure_python   | 308 us                                                 | 347 us: 1.13x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                             |
| json_loads           | 26.5 us                                                | 31.4 us: 1.18x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                             |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.72 ms: 1.36x slower                                             |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                             |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 56.7 ms: 1.13x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.0 ms: 1.18x slower                                             |
| django_template | 34.7 ms                                                | 41.3 ms: 1.19x slower                                             |
| mako            | 11.0 ms                                                | 15.5 ms: 1.40x slower                                             |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.98x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 566 ms: 1.96x faster                                              |
| async_tree_io              | 1.08 sec                                               | 598 ms: 1.81x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                              |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 346 ms: 1.60x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 494 ms: 1.46x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 526 ms: 1.36x faster                                              |
| deepcopy                   | 352 us                                                 | 302 us: 1.16x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                             |
| regex_effbot               | 3.17 ms                                                | 2.82 ms: 1.12x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 88.3 ms: 1.10x faster                                             |
| float                      | 80.8 ms                                                | 74.1 ms: 1.09x faster                                             |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                             |
| generators                 | 32.2 ms                                                | 29.9 ms: 1.08x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 37.4 us: 1.08x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                              |
| async_generators           | 384 ms                                                 | 368 ms: 1.05x faster                                              |
| spectral_norm              | 110 ms                                                 | 106 ms: 1.04x faster                                              |
| go                         | 139 ms                                                 | 134 ms: 1.04x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.60 sec: 1.03x faster                                            |
| scimark_sor                | 130 ms                                                 | 127 ms: 1.02x faster                                              |
| comprehensions             | 19.8 us                                                | 19.5 us: 1.02x faster                                             |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.01x faster                                            |
| regex_compile              | 142 ms                                                 | 145 ms: 1.01x slower                                              |
| logging_silent             | 109 ns                                                 | 111 ns: 1.02x slower                                              |
| dulwich_log                | 78.9 ms                                                | 80.7 ms: 1.02x slower                                             |
| docutils                   | 2.64 sec                                               | 2.74 sec: 1.04x slower                                            |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                              |
| chaos                      | 62.8 ms                                                | 66.3 ms: 1.06x slower                                             |
| pyflate                    | 448 ms                                                 | 474 ms: 1.06x slower                                              |
| raytrace                   | 299 ms                                                 | 316 ms: 1.06x slower                                              |
| tomli_loads                | 2.11 sec                                               | 2.23 sec: 1.06x slower                                            |
| logging_simple             | 6.63 us                                                | 7.02 us: 1.06x slower                                             |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 798 ms: 1.07x slower                                              |
| unpickle_pure_python       | 221 us                                                 | 237 us: 1.07x slower                                              |
| logging_format             | 7.35 us                                                | 7.92 us: 1.08x slower                                             |
| sqlalchemy_declarative     | 143 ms                                                 | 154 ms: 1.08x slower                                              |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                              |
| mdp                        | 2.42 sec                                               | 2.62 sec: 1.08x slower                                            |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.09x slower                                            |
| sqlglot_normalize          | 107 ms                                                 | 117 ms: 1.10x slower                                              |
| deltablue                  | 3.45 ms                                                | 3.79 ms: 1.10x slower                                             |
| scimark_fft                | 342 ms                                                 | 376 ms: 1.10x slower                                              |
| sympy_sum                  | 166 ms                                                 | 183 ms: 1.11x slower                                              |
| html5lib                   | 63.6 ms                                                | 70.3 ms: 1.11x slower                                             |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.11x slower                                             |
| thrift                     | 791 us                                                 | 881 us: 1.11x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 94.9 ms: 1.11x slower                                             |
| sqlglot_optimize           | 53.3 ms                                                | 60.1 ms: 1.13x slower                                             |
| 2to3                       | 264 ms                                                 | 297 ms: 1.13x slower                                              |
| sqlglot_transpile          | 1.67 ms                                                | 1.89 ms: 1.13x slower                                             |
| pickle_pure_python         | 308 us                                                 | 347 us: 1.13x slower                                              |
| genshi_xml                 | 50.2 ms                                                | 56.7 ms: 1.13x slower                                             |
| crypto_pyaes               | 76.6 ms                                                | 86.7 ms: 1.13x slower                                             |
| sympy_str                  | 292 ms                                                 | 331 ms: 1.13x slower                                              |
| hexiom                     | 6.17 ms                                                | 7.08 ms: 1.15x slower                                             |
| sympy_expand               | 468 ms                                                 | 540 ms: 1.15x slower                                              |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                             |
| nqueens                    | 80.1 ms                                                | 92.9 ms: 1.16x slower                                             |
| scimark_lu                 | 114 ms                                                 | 133 ms: 1.16x slower                                              |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.16x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 23.9 ms: 1.16x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 80.8 ms: 1.18x slower                                             |
| genshi_text                | 22.8 ms                                                | 27.0 ms: 1.18x slower                                             |
| json_loads                 | 26.5 us                                                | 31.4 us: 1.18x slower                                             |
| django_template            | 34.7 ms                                                | 41.3 ms: 1.19x slower                                             |
| richards                   | 45.9 ms                                                | 55.1 ms: 1.20x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.41 ms: 1.23x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                             |
| richards_super             | 51.9 ms                                                | 64.0 ms: 1.23x slower                                             |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.40 ms: 1.28x slower                                             |
| fannkuch                   | 372 ms                                                 | 477 ms: 1.28x slower                                              |
| telco                      | 6.53 ms                                                | 8.81 ms: 1.35x slower                                             |
| coverage                   | 71.4 ms                                                | 96.7 ms: 1.35x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.72 ms: 1.36x slower                                             |
| nbody                      | 89.3 ms                                                | 125 ms: 1.40x slower                                              |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.40x slower                                             |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.50x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.0 ms: 8.79x slower                                             |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                      |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, deepcopy_reduce
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250213-3.14.0a5+-68b535b-NOGIL/bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.027x slower

# HPT report

- Reliability score: 99.63% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.37x