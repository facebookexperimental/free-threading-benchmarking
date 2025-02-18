# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: c3669ca
- commit date: 2025-02-17
- overall geometric mean: 1.061x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 308 ms: 1.17x slower                                              |
| docutils       | 2.64 sec                                               | 2.81 sec: 1.06x slower                                            |
| html5lib       | 63.6 ms                                                | 71.6 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                              |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                              |
| async_tree_none            | 464 ms                                                 | 290 ms: 1.60x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 356 ms: 1.56x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 554 ms: 1.31x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 589 ms: 1.21x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                             |
| async_generators           | 384 ms                                                 | 379 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                              |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.3 ms: 1.03x faster                                             |
| pidigits       | 184 ms                                                 | 219 ms: 1.19x slower                                              |
| nbody          | 89.3 ms                                                | 137 ms: 1.53x slower                                              |
| Geometric mean | (ref)                                                  | 1.21x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                             |
| regex_compile  | 142 ms                                                 | 153 ms: 1.07x slower                                              |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.04x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.6 ms: 1.08x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.11x slower                                            |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.13x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 97.6 ms: 1.14x slower                                             |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                             |
| pickle_pure_python   | 308 us                                                 | 366 us: 1.19x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 70.9 ms: 1.20x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.25x slower                                             |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.68 ms: 1.35x slower                                             |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.56x slower                                             |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.0 ms: 1.19x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.9 ms: 1.22x slower                                             |
| django_template | 34.7 ms                                                | 43.3 ms: 1.25x slower                                             |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                             |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.98x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                              |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                              |
| async_tree_none            | 464 ms                                                 | 290 ms: 1.60x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 356 ms: 1.56x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 554 ms: 1.31x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 589 ms: 1.21x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                             |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 89.6 ms: 1.08x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 38.7 us: 1.04x faster                                             |
| float                      | 80.8 ms                                                | 78.3 ms: 1.03x faster                                             |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                             |
| async_generators           | 384 ms                                                 | 379 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.72 sec: 1.00x faster                                            |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                              |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.01x slower                                              |
| comprehensions             | 19.8 us                                                | 20.5 us: 1.03x slower                                             |
| pycparser                  | 1.17 sec                                               | 1.21 sec: 1.03x slower                                            |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.20 us: 1.04x slower                                             |
| logging_silent             | 109 ns                                                 | 115 ns: 1.05x slower                                              |
| dulwich_log                | 78.9 ms                                                | 83.9 ms: 1.06x slower                                             |
| docutils                   | 2.64 sec                                               | 2.81 sec: 1.06x slower                                            |
| regex_compile              | 142 ms                                                 | 153 ms: 1.07x slower                                              |
| json                       | 5.02 ms                                                | 5.42 ms: 1.08x slower                                             |
| logging_simple             | 6.63 us                                                | 7.21 us: 1.09x slower                                             |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                              |
| raytrace                   | 299 ms                                                 | 331 ms: 1.11x slower                                              |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                              |
| pyflate                    | 448 ms                                                 | 497 ms: 1.11x slower                                              |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.11x slower                                            |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.4 ms: 1.12x slower                                             |
| logging_format             | 7.35 us                                                | 8.25 us: 1.12x slower                                             |
| html5lib                   | 63.6 ms                                                | 71.6 ms: 1.13x slower                                             |
| chaos                      | 62.8 ms                                                | 71.1 ms: 1.13x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 840 ms: 1.13x slower                                              |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                             |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.13x slower                                              |
| sympy_sum                  | 166 ms                                                 | 189 ms: 1.14x slower                                              |
| pprint_pformat             | 1.52 sec                                               | 1.73 sec: 1.14x slower                                            |
| thrift                     | 791 us                                                 | 905 us: 1.14x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 97.6 ms: 1.14x slower                                             |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.15x slower                                              |
| deltablue                  | 3.45 ms                                                | 3.96 ms: 1.15x slower                                             |
| mdp                        | 2.42 sec                                               | 2.78 sec: 1.15x slower                                            |
| 2to3                       | 264 ms                                                 | 308 ms: 1.17x slower                                              |
| sympy_str                  | 292 ms                                                 | 342 ms: 1.17x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 62.5 ms: 1.17x slower                                             |
| scimark_fft                | 342 ms                                                 | 402 ms: 1.18x slower                                              |
| sqlglot_transpile          | 1.67 ms                                                | 1.98 ms: 1.18x slower                                             |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                             |
| sympy_expand               | 468 ms                                                 | 555 ms: 1.19x slower                                              |
| pickle_pure_python         | 308 us                                                 | 366 us: 1.19x slower                                              |
| pidigits                   | 184 ms                                                 | 219 ms: 1.19x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 91.2 ms: 1.19x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 60.0 ms: 1.19x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.6 ms: 1.20x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.41 ms: 1.20x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 70.9 ms: 1.20x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.65 ms: 1.21x slower                                             |
| nqueens                    | 80.1 ms                                                | 97.6 ms: 1.22x slower                                             |
| genshi_text                | 22.8 ms                                                | 27.9 ms: 1.22x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.23x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 84.1 ms: 1.23x slower                                             |
| richards                   | 45.9 ms                                                | 57.1 ms: 1.24x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.25x slower                                             |
| django_template            | 34.7 ms                                                | 43.3 ms: 1.25x slower                                             |
| scimark_lu                 | 114 ms                                                 | 143 ms: 1.25x slower                                              |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.27x slower                                             |
| richards_super             | 51.9 ms                                                | 66.2 ms: 1.28x slower                                             |
| telco                      | 6.53 ms                                                | 8.62 ms: 1.32x slower                                             |
| fannkuch                   | 372 ms                                                 | 495 ms: 1.33x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.87 ms: 1.34x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.68 ms: 1.35x slower                                             |
| coverage                   | 71.4 ms                                                | 97.9 ms: 1.37x slower                                             |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                             |
| nbody                      | 89.3 ms                                                | 137 ms: 1.53x slower                                              |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.56x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.1 ms: 8.81x slower                                             |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                      |

Benchmark hidden because not significant (2): generators, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250217-3.14.0a5+-c3669ca-NOGIL/bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.061x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.36x