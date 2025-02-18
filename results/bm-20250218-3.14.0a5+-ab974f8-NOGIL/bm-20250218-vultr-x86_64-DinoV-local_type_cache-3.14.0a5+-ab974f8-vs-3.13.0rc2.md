# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: ab974f8
- commit date: 2025-02-18
- overall geometric mean: 1.084x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 307 ms: 1.18x slower                                              |
| docutils       | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                            |
| html5lib       | 68.6 ms                                                                | 73.4 ms: 1.07x slower                                             |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 582 ms: 1.55x faster                                              |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 359 ms: 1.28x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 261 ms: 1.27x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 322 ms: 1.27x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 507 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 543 ms: 1.23x faster                                              |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.21x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.01x faster                                              |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                              |
| float          | 76.7 ms                                                                | 78.4 ms: 1.02x slower                                             |
| nbody          | 85.3 ms                                                                | 130 ms: 1.52x slower                                              |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.81 ms: 1.14x faster                                             |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.04x faster                                              |
| regex_v8       | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                             |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.16x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 96.8 ms: 1.13x slower                                             |
| json_loads           | 27.3 us                                                                | 31.0 us: 1.14x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                            |
| xml_etree_process    | 59.2 ms                                                                | 70.1 ms: 1.18x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 249 us: 1.20x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 360 us: 1.23x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.74 ms: 1.31x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.1 ms: 1.22x slower                                             |
| django_template | 34.2 ms                                                                | 43.0 ms: 1.26x slower                                             |
| genshi_text     | 21.7 ms                                                                | 28.2 ms: 1.30x slower                                             |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.75 ms: 1.89x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 582 ms: 1.55x faster                                              |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 359 ms: 1.28x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 261 ms: 1.27x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 322 ms: 1.27x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 507 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 543 ms: 1.23x faster                                              |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.21x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.81 ms: 1.14x faster                                             |
| deepcopy                   | 357 us                                                                 | 315 us: 1.14x faster                                              |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                              |
| sqlite_synth               | 2.25 us                                                                | 2.06 us: 1.09x faster                                             |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                              |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.04x faster                                              |
| scimark_sor                | 134 ms                                                                 | 132 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.01x faster                                              |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                              |
| deepcopy_reduce            | 3.12 us                                                                | 3.14 us: 1.01x slower                                             |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                             |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                             |
| deepcopy_memo              | 38.1 us                                                                | 38.6 us: 1.01x slower                                             |
| regex_v8                   | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                             |
| float                      | 76.7 ms                                                                | 78.4 ms: 1.02x slower                                             |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.03x slower                                              |
| create_gc_cycles           | 1.33 ms                                                                | 1.39 ms: 1.05x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.71 sec: 1.06x slower                                            |
| docutils                   | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                            |
| html5lib                   | 68.6 ms                                                                | 73.4 ms: 1.07x slower                                             |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                            |
| json                       | 4.98 ms                                                                | 5.36 ms: 1.08x slower                                             |
| telco                      | 7.77 ms                                                                | 8.51 ms: 1.09x slower                                             |
| mdp                        | 2.34 sec                                                               | 2.59 sec: 1.11x slower                                            |
| dulwich_log                | 74.5 ms                                                                | 83.2 ms: 1.12x slower                                             |
| generators                 | 28.5 ms                                                                | 32.0 ms: 1.12x slower                                             |
| pyflate                    | 449 ms                                                                 | 509 ms: 1.13x slower                                              |
| scimark_fft                | 348 ms                                                                 | 395 ms: 1.13x slower                                              |
| xml_etree_generate         | 85.4 ms                                                                | 96.8 ms: 1.13x slower                                             |
| json_loads                 | 27.3 us                                                                | 31.0 us: 1.14x slower                                             |
| logging_silent             | 98.2 ns                                                                | 112 ns: 1.14x slower                                              |
| pprint_safe_repr           | 719 ms                                                                 | 826 ms: 1.15x slower                                              |
| sqlglot_normalize          | 106 ms                                                                 | 122 ms: 1.16x slower                                              |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.16x slower                                              |
| pprint_pformat             | 1.46 sec                                                               | 1.70 sec: 1.17x slower                                            |
| sqlglot_optimize           | 52.7 ms                                                                | 61.6 ms: 1.17x slower                                             |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                            |
| thrift                     | 772 us                                                                 | 910 us: 1.18x slower                                              |
| coverage                   | 82.5 ms                                                                | 97.4 ms: 1.18x slower                                             |
| 2to3                       | 259 ms                                                                 | 307 ms: 1.18x slower                                              |
| xml_etree_process          | 59.2 ms                                                                | 70.1 ms: 1.18x slower                                             |
| logging_simple             | 6.14 us                                                                | 7.29 us: 1.19x slower                                             |
| logging_format             | 6.92 us                                                                | 8.27 us: 1.20x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 249 us: 1.20x slower                                              |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.72 ms: 1.20x slower                                             |
| comprehensions             | 16.6 us                                                                | 20.0 us: 1.21x slower                                             |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 188 ms: 1.22x slower                                              |
| sympy_expand               | 454 ms                                                                 | 554 ms: 1.22x slower                                              |
| genshi_xml                 | 49.1 ms                                                                | 60.1 ms: 1.22x slower                                             |
| pickle_pure_python         | 292 us                                                                 | 360 us: 1.23x slower                                              |
| nqueens                    | 77.7 ms                                                                | 96.5 ms: 1.24x slower                                             |
| hexiom                     | 5.95 ms                                                                | 7.40 ms: 1.24x slower                                             |
| chaos                      | 56.3 ms                                                                | 70.0 ms: 1.24x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 140 ms: 1.24x slower                                              |
| sympy_integrate            | 19.7 ms                                                                | 24.6 ms: 1.25x slower                                             |
| sympy_str                  | 274 ms                                                                 | 342 ms: 1.25x slower                                              |
| django_template            | 34.2 ms                                                                | 43.0 ms: 1.26x slower                                             |
| sqlglot_transpile          | 1.55 ms                                                                | 1.96 ms: 1.26x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.1 ms: 1.26x slower                                             |
| richards                   | 44.4 ms                                                                | 56.5 ms: 1.27x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.95 ms: 1.28x slower                                             |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                              |
| typing_runtime_protocols   | 156 us                                                                 | 200 us: 1.29x slower                                              |
| crypto_pyaes               | 68.2 ms                                                                | 88.4 ms: 1.30x slower                                             |
| genshi_text                | 21.7 ms                                                                | 28.2 ms: 1.30x slower                                             |
| richards_super             | 50.4 ms                                                                | 65.6 ms: 1.30x slower                                             |
| raytrace                   | 250 ms                                                                 | 326 ms: 1.30x slower                                              |
| sqlglot_parse              | 1.25 ms                                                                | 1.63 ms: 1.31x slower                                             |
| fannkuch                   | 376 ms                                                                 | 494 ms: 1.31x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.74 ms: 1.31x slower                                             |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                             |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                             |
| nbody                      | 85.3 ms                                                                | 130 ms: 1.52x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.33 ms: 3.61x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 95.7 ms: 8.70x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (2): go, pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250218-3.14.0a5+-ab974f8-NOGIL/bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-ab974f8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.084x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.35x