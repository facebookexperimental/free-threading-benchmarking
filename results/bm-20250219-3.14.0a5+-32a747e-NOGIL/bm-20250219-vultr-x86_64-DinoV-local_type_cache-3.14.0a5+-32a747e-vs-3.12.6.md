# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 32a747e
- commit date: 2025-02-19
- overall geometric mean: 1.043x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 303 ms: 1.15x slower                                              |
| docutils       | 2.64 sec                                               | 2.73 sec: 1.03x slower                                            |
| html5lib       | 63.6 ms                                                | 72.2 ms: 1.14x slower                                             |
| Geometric mean | (ref)                                                  | 1.11x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 554 ms: 2.00x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                              |
| async_tree_io              | 1.08 sec                                               | 586 ms: 1.85x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                              |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 493 ms: 1.46x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 530 ms: 1.35x faster                                              |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.03x faster                                             |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                              |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.7 ms: 1.07x faster                                             |
| pidigits       | 184 ms                                                 | 199 ms: 1.08x slower                                              |
| nbody          | 89.3 ms                                                | 129 ms: 1.44x slower                                              |
| Geometric mean | (ref)                                                  | 1.13x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                             |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                              |
| regex_compile  | 142 ms                                                 | 154 ms: 1.08x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                             |
| Geometric mean | (ref)                                                  | 1.05x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.5 ms: 1.09x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.33 sec: 1.11x slower                                            |
| unpickle_pure_python | 221 us                                                 | 245 us: 1.11x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 96.3 ms: 1.13x slower                                             |
| pickle_pure_python   | 308 us                                                 | 360 us: 1.17x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 69.6 ms: 1.18x slower                                             |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                             |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.76 ms: 1.36x slower                                             |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                             |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.2 ms: 1.18x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.8 ms: 1.22x slower                                             |
| django_template | 34.7 ms                                                | 43.7 ms: 1.26x slower                                             |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                             |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 554 ms: 2.00x faster                                              |
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.97x faster                                             |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                              |
| async_tree_io              | 1.08 sec                                               | 586 ms: 1.85x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                              |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 493 ms: 1.46x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 530 ms: 1.35x faster                                              |
| deepcopy                   | 352 us                                                 | 309 us: 1.14x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                             |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 88.5 ms: 1.09x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.08x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 37.6 us: 1.07x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                              |
| float                      | 80.8 ms                                                | 75.7 ms: 1.07x faster                                             |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.03x faster                                             |
| generators                 | 32.2 ms                                                | 31.3 ms: 1.03x faster                                             |
| go                         | 139 ms                                                 | 137 ms: 1.01x faster                                              |
| logging_silent             | 109 ns                                                 | 108 ns: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.72 sec: 1.00x faster                                            |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                              |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                            |
| docutils                   | 2.64 sec                                               | 2.73 sec: 1.03x slower                                            |
| deepcopy_reduce            | 3.08 us                                                | 3.20 us: 1.04x slower                                             |
| dulwich_log                | 78.9 ms                                                | 82.6 ms: 1.05x slower                                             |
| json                       | 5.02 ms                                                | 5.35 ms: 1.06x slower                                             |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                              |
| raytrace                   | 299 ms                                                 | 323 ms: 1.08x slower                                              |
| pidigits                   | 184 ms                                                 | 199 ms: 1.08x slower                                              |
| regex_compile              | 142 ms                                                 | 154 ms: 1.08x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 155 ms: 1.09x slower                                              |
| pyflate                    | 448 ms                                                 | 490 ms: 1.09x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.9 ms: 1.10x slower                                             |
| deltablue                  | 3.45 ms                                                | 3.80 ms: 1.10x slower                                             |
| tomli_loads                | 2.11 sec                                               | 2.33 sec: 1.11x slower                                            |
| unpickle_pure_python       | 221 us                                                 | 245 us: 1.11x slower                                              |
| logging_simple             | 6.63 us                                                | 7.37 us: 1.11x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 829 ms: 1.12x slower                                              |
| chaos                      | 62.8 ms                                                | 70.4 ms: 1.12x slower                                             |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.12x slower                                              |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                            |
| logging_format             | 7.35 us                                                | 8.30 us: 1.13x slower                                             |
| xml_etree_generate         | 85.2 ms                                                | 96.3 ms: 1.13x slower                                             |
| thrift                     | 791 us                                                 | 895 us: 1.13x slower                                              |
| html5lib                   | 63.6 ms                                                | 72.2 ms: 1.14x slower                                             |
| scimark_fft                | 342 ms                                                 | 390 ms: 1.14x slower                                              |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.14x slower                                              |
| regex_v8                   | 20.6 ms                                                | 23.5 ms: 1.14x slower                                             |
| 2to3                       | 264 ms                                                 | 303 ms: 1.15x slower                                              |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                              |
| mdp                        | 2.42 sec                                               | 2.80 sec: 1.16x slower                                            |
| crypto_pyaes               | 76.6 ms                                                | 88.6 ms: 1.16x slower                                             |
| sqlglot_optimize           | 53.3 ms                                                | 61.9 ms: 1.16x slower                                             |
| sqlglot_transpile          | 1.67 ms                                                | 1.95 ms: 1.17x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 24.0 ms: 1.17x slower                                             |
| sympy_expand               | 468 ms                                                 | 547 ms: 1.17x slower                                              |
| pickle_pure_python         | 308 us                                                 | 360 us: 1.17x slower                                              |
| hexiom                     | 6.17 ms                                                | 7.24 ms: 1.17x slower                                             |
| richards                   | 45.9 ms                                                | 54.1 ms: 1.18x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 69.6 ms: 1.18x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 59.2 ms: 1.18x slower                                             |
| nqueens                    | 80.1 ms                                                | 94.8 ms: 1.18x slower                                             |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                              |
| sqlglot_parse              | 1.36 ms                                                | 1.63 ms: 1.20x slower                                             |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                              |
| richards_super             | 51.9 ms                                                | 63.0 ms: 1.21x slower                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 83.3 ms: 1.22x slower                                             |
| genshi_text                | 22.8 ms                                                | 27.8 ms: 1.22x slower                                             |
| scimark_lu                 | 114 ms                                                 | 140 ms: 1.23x slower                                              |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                             |
| django_template            | 34.7 ms                                                | 43.7 ms: 1.26x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.27x slower                                             |
| fannkuch                   | 372 ms                                                 | 483 ms: 1.30x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.71 ms: 1.30x slower                                             |
| telco                      | 6.53 ms                                                | 8.75 ms: 1.34x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.76 ms: 1.36x slower                                             |
| coverage                   | 71.4 ms                                                | 98.5 ms: 1.38x slower                                             |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                             |
| nbody                      | 89.3 ms                                                | 129 ms: 1.44x slower                                              |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.34 ms: 3.54x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 96.0 ms: 8.89x slower                                             |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                      |

Benchmark hidden because not significant (3): pylint, spectral_norm, comprehensions
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250219-3.14.0a5+-32a747e-NOGIL/bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.043x slower

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.37x