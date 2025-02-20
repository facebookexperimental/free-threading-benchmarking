# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 32a747e
- commit date: 2025-02-19
- overall geometric mean: 1.075x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 303 ms: 1.17x slower                                              |
| docutils       | 2.63 sec                                                               | 2.73 sec: 1.04x slower                                            |
| html5lib       | 68.6 ms                                                                | 72.2 ms: 1.05x slower                                             |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 554 ms: 1.63x faster                                              |
| async_tree_io              | 881 ms                                                                 | 586 ms: 1.50x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 341 ms: 1.35x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 493 ms: 1.28x faster                                              |
| async_tree_none            | 353 ms                                                                 | 278 ms: 1.27x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 530 ms: 1.26x faster                                              |
| async_generators           | 375 ms                                                                 | 371 ms: 1.01x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                             |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 199 ms: 1.09x faster                                              |
| float          | 76.7 ms                                                                | 75.7 ms: 1.01x faster                                             |
| nbody          | 85.3 ms                                                                | 129 ms: 1.51x slower                                              |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.85 ms: 1.13x faster                                             |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                              |
| regex_v8       | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                             |
| regex_compile  | 131 ms                                                                 | 154 ms: 1.17x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.5 ms: 1.07x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 96.3 ms: 1.13x slower                                             |
| json_loads           | 27.3 us                                                                | 31.5 us: 1.15x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.33 sec: 1.16x slower                                            |
| xml_etree_process    | 59.2 ms                                                                | 69.6 ms: 1.18x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 245 us: 1.18x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 360 us: 1.23x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.76 ms: 1.32x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                             |
| genshi_text     | 21.7 ms                                                                | 27.8 ms: 1.28x slower                                             |
| django_template | 34.2 ms                                                                | 43.7 ms: 1.28x slower                                             |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.75 ms: 1.90x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 554 ms: 1.63x faster                                              |
| async_tree_io              | 881 ms                                                                 | 586 ms: 1.50x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 341 ms: 1.35x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 493 ms: 1.28x faster                                              |
| async_tree_none            | 353 ms                                                                 | 278 ms: 1.27x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 530 ms: 1.26x faster                                              |
| deepcopy                   | 357 us                                                                 | 309 us: 1.16x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.85 ms: 1.13x faster                                             |
| sqlite_synth               | 2.25 us                                                                | 2.05 us: 1.10x faster                                             |
| pidigits                   | 216 ms                                                                 | 199 ms: 1.09x faster                                              |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.5 ms: 1.07x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                              |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                              |
| go                         | 141 ms                                                                 | 137 ms: 1.02x faster                                              |
| scimark_sor                | 134 ms                                                                 | 131 ms: 1.02x faster                                              |
| float                      | 76.7 ms                                                                | 75.7 ms: 1.01x faster                                             |
| deepcopy_memo              | 38.1 us                                                                | 37.6 us: 1.01x faster                                             |
| async_generators           | 375 ms                                                                 | 371 ms: 1.01x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                             |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                              |
| regex_v8                   | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                             |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                             |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                              |
| deepcopy_reduce            | 3.12 us                                                                | 3.20 us: 1.02x slower                                             |
| docutils                   | 2.63 sec                                                               | 2.73 sec: 1.04x slower                                            |
| create_gc_cycles           | 1.33 ms                                                                | 1.39 ms: 1.04x slower                                             |
| html5lib                   | 68.6 ms                                                                | 72.2 ms: 1.05x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.72 sec: 1.06x slower                                            |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.07x slower                                            |
| json                       | 4.98 ms                                                                | 5.35 ms: 1.07x slower                                             |
| pyflate                    | 449 ms                                                                 | 490 ms: 1.09x slower                                              |
| generators                 | 28.5 ms                                                                | 31.3 ms: 1.10x slower                                             |
| logging_silent             | 98.2 ns                                                                | 108 ns: 1.10x slower                                              |
| dulwich_log                | 74.5 ms                                                                | 82.6 ms: 1.11x slower                                             |
| scimark_fft                | 348 ms                                                                 | 390 ms: 1.12x slower                                              |
| telco                      | 7.77 ms                                                                | 8.75 ms: 1.13x slower                                             |
| xml_etree_generate         | 85.4 ms                                                                | 96.3 ms: 1.13x slower                                             |
| json_loads                 | 27.3 us                                                                | 31.5 us: 1.15x slower                                             |
| sqlglot_normalize          | 106 ms                                                                 | 122 ms: 1.15x slower                                              |
| pprint_safe_repr           | 719 ms                                                                 | 829 ms: 1.15x slower                                              |
| thrift                     | 772 us                                                                 | 895 us: 1.16x slower                                              |
| tomli_loads                | 2.01 sec                                                               | 2.33 sec: 1.16x slower                                            |
| 2to3                       | 259 ms                                                                 | 303 ms: 1.17x slower                                              |
| regex_compile              | 131 ms                                                                 | 154 ms: 1.17x slower                                              |
| sqlglot_optimize           | 52.7 ms                                                                | 61.9 ms: 1.18x slower                                             |
| xml_etree_process          | 59.2 ms                                                                | 69.6 ms: 1.18x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 245 us: 1.18x slower                                              |
| pprint_pformat             | 1.46 sec                                                               | 1.72 sec: 1.18x slower                                            |
| coverage                   | 82.5 ms                                                                | 98.5 ms: 1.19x slower                                             |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.19x slower                                             |
| mdp                        | 2.34 sec                                                               | 2.80 sec: 1.19x slower                                            |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.20x slower                                             |
| logging_simple             | 6.14 us                                                                | 7.37 us: 1.20x slower                                             |
| logging_format             | 6.92 us                                                                | 8.30 us: 1.20x slower                                             |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.71 ms: 1.20x slower                                             |
| sympy_expand               | 454 ms                                                                 | 547 ms: 1.21x slower                                              |
| genshi_xml                 | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                              |
| hexiom                     | 5.95 ms                                                                | 7.24 ms: 1.22x slower                                             |
| sympy_integrate            | 19.7 ms                                                                | 24.0 ms: 1.22x slower                                             |
| richards                   | 44.4 ms                                                                | 54.1 ms: 1.22x slower                                             |
| nqueens                    | 77.7 ms                                                                | 94.8 ms: 1.22x slower                                             |
| sympy_str                  | 274 ms                                                                 | 336 ms: 1.22x slower                                              |
| deltablue                  | 3.10 ms                                                                | 3.80 ms: 1.23x slower                                             |
| meteor_contest             | 101 ms                                                                 | 125 ms: 1.23x slower                                              |
| pickle_pure_python         | 292 us                                                                 | 360 us: 1.23x slower                                              |
| scimark_lu                 | 112 ms                                                                 | 140 ms: 1.24x slower                                              |
| richards_super             | 50.4 ms                                                                | 63.0 ms: 1.25x slower                                             |
| chaos                      | 56.3 ms                                                                | 70.4 ms: 1.25x slower                                             |
| sqlglot_transpile          | 1.55 ms                                                                | 1.95 ms: 1.25x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 196 us: 1.26x slower                                              |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.3 ms: 1.27x slower                                             |
| genshi_text                | 21.7 ms                                                                | 27.8 ms: 1.28x slower                                             |
| django_template            | 34.2 ms                                                                | 43.7 ms: 1.28x slower                                             |
| fannkuch                   | 376 ms                                                                 | 483 ms: 1.29x slower                                              |
| raytrace                   | 250 ms                                                                 | 323 ms: 1.29x slower                                              |
| crypto_pyaes               | 68.2 ms                                                                | 88.6 ms: 1.30x slower                                             |
| sqlglot_parse              | 1.25 ms                                                                | 1.63 ms: 1.31x slower                                             |
| python_startup_no_site     | 7.41 ms                                                                | 9.76 ms: 1.32x slower                                             |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                             |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                             |
| nbody                      | 85.3 ms                                                                | 129 ms: 1.51x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.34 ms: 3.61x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 96.0 ms: 8.73x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                      |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250219-3.14.0a5+-32a747e-NOGIL/bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.075x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.36x