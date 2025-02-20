# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: aa60561
- commit date: 2025-02-20
- overall geometric mean: 1.078x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 304 ms: 1.17x slower                                              |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                            |
| html5lib       | 68.6 ms                                                                | 73.2 ms: 1.07x slower                                             |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 559 ms: 1.61x faster                                              |
| async_tree_io              | 881 ms                                                                 | 602 ms: 1.46x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 243 ms: 1.37x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 344 ms: 1.33x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 313 ms: 1.31x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 501 ms: 1.26x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 532 ms: 1.25x faster                                              |
| async_tree_none            | 353 ms                                                                 | 283 ms: 1.25x faster                                              |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 520 ms: 1.00x slower                                              |
| coroutines                 | 23.3 ms                                                                | 23.9 ms: 1.02x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 198 ms: 1.09x faster                                              |
| float          | 76.7 ms                                                                | 74.7 ms: 1.03x faster                                             |
| nbody          | 85.3 ms                                                                | 128 ms: 1.51x slower                                              |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.91 ms: 1.10x faster                                             |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                              |
| regex_v8       | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                             |
| regex_compile  | 131 ms                                                                 | 155 ms: 1.18x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.7 ms: 1.08x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 95.2 ms: 1.12x slower                                             |
| json_loads           | 27.3 us                                                                | 31.4 us: 1.15x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.31 sec: 1.15x slower                                            |
| xml_etree_process    | 59.2 ms                                                                | 69.1 ms: 1.17x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 243 us: 1.17x slower                                              |
| json_dumps           | 10.6 ms                                                                | 13.0 ms: 1.23x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 363 us: 1.24x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.82 ms: 1.32x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.38x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.7 ms: 1.22x slower                                             |
| genshi_text     | 21.7 ms                                                                | 27.6 ms: 1.27x slower                                             |
| django_template | 34.2 ms                                                                | 43.9 ms: 1.28x slower                                             |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.75 ms: 1.90x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 559 ms: 1.61x faster                                              |
| async_tree_io              | 881 ms                                                                 | 602 ms: 1.46x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 243 ms: 1.37x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 344 ms: 1.33x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 313 ms: 1.31x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 501 ms: 1.26x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 532 ms: 1.25x faster                                              |
| async_tree_none            | 353 ms                                                                 | 283 ms: 1.25x faster                                              |
| deepcopy                   | 357 us                                                                 | 308 us: 1.16x faster                                              |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                             |
| regex_effbot               | 3.21 ms                                                                | 2.91 ms: 1.10x faster                                             |
| pidigits                   | 216 ms                                                                 | 198 ms: 1.09x faster                                              |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.7 ms: 1.08x faster                                             |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                              |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                              |
| go                         | 141 ms                                                                 | 137 ms: 1.03x faster                                              |
| float                      | 76.7 ms                                                                | 74.7 ms: 1.03x faster                                             |
| scimark_sor                | 134 ms                                                                 | 131 ms: 1.02x faster                                              |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 520 ms: 1.00x slower                                              |
| regex_v8                   | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                             |
| coroutines                 | 23.3 ms                                                                | 23.9 ms: 1.02x slower                                             |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.03x slower                                             |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.04x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.71 sec: 1.06x slower                                            |
| docutils                   | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                            |
| html5lib                   | 68.6 ms                                                                | 73.2 ms: 1.07x slower                                             |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                            |
| json                       | 4.98 ms                                                                | 5.35 ms: 1.07x slower                                             |
| pyflate                    | 449 ms                                                                 | 494 ms: 1.10x slower                                              |
| generators                 | 28.5 ms                                                                | 31.4 ms: 1.10x slower                                             |
| telco                      | 7.77 ms                                                                | 8.62 ms: 1.11x slower                                             |
| dulwich_log                | 74.5 ms                                                                | 82.8 ms: 1.11x slower                                             |
| xml_etree_generate         | 85.4 ms                                                                | 95.2 ms: 1.12x slower                                             |
| scimark_fft                | 348 ms                                                                 | 391 ms: 1.12x slower                                              |
| logging_silent             | 98.2 ns                                                                | 110 ns: 1.12x slower                                              |
| sqlglot_normalize          | 106 ms                                                                 | 121 ms: 1.15x slower                                              |
| json_loads                 | 27.3 us                                                                | 31.4 us: 1.15x slower                                             |
| tomli_loads                | 2.01 sec                                                               | 2.31 sec: 1.15x slower                                            |
| pprint_safe_repr           | 719 ms                                                                 | 836 ms: 1.16x slower                                              |
| xml_etree_process          | 59.2 ms                                                                | 69.1 ms: 1.17x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 243 us: 1.17x slower                                              |
| sqlglot_optimize           | 52.7 ms                                                                | 61.5 ms: 1.17x slower                                             |
| logging_format             | 6.92 us                                                                | 8.09 us: 1.17x slower                                             |
| thrift                     | 772 us                                                                 | 903 us: 1.17x slower                                              |
| 2to3                       | 259 ms                                                                 | 304 ms: 1.17x slower                                              |
| mdp                        | 2.34 sec                                                               | 2.76 sec: 1.18x slower                                            |
| regex_compile              | 131 ms                                                                 | 155 ms: 1.18x slower                                              |
| logging_simple             | 6.14 us                                                                | 7.26 us: 1.18x slower                                             |
| pprint_pformat             | 1.46 sec                                                               | 1.72 sec: 1.18x slower                                            |
| coverage                   | 82.5 ms                                                                | 98.0 ms: 1.19x slower                                             |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.19x slower                                             |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.71 ms: 1.20x slower                                             |
| sympy_expand               | 454 ms                                                                 | 548 ms: 1.21x slower                                              |
| hexiom                     | 5.95 ms                                                                | 7.22 ms: 1.21x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                              |
| genshi_xml                 | 49.1 ms                                                                | 59.7 ms: 1.22x slower                                             |
| sympy_integrate            | 19.7 ms                                                                | 24.1 ms: 1.22x slower                                             |
| nqueens                    | 77.7 ms                                                                | 95.0 ms: 1.22x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.79 ms: 1.22x slower                                             |
| json_dumps                 | 10.6 ms                                                                | 13.0 ms: 1.23x slower                                             |
| richards                   | 44.4 ms                                                                | 54.6 ms: 1.23x slower                                             |
| chaos                      | 56.3 ms                                                                | 69.2 ms: 1.23x slower                                             |
| sympy_str                  | 274 ms                                                                 | 340 ms: 1.24x slower                                              |
| pickle_pure_python         | 292 us                                                                 | 363 us: 1.24x slower                                              |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.2 ms: 1.25x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 141 ms: 1.25x slower                                              |
| richards_super             | 50.4 ms                                                                | 63.7 ms: 1.26x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                              |
| genshi_text                | 21.7 ms                                                                | 27.6 ms: 1.27x slower                                             |
| raytrace                   | 250 ms                                                                 | 319 ms: 1.28x slower                                              |
| crypto_pyaes               | 68.2 ms                                                                | 87.4 ms: 1.28x slower                                             |
| django_template            | 34.2 ms                                                                | 43.9 ms: 1.28x slower                                             |
| fannkuch                   | 376 ms                                                                 | 489 ms: 1.30x slower                                              |
| meteor_contest             | 101 ms                                                                 | 132 ms: 1.30x slower                                              |
| sqlglot_transpile          | 1.55 ms                                                                | 2.06 ms: 1.32x slower                                             |
| python_startup_no_site     | 7.41 ms                                                                | 9.82 ms: 1.32x slower                                             |
| sqlglot_parse              | 1.25 ms                                                                | 1.67 ms: 1.34x slower                                             |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                             |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                             |
| nbody                      | 85.3 ms                                                                | 128 ms: 1.51x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.30 ms: 3.57x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 96.7 ms: 8.79x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (4): deepcopy_memo, spectral_norm, deepcopy_reduce, pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250220-3.14.0a5+-aa60561-NOGIL/bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.078x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.36x