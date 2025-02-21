# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 15d5533
- commit date: 2025-02-20
- overall geometric mean: 1.074x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 302 ms: 1.16x slower                                              |
| docutils       | 2.63 sec                                                               | 2.72 sec: 1.04x slower                                            |
| html5lib       | 68.6 ms                                                                | 72.1 ms: 1.05x slower                                             |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 553 ms: 1.63x faster                                              |
| async_tree_io              | 881 ms                                                                 | 585 ms: 1.51x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 341 ms: 1.35x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 306 ms: 1.34x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 489 ms: 1.29x faster                                              |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 523 ms: 1.27x faster                                              |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 194 ms: 1.12x faster                                              |
| float          | 76.7 ms                                                                | 76.4 ms: 1.00x faster                                             |
| nbody          | 85.3 ms                                                                | 128 ms: 1.50x slower                                              |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.87 ms: 1.12x faster                                             |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.03x faster                                              |
| regex_v8       | 23.2 ms                                                                | 23.9 ms: 1.03x slower                                             |
| regex_compile  | 131 ms                                                                 | 154 ms: 1.17x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 94.9 ms: 1.11x slower                                             |
| json_loads           | 27.3 us                                                                | 31.4 us: 1.15x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.33 sec: 1.16x slower                                            |
| xml_etree_process    | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 367 us: 1.26x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.75 ms: 1.32x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.0 ms: 1.20x slower                                             |
| django_template | 34.2 ms                                                                | 42.3 ms: 1.24x slower                                             |
| genshi_text     | 21.7 ms                                                                | 27.8 ms: 1.28x slower                                             |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.73 ms: 1.92x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 553 ms: 1.63x faster                                              |
| async_tree_io              | 881 ms                                                                 | 585 ms: 1.51x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 341 ms: 1.35x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 306 ms: 1.34x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 489 ms: 1.29x faster                                              |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 523 ms: 1.27x faster                                              |
| deepcopy                   | 357 us                                                                 | 308 us: 1.16x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.87 ms: 1.12x faster                                             |
| pidigits                   | 216 ms                                                                 | 194 ms: 1.12x faster                                              |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                             |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.03x faster                                              |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                              |
| float                      | 76.7 ms                                                                | 76.4 ms: 1.00x faster                                             |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                             |
| spectral_norm              | 108 ms                                                                 | 109 ms: 1.01x slower                                              |
| deepcopy_memo              | 38.1 us                                                                | 38.6 us: 1.01x slower                                             |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.02x slower                                             |
| regex_v8                   | 23.2 ms                                                                | 23.9 ms: 1.03x slower                                             |
| pathlib                    | 19.3 ms                                                                | 19.9 ms: 1.03x slower                                             |
| docutils                   | 2.63 sec                                                               | 2.72 sec: 1.04x slower                                            |
| html5lib                   | 68.6 ms                                                                | 72.1 ms: 1.05x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.72 sec: 1.06x slower                                            |
| json                       | 4.98 ms                                                                | 5.30 ms: 1.06x slower                                             |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                            |
| pyflate                    | 449 ms                                                                 | 496 ms: 1.10x slower                                              |
| xml_etree_generate         | 85.4 ms                                                                | 94.9 ms: 1.11x slower                                             |
| dulwich_log                | 74.5 ms                                                                | 82.8 ms: 1.11x slower                                             |
| generators                 | 28.5 ms                                                                | 31.7 ms: 1.11x slower                                             |
| scimark_fft                | 348 ms                                                                 | 390 ms: 1.12x slower                                              |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.13x slower                                              |
| thrift                     | 772 us                                                                 | 875 us: 1.13x slower                                              |
| telco                      | 7.77 ms                                                                | 8.82 ms: 1.13x slower                                             |
| mdp                        | 2.34 sec                                                               | 2.66 sec: 1.14x slower                                            |
| json_loads                 | 27.3 us                                                                | 31.4 us: 1.15x slower                                             |
| tomli_loads                | 2.01 sec                                                               | 2.33 sec: 1.16x slower                                            |
| logging_silent             | 98.2 ns                                                                | 114 ns: 1.16x slower                                              |
| sqlglot_optimize           | 52.7 ms                                                                | 61.1 ms: 1.16x slower                                             |
| logging_simple             | 6.14 us                                                                | 7.15 us: 1.16x slower                                             |
| 2to3                       | 259 ms                                                                 | 302 ms: 1.16x slower                                              |
| xml_etree_process          | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                             |
| pprint_safe_repr           | 719 ms                                                                 | 842 ms: 1.17x slower                                              |
| regex_compile              | 131 ms                                                                 | 154 ms: 1.17x slower                                              |
| logging_format             | 6.92 us                                                                | 8.13 us: 1.18x slower                                             |
| pprint_pformat             | 1.46 sec                                                               | 1.73 sec: 1.19x slower                                            |
| sympy_expand               | 454 ms                                                                 | 539 ms: 1.19x slower                                              |
| coverage                   | 82.5 ms                                                                | 98.3 ms: 1.19x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 184 ms: 1.19x slower                                              |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                              |
| genshi_xml                 | 49.1 ms                                                                | 59.0 ms: 1.20x slower                                             |
| sympy_integrate            | 19.7 ms                                                                | 23.7 ms: 1.20x slower                                             |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                             |
| comprehensions             | 16.6 us                                                                | 20.0 us: 1.21x slower                                             |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.73 ms: 1.21x slower                                             |
| sympy_str                  | 274 ms                                                                 | 332 ms: 1.21x slower                                              |
| hexiom                     | 5.95 ms                                                                | 7.34 ms: 1.23x slower                                             |
| sqlglot_transpile          | 1.55 ms                                                                | 1.92 ms: 1.23x slower                                             |
| richards                   | 44.4 ms                                                                | 54.9 ms: 1.24x slower                                             |
| django_template            | 34.2 ms                                                                | 42.3 ms: 1.24x slower                                             |
| chaos                      | 56.3 ms                                                                | 69.9 ms: 1.24x slower                                             |
| nqueens                    | 77.7 ms                                                                | 96.7 ms: 1.24x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 140 ms: 1.24x slower                                              |
| deltablue                  | 3.10 ms                                                                | 3.87 ms: 1.25x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.6 ms: 1.26x slower                                             |
| pickle_pure_python         | 292 us                                                                 | 367 us: 1.26x slower                                              |
| typing_runtime_protocols   | 156 us                                                                 | 197 us: 1.27x slower                                              |
| richards_super             | 50.4 ms                                                                | 64.0 ms: 1.27x slower                                             |
| crypto_pyaes               | 68.2 ms                                                                | 87.0 ms: 1.28x slower                                             |
| genshi_text                | 21.7 ms                                                                | 27.8 ms: 1.28x slower                                             |
| sqlglot_parse              | 1.25 ms                                                                | 1.60 ms: 1.28x slower                                             |
| meteor_contest             | 101 ms                                                                 | 131 ms: 1.29x slower                                              |
| raytrace                   | 250 ms                                                                 | 325 ms: 1.30x slower                                              |
| fannkuch                   | 376 ms                                                                 | 490 ms: 1.30x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.75 ms: 1.32x slower                                             |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                             |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                             |
| nbody                      | 85.3 ms                                                                | 128 ms: 1.50x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.31 ms: 3.58x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 95.9 ms: 8.72x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                      |

Benchmark hidden because not significant (5): pylint, scimark_sor, go, asyncio_websockets, deepcopy_reduce
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250220-3.14.0a5+-15d5533-NOGIL/bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.074x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x