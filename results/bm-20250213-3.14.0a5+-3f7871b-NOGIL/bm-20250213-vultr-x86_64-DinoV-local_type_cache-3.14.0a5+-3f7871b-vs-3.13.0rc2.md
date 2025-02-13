# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 3f7871b
- commit date: 2025-02-13
- overall geometric mean: 1.084x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 304 ms: 1.17x slower                                              |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                            |
| html5lib       | 68.6 ms                                                                | 72.9 ms: 1.06x slower                                             |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 579 ms: 1.56x faster                                              |
| async_tree_io              | 881 ms                                                                 | 606 ms: 1.45x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 356 ms: 1.29x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 260 ms: 1.28x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 320 ms: 1.28x faster                                              |
| async_tree_none            | 353 ms                                                                 | 289 ms: 1.22x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 559 ms: 1.13x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 591 ms: 1.13x faster                                              |
| async_generators           | 375 ms                                                                 | 374 ms: 1.00x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.20x faster                                                      |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 206 ms: 1.05x faster                                              |
| nbody          | 85.3 ms                                                                | 129 ms: 1.51x slower                                              |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.87 ms: 1.12x faster                                             |
| regex_dna      | 189 ms                                                                 | 185 ms: 1.02x faster                                              |
| regex_v8       | 23.2 ms                                                                | 23.1 ms: 1.01x faster                                             |
| regex_compile  | 131 ms                                                                 | 153 ms: 1.16x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 96.9 ms: 1.13x slower                                             |
| json_loads           | 27.3 us                                                                | 31.2 us: 1.14x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                            |
| xml_etree_process    | 59.2 ms                                                                | 70.2 ms: 1.19x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 249 us: 1.19x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 358 us: 1.23x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.64 ms: 1.30x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.4 ms: 1.39x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.7 ms: 1.22x slower                                             |
| django_template | 34.2 ms                                                                | 42.4 ms: 1.24x slower                                             |
| genshi_text     | 21.7 ms                                                                | 28.4 ms: 1.30x slower                                             |
| mako            | 11.2 ms                                                                | 16.0 ms: 1.42x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.75 ms: 1.90x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 579 ms: 1.56x faster                                              |
| async_tree_io              | 881 ms                                                                 | 606 ms: 1.45x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 356 ms: 1.29x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 260 ms: 1.28x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 320 ms: 1.28x faster                                              |
| async_tree_none            | 353 ms                                                                 | 289 ms: 1.22x faster                                              |
| deepcopy                   | 357 us                                                                 | 308 us: 1.16x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 559 ms: 1.13x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 591 ms: 1.13x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.87 ms: 1.12x faster                                             |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                             |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| pidigits                   | 216 ms                                                                 | 206 ms: 1.05x faster                                              |
| scimark_sor                | 134 ms                                                                 | 131 ms: 1.02x faster                                              |
| regex_dna                  | 189 ms                                                                 | 185 ms: 1.02x faster                                              |
| go                         | 141 ms                                                                 | 140 ms: 1.01x faster                                              |
| regex_v8                   | 23.2 ms                                                                | 23.1 ms: 1.01x faster                                             |
| async_generators           | 375 ms                                                                 | 374 ms: 1.00x faster                                              |
| deepcopy_reduce            | 3.12 us                                                                | 3.14 us: 1.01x slower                                             |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                              |
| create_gc_cycles           | 1.33 ms                                                                | 1.39 ms: 1.04x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.69 sec: 1.05x slower                                            |
| html5lib                   | 68.6 ms                                                                | 72.9 ms: 1.06x slower                                             |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.07x slower                                            |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                            |
| json                       | 4.98 ms                                                                | 5.38 ms: 1.08x slower                                             |
| pyflate                    | 449 ms                                                                 | 493 ms: 1.10x slower                                              |
| telco                      | 7.77 ms                                                                | 8.54 ms: 1.10x slower                                             |
| dulwich_log                | 74.5 ms                                                                | 83.1 ms: 1.12x slower                                             |
| generators                 | 28.5 ms                                                                | 31.9 ms: 1.12x slower                                             |
| scimark_fft                | 348 ms                                                                 | 390 ms: 1.12x slower                                              |
| xml_etree_generate         | 85.4 ms                                                                | 96.9 ms: 1.13x slower                                             |
| logging_silent             | 98.2 ns                                                                | 111 ns: 1.13x slower                                              |
| json_loads                 | 27.3 us                                                                | 31.2 us: 1.14x slower                                             |
| sqlglot_normalize          | 106 ms                                                                 | 121 ms: 1.14x slower                                              |
| pprint_safe_repr           | 719 ms                                                                 | 824 ms: 1.15x slower                                              |
| mdp                        | 2.34 sec                                                               | 2.71 sec: 1.16x slower                                            |
| pprint_pformat             | 1.46 sec                                                               | 1.69 sec: 1.16x slower                                            |
| thrift                     | 772 us                                                                 | 897 us: 1.16x slower                                              |
| regex_compile              | 131 ms                                                                 | 153 ms: 1.16x slower                                              |
| logging_simple             | 6.14 us                                                                | 7.14 us: 1.16x slower                                             |
| tomli_loads                | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                            |
| sqlglot_optimize           | 52.7 ms                                                                | 61.7 ms: 1.17x slower                                             |
| coverage                   | 82.5 ms                                                                | 96.7 ms: 1.17x slower                                             |
| 2to3                       | 259 ms                                                                 | 304 ms: 1.17x slower                                              |
| logging_format             | 6.92 us                                                                | 8.14 us: 1.18x slower                                             |
| xml_etree_process          | 59.2 ms                                                                | 70.2 ms: 1.19x slower                                             |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.19x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 249 us: 1.19x slower                                              |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                             |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.78 ms: 1.22x slower                                             |
| genshi_xml                 | 49.1 ms                                                                | 59.7 ms: 1.22x slower                                             |
| sympy_expand               | 454 ms                                                                 | 552 ms: 1.22x slower                                              |
| sympy_sum                  | 154 ms                                                                 | 188 ms: 1.22x slower                                              |
| pickle_pure_python         | 292 us                                                                 | 358 us: 1.23x slower                                              |
| chaos                      | 56.3 ms                                                                | 69.4 ms: 1.23x slower                                             |
| django_template            | 34.2 ms                                                                | 42.4 ms: 1.24x slower                                             |
| hexiom                     | 5.95 ms                                                                | 7.38 ms: 1.24x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 139 ms: 1.24x slower                                              |
| sympy_str                  | 274 ms                                                                 | 340 ms: 1.24x slower                                              |
| nqueens                    | 77.7 ms                                                                | 96.6 ms: 1.24x slower                                             |
| sympy_integrate            | 19.7 ms                                                                | 24.6 ms: 1.25x slower                                             |
| sqlglot_transpile          | 1.55 ms                                                                | 1.94 ms: 1.25x slower                                             |
| richards                   | 44.4 ms                                                                | 55.7 ms: 1.25x slower                                             |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                              |
| scimark_monte_carlo        | 65.8 ms                                                                | 84.5 ms: 1.28x slower                                             |
| richards_super             | 50.4 ms                                                                | 65.0 ms: 1.29x slower                                             |
| fannkuch                   | 376 ms                                                                 | 487 ms: 1.29x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.64 ms: 1.30x slower                                             |
| sqlglot_parse              | 1.25 ms                                                                | 1.63 ms: 1.30x slower                                             |
| genshi_text                | 21.7 ms                                                                | 28.4 ms: 1.30x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 203 us: 1.31x slower                                              |
| raytrace                   | 250 ms                                                                 | 326 ms: 1.31x slower                                              |
| crypto_pyaes               | 68.2 ms                                                                | 89.7 ms: 1.32x slower                                             |
| deltablue                  | 3.10 ms                                                                | 4.10 ms: 1.32x slower                                             |
| python_startup             | 11.0 ms                                                                | 15.4 ms: 1.39x slower                                             |
| mako                       | 11.2 ms                                                                | 16.0 ms: 1.42x slower                                             |
| nbody                      | 85.3 ms                                                                | 129 ms: 1.51x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.34 ms: 3.62x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 94.9 ms: 8.62x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (6): pathlib, coroutines, float, deepcopy_memo, asyncio_websockets, pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250213-3.14.0a5+-3f7871b-NOGIL/bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.084x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x