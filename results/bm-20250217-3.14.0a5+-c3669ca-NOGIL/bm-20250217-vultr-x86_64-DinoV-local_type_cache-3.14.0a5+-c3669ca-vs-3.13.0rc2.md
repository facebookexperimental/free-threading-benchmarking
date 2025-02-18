# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: c3669ca
- commit date: 2025-02-17
- overall geometric mean: 1.093x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 308 ms: 1.19x slower                                              |
| docutils       | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                            |
| html5lib       | 68.6 ms                                                                | 71.6 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 579 ms: 1.56x faster                                              |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 356 ms: 1.29x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 260 ms: 1.28x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 321 ms: 1.28x faster                                              |
| async_tree_none            | 353 ms                                                                 | 290 ms: 1.22x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 554 ms: 1.14x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 589 ms: 1.13x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                             |
| async_generators           | 375 ms                                                                 | 379 ms: 1.01x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.20x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 219 ms: 1.01x slower                                              |
| float          | 76.7 ms                                                                | 78.3 ms: 1.02x slower                                             |
| nbody          | 85.3 ms                                                                | 137 ms: 1.61x slower                                              |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.80 ms: 1.15x faster                                             |
| regex_dna      | 189 ms                                                                 | 186 ms: 1.01x faster                                              |
| regex_v8       | 23.2 ms                                                                | 23.3 ms: 1.01x slower                                             |
| regex_compile  | 131 ms                                                                 | 153 ms: 1.16x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 89.6 ms: 1.05x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 97.6 ms: 1.14x slower                                             |
| json_loads           | 27.3 us                                                                | 31.5 us: 1.15x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                            |
| xml_etree_process    | 59.2 ms                                                                | 70.9 ms: 1.20x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 366 us: 1.25x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.13x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.68 ms: 1.31x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.0 ms: 1.22x slower                                             |
| django_template | 34.2 ms                                                                | 43.3 ms: 1.27x slower                                             |
| genshi_text     | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                             |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.75 ms: 1.90x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 579 ms: 1.56x faster                                              |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 356 ms: 1.29x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 260 ms: 1.28x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 321 ms: 1.28x faster                                              |
| async_tree_none            | 353 ms                                                                 | 290 ms: 1.22x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.80 ms: 1.15x faster                                             |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 554 ms: 1.14x faster                                              |
| deepcopy                   | 357 us                                                                 | 314 us: 1.14x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 589 ms: 1.13x faster                                              |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                             |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.6 ms: 1.05x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                              |
| regex_dna                  | 189 ms                                                                 | 186 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                              |
| scimark_sor                | 134 ms                                                                 | 134 ms: 1.00x slower                                              |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                             |
| regex_v8                   | 23.2 ms                                                                | 23.3 ms: 1.01x slower                                             |
| async_generators           | 375 ms                                                                 | 379 ms: 1.01x slower                                              |
| pidigits                   | 216 ms                                                                 | 219 ms: 1.01x slower                                              |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                             |
| deepcopy_memo              | 38.1 us                                                                | 38.7 us: 1.02x slower                                             |
| float                      | 76.7 ms                                                                | 78.3 ms: 1.02x slower                                             |
| deepcopy_reduce            | 3.12 us                                                                | 3.20 us: 1.03x slower                                             |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.04x slower                                              |
| create_gc_cycles           | 1.33 ms                                                                | 1.39 ms: 1.04x slower                                             |
| html5lib                   | 68.6 ms                                                                | 71.6 ms: 1.04x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.72 sec: 1.06x slower                                            |
| docutils                   | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                            |
| pycparser                  | 1.12 sec                                                               | 1.21 sec: 1.08x slower                                            |
| json                       | 4.98 ms                                                                | 5.42 ms: 1.09x slower                                             |
| pyflate                    | 449 ms                                                                 | 497 ms: 1.11x slower                                              |
| telco                      | 7.77 ms                                                                | 8.62 ms: 1.11x slower                                             |
| dulwich_log                | 74.5 ms                                                                | 83.9 ms: 1.13x slower                                             |
| generators                 | 28.5 ms                                                                | 32.2 ms: 1.13x slower                                             |
| xml_etree_generate         | 85.4 ms                                                                | 97.6 ms: 1.14x slower                                             |
| json_loads                 | 27.3 us                                                                | 31.5 us: 1.15x slower                                             |
| scimark_fft                | 348 ms                                                                 | 402 ms: 1.15x slower                                              |
| sqlglot_normalize          | 106 ms                                                                 | 122 ms: 1.16x slower                                              |
| regex_compile              | 131 ms                                                                 | 153 ms: 1.16x slower                                              |
| logging_silent             | 98.2 ns                                                                | 115 ns: 1.17x slower                                              |
| tomli_loads                | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                            |
| pprint_safe_repr           | 719 ms                                                                 | 840 ms: 1.17x slower                                              |
| thrift                     | 772 us                                                                 | 905 us: 1.17x slower                                              |
| logging_simple             | 6.14 us                                                                | 7.21 us: 1.17x slower                                             |
| 2to3                       | 259 ms                                                                 | 308 ms: 1.19x slower                                              |
| coverage                   | 82.5 ms                                                                | 97.9 ms: 1.19x slower                                             |
| sqlglot_optimize           | 52.7 ms                                                                | 62.5 ms: 1.19x slower                                             |
| pprint_pformat             | 1.46 sec                                                               | 1.73 sec: 1.19x slower                                            |
| mdp                        | 2.34 sec                                                               | 2.78 sec: 1.19x slower                                            |
| logging_format             | 6.92 us                                                                | 8.25 us: 1.19x slower                                             |
| xml_etree_process          | 59.2 ms                                                                | 70.9 ms: 1.20x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                              |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                             |
| genshi_xml                 | 49.1 ms                                                                | 60.0 ms: 1.22x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 189 ms: 1.22x slower                                              |
| sympy_expand               | 454 ms                                                                 | 555 ms: 1.22x slower                                              |
| comprehensions             | 16.6 us                                                                | 20.5 us: 1.23x slower                                             |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.87 ms: 1.24x slower                                             |
| hexiom                     | 5.95 ms                                                                | 7.41 ms: 1.24x slower                                             |
| sympy_integrate            | 19.7 ms                                                                | 24.6 ms: 1.25x slower                                             |
| sympy_str                  | 274 ms                                                                 | 342 ms: 1.25x slower                                              |
| pickle_pure_python         | 292 us                                                                 | 366 us: 1.25x slower                                              |
| nqueens                    | 77.7 ms                                                                | 97.6 ms: 1.26x slower                                             |
| chaos                      | 56.3 ms                                                                | 71.1 ms: 1.26x slower                                             |
| django_template            | 34.2 ms                                                                | 43.3 ms: 1.27x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 143 ms: 1.27x slower                                              |
| sqlglot_transpile          | 1.55 ms                                                                | 1.98 ms: 1.27x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 84.1 ms: 1.28x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.96 ms: 1.28x slower                                             |
| genshi_text                | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 200 us: 1.29x slower                                              |
| richards                   | 44.4 ms                                                                | 57.1 ms: 1.29x slower                                             |
| meteor_contest             | 101 ms                                                                 | 131 ms: 1.30x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.68 ms: 1.31x slower                                             |
| richards_super             | 50.4 ms                                                                | 66.2 ms: 1.31x slower                                             |
| fannkuch                   | 376 ms                                                                 | 495 ms: 1.32x slower                                              |
| sqlglot_parse              | 1.25 ms                                                                | 1.65 ms: 1.32x slower                                             |
| raytrace                   | 250 ms                                                                 | 331 ms: 1.32x slower                                              |
| crypto_pyaes               | 68.2 ms                                                                | 91.2 ms: 1.34x slower                                             |
| python_startup             | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                             |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                             |
| nbody                      | 85.3 ms                                                                | 137 ms: 1.61x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.33 ms: 3.60x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 95.1 ms: 8.65x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.14x slower                                                      |

Benchmark hidden because not significant (2): go, pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250217-3.14.0a5+-c3669ca-NOGIL/bm-20250217-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-c3669ca.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.093x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.35x