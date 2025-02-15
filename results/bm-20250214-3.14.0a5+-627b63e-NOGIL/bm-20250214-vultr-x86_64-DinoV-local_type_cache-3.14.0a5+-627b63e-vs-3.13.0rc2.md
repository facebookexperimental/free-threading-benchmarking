# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 627b63e
- commit date: 2025-02-14
- overall geometric mean: 1.084x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 307 ms: 1.18x slower                                              |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.06x slower                                            |
| html5lib       | 68.6 ms                                                                | 71.6 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 578 ms: 1.56x faster                                              |
| async_tree_io              | 881 ms                                                                 | 610 ms: 1.45x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 355 ms: 1.29x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 320 ms: 1.28x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 260 ms: 1.28x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 509 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 542 ms: 1.23x faster                                              |
| async_tree_none            | 353 ms                                                                 | 289 ms: 1.22x faster                                              |
| async_generators           | 375 ms                                                                 | 369 ms: 1.02x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                             |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                              |
| float          | 76.7 ms                                                                | 77.1 ms: 1.00x slower                                             |
| nbody          | 85.3 ms                                                                | 133 ms: 1.55x slower                                              |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.87 ms: 1.12x faster                                             |
| regex_dna      | 189 ms                                                                 | 184 ms: 1.03x faster                                              |
| regex_v8       | 23.2 ms                                                                | 25.0 ms: 1.08x slower                                             |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.16x slower                                              |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.8 ms: 1.06x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 97.0 ms: 1.14x slower                                             |
| json_loads           | 27.3 us                                                                | 31.1 us: 1.14x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                            |
| xml_etree_process    | 59.2 ms                                                                | 70.3 ms: 1.19x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.22x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 362 us: 1.24x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.71 ms: 1.31x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.40x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.3 ms: 1.21x slower                                             |
| django_template | 34.2 ms                                                                | 43.0 ms: 1.26x slower                                             |
| genshi_text     | 21.7 ms                                                                | 27.8 ms: 1.28x slower                                             |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.74 ms: 1.91x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 578 ms: 1.56x faster                                              |
| async_tree_io              | 881 ms                                                                 | 610 ms: 1.45x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 355 ms: 1.29x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 320 ms: 1.28x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 260 ms: 1.28x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 509 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 542 ms: 1.23x faster                                              |
| async_tree_none            | 353 ms                                                                 | 289 ms: 1.22x faster                                              |
| deepcopy                   | 357 us                                                                 | 310 us: 1.15x faster                                              |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.87 ms: 1.12x faster                                             |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                             |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.8 ms: 1.06x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                              |
| regex_dna                  | 189 ms                                                                 | 184 ms: 1.03x faster                                              |
| scimark_sor                | 134 ms                                                                 | 131 ms: 1.02x faster                                              |
| async_generators           | 375 ms                                                                 | 369 ms: 1.02x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                             |
| go                         | 141 ms                                                                 | 140 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                              |
| float                      | 76.7 ms                                                                | 77.1 ms: 1.00x slower                                             |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                             |
| deepcopy_memo              | 38.1 us                                                                | 38.7 us: 1.02x slower                                             |
| deepcopy_reduce            | 3.12 us                                                                | 3.20 us: 1.03x slower                                             |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.04x slower                                             |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.04x slower                                              |
| html5lib                   | 68.6 ms                                                                | 71.6 ms: 1.04x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.69 sec: 1.05x slower                                            |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.06x slower                                            |
| json                       | 4.98 ms                                                                | 5.36 ms: 1.08x slower                                             |
| regex_v8                   | 23.2 ms                                                                | 25.0 ms: 1.08x slower                                             |
| pycparser                  | 1.12 sec                                                               | 1.21 sec: 1.08x slower                                            |
| telco                      | 7.77 ms                                                                | 8.68 ms: 1.12x slower                                             |
| dulwich_log                | 74.5 ms                                                                | 83.2 ms: 1.12x slower                                             |
| logging_silent             | 98.2 ns                                                                | 110 ns: 1.12x slower                                              |
| generators                 | 28.5 ms                                                                | 32.1 ms: 1.13x slower                                             |
| xml_etree_generate         | 85.4 ms                                                                | 97.0 ms: 1.14x slower                                             |
| pyflate                    | 449 ms                                                                 | 510 ms: 1.14x slower                                              |
| json_loads                 | 27.3 us                                                                | 31.1 us: 1.14x slower                                             |
| scimark_fft                | 348 ms                                                                 | 396 ms: 1.14x slower                                              |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.14x slower                                              |
| mdp                        | 2.34 sec                                                               | 2.71 sec: 1.16x slower                                            |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.16x slower                                              |
| pprint_safe_repr           | 719 ms                                                                 | 836 ms: 1.16x slower                                              |
| sqlglot_optimize           | 52.7 ms                                                                | 61.7 ms: 1.17x slower                                             |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                            |
| logging_simple             | 6.14 us                                                                | 7.21 us: 1.17x slower                                             |
| coverage                   | 82.5 ms                                                                | 96.8 ms: 1.17x slower                                             |
| thrift                     | 772 us                                                                 | 911 us: 1.18x slower                                              |
| 2to3                       | 259 ms                                                                 | 307 ms: 1.18x slower                                              |
| pprint_pformat             | 1.46 sec                                                               | 1.72 sec: 1.18x slower                                            |
| xml_etree_process          | 59.2 ms                                                                | 70.3 ms: 1.19x slower                                             |
| logging_format             | 6.92 us                                                                | 8.21 us: 1.19x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                              |
| genshi_xml                 | 49.1 ms                                                                | 59.3 ms: 1.21x slower                                             |
| comprehensions             | 16.6 us                                                                | 20.1 us: 1.21x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                              |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.22x slower                                             |
| sympy_expand               | 454 ms                                                                 | 556 ms: 1.22x slower                                              |
| nqueens                    | 77.7 ms                                                                | 96.3 ms: 1.24x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 139 ms: 1.24x slower                                              |
| sympy_str                  | 274 ms                                                                 | 340 ms: 1.24x slower                                              |
| pickle_pure_python         | 292 us                                                                 | 362 us: 1.24x slower                                              |
| sympy_integrate            | 19.7 ms                                                                | 24.5 ms: 1.24x slower                                             |
| hexiom                     | 5.95 ms                                                                | 7.40 ms: 1.24x slower                                             |
| chaos                      | 56.3 ms                                                                | 70.2 ms: 1.25x slower                                             |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.94 ms: 1.25x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.88 ms: 1.25x slower                                             |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.25x slower                                              |
| richards                   | 44.4 ms                                                                | 55.7 ms: 1.25x slower                                             |
| django_template            | 34.2 ms                                                                | 43.0 ms: 1.26x slower                                             |
| sqlglot_transpile          | 1.55 ms                                                                | 1.97 ms: 1.27x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.6 ms: 1.27x slower                                             |
| genshi_text                | 21.7 ms                                                                | 27.8 ms: 1.28x slower                                             |
| richards_super             | 50.4 ms                                                                | 64.8 ms: 1.29x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 202 us: 1.30x slower                                              |
| raytrace                   | 250 ms                                                                 | 326 ms: 1.30x slower                                              |
| fannkuch                   | 376 ms                                                                 | 491 ms: 1.31x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.71 ms: 1.31x slower                                             |
| sqlglot_parse              | 1.25 ms                                                                | 1.63 ms: 1.31x slower                                             |
| crypto_pyaes               | 68.2 ms                                                                | 90.1 ms: 1.32x slower                                             |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.40x slower                                             |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                             |
| nbody                      | 85.3 ms                                                                | 133 ms: 1.55x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.32 ms: 3.59x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 95.0 ms: 8.63x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250214-3.14.0a5+-627b63e-NOGIL/bm-20250214-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-627b63e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.084x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.35x