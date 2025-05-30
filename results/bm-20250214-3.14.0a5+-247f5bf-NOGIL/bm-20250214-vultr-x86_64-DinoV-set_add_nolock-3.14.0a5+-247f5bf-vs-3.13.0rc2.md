# Results vs. 3.13.0rc2

- fork: DinoV
- ref: set_add_nolock
- machine: linux-x86_64
- commit hash: 247f5bf
- commit date: 2025-02-14
- overall geometric mean: 1.077x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 304 ms: 1.17x slower                                            |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                          |
| html5lib       | 68.6 ms                                                                | 71.3 ms: 1.04x slower                                           |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 580 ms: 1.55x faster                                            |
| async_tree_io              | 881 ms                                                                 | 607 ms: 1.45x faster                                            |
| async_tree_memoization     | 459 ms                                                                 | 351 ms: 1.31x faster                                            |
| async_tree_none_tg         | 333 ms                                                                 | 258 ms: 1.29x faster                                            |
| async_tree_memoization_tg  | 410 ms                                                                 | 319 ms: 1.28x faster                                            |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 505 ms: 1.26x faster                                            |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 538 ms: 1.24x faster                                            |
| async_tree_none            | 353 ms                                                                 | 286 ms: 1.23x faster                                            |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                            |
| Geometric mean             | (ref)                                                                  | 1.23x faster                                                    |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 213 ms: 1.02x faster                                            |
| float          | 76.7 ms                                                                | 76.0 ms: 1.01x faster                                           |
| nbody          | 85.3 ms                                                                | 129 ms: 1.51x slower                                            |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                           |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.03x faster                                            |
| regex_v8       | 23.2 ms                                                                | 24.1 ms: 1.04x slower                                           |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.16x slower                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                           |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                            |
| xml_etree_generate   | 85.4 ms                                                                | 95.8 ms: 1.12x slower                                           |
| json_loads           | 27.3 us                                                                | 31.5 us: 1.15x slower                                           |
| tomli_loads          | 2.01 sec                                                               | 2.34 sec: 1.16x slower                                          |
| xml_etree_process    | 59.2 ms                                                                | 69.7 ms: 1.18x slower                                           |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                            |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                           |
| pickle_pure_python   | 292 us                                                                 | 363 us: 1.24x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                           |
| python_startup         | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                           |
| Geometric mean         | (ref)                                                                  | 1.34x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                           |
| django_template | 34.2 ms                                                                | 42.2 ms: 1.23x slower                                           |
| genshi_text     | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                           |
| mako            | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                           |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.73 ms: 1.92x faster                                           |
| async_tree_io_tg           | 901 ms                                                                 | 580 ms: 1.55x faster                                            |
| async_tree_io              | 881 ms                                                                 | 607 ms: 1.45x faster                                            |
| async_tree_memoization     | 459 ms                                                                 | 351 ms: 1.31x faster                                            |
| async_tree_none_tg         | 333 ms                                                                 | 258 ms: 1.29x faster                                            |
| async_tree_memoization_tg  | 410 ms                                                                 | 319 ms: 1.28x faster                                            |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 505 ms: 1.26x faster                                            |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 538 ms: 1.24x faster                                            |
| async_tree_none            | 353 ms                                                                 | 286 ms: 1.23x faster                                            |
| regex_effbot               | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                           |
| deepcopy                   | 357 us                                                                 | 320 us: 1.12x faster                                            |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                           |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                           |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                            |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.03x faster                                            |
| scimark_sor                | 134 ms                                                                 | 131 ms: 1.02x faster                                            |
| pidigits                   | 216 ms                                                                 | 213 ms: 1.02x faster                                            |
| spectral_norm              | 108 ms                                                                 | 106 ms: 1.01x faster                                            |
| float                      | 76.7 ms                                                                | 76.0 ms: 1.01x faster                                           |
| go                         | 141 ms                                                                 | 139 ms: 1.01x faster                                            |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                            |
| deepcopy_memo              | 38.1 us                                                                | 37.9 us: 1.00x faster                                           |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.03x slower                                           |
| regex_v8                   | 23.2 ms                                                                | 24.1 ms: 1.04x slower                                           |
| html5lib                   | 68.6 ms                                                                | 71.3 ms: 1.04x slower                                           |
| deepcopy_reduce            | 3.12 us                                                                | 3.25 us: 1.04x slower                                           |
| bpe_tokeniser              | 4.46 sec                                                               | 4.68 sec: 1.05x slower                                          |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                          |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                          |
| json                       | 4.98 ms                                                                | 5.41 ms: 1.09x slower                                           |
| pyflate                    | 449 ms                                                                 | 489 ms: 1.09x slower                                            |
| telco                      | 7.77 ms                                                                | 8.48 ms: 1.09x slower                                           |
| scimark_fft                | 348 ms                                                                 | 385 ms: 1.11x slower                                            |
| dulwich_log                | 74.5 ms                                                                | 82.8 ms: 1.11x slower                                           |
| generators                 | 28.5 ms                                                                | 31.8 ms: 1.11x slower                                           |
| xml_etree_generate         | 85.4 ms                                                                | 95.8 ms: 1.12x slower                                           |
| logging_silent             | 98.2 ns                                                                | 111 ns: 1.13x slower                                            |
| pprint_safe_repr           | 719 ms                                                                 | 817 ms: 1.14x slower                                            |
| sqlglot_normalize          | 106 ms                                                                 | 121 ms: 1.14x slower                                            |
| json_loads                 | 27.3 us                                                                | 31.5 us: 1.15x slower                                           |
| coverage                   | 82.5 ms                                                                | 95.3 ms: 1.16x slower                                           |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.16x slower                                            |
| tomli_loads                | 2.01 sec                                                               | 2.34 sec: 1.16x slower                                          |
| sqlglot_optimize           | 52.7 ms                                                                | 61.3 ms: 1.16x slower                                           |
| pprint_pformat             | 1.46 sec                                                               | 1.70 sec: 1.17x slower                                          |
| thrift                     | 772 us                                                                 | 903 us: 1.17x slower                                            |
| 2to3                       | 259 ms                                                                 | 304 ms: 1.17x slower                                            |
| xml_etree_process          | 59.2 ms                                                                | 69.7 ms: 1.18x slower                                           |
| mdp                        | 2.34 sec                                                               | 2.77 sec: 1.18x slower                                          |
| logging_simple             | 6.14 us                                                                | 7.27 us: 1.18x slower                                           |
| comprehensions             | 16.6 us                                                                | 19.7 us: 1.19x slower                                           |
| logging_format             | 6.92 us                                                                | 8.24 us: 1.19x slower                                           |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                            |
| sympy_expand               | 454 ms                                                                 | 544 ms: 1.20x slower                                            |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                            |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                           |
| genshi_xml                 | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                           |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.73 ms: 1.21x slower                                           |
| scimark_lu                 | 112 ms                                                                 | 136 ms: 1.21x slower                                            |
| sympy_str                  | 274 ms                                                                 | 333 ms: 1.22x slower                                            |
| sympy_integrate            | 19.7 ms                                                                | 24.0 ms: 1.22x slower                                           |
| chaos                      | 56.3 ms                                                                | 69.2 ms: 1.23x slower                                           |
| nqueens                    | 77.7 ms                                                                | 95.9 ms: 1.23x slower                                           |
| django_template            | 34.2 ms                                                                | 42.2 ms: 1.23x slower                                           |
| sqlglot_transpile          | 1.55 ms                                                                | 1.92 ms: 1.24x slower                                           |
| hexiom                     | 5.95 ms                                                                | 7.37 ms: 1.24x slower                                           |
| pickle_pure_python         | 292 us                                                                 | 363 us: 1.24x slower                                            |
| deltablue                  | 3.10 ms                                                                | 3.87 ms: 1.25x slower                                           |
| richards                   | 44.4 ms                                                                | 56.1 ms: 1.26x slower                                           |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.2 ms: 1.26x slower                                           |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                            |
| sqlglot_parse              | 1.25 ms                                                                | 1.59 ms: 1.28x slower                                           |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.28x slower                                            |
| genshi_text                | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                           |
| richards_super             | 50.4 ms                                                                | 65.0 ms: 1.29x slower                                           |
| fannkuch                   | 376 ms                                                                 | 485 ms: 1.29x slower                                            |
| crypto_pyaes               | 68.2 ms                                                                | 88.2 ms: 1.29x slower                                           |
| python_startup_no_site     | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                           |
| raytrace                   | 250 ms                                                                 | 325 ms: 1.30x slower                                            |
| python_startup             | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                           |
| mako                       | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                           |
| nbody                      | 85.3 ms                                                                | 129 ms: 1.51x slower                                            |
| bench_thread_pool          | 924 us                                                                 | 3.33 ms: 3.60x slower                                           |
| bench_mp_pool              | 11.0 ms                                                                | 94.7 ms: 8.61x slower                                           |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                    |

Benchmark hidden because not significant (4): pathlib, asyncio_websockets, pylint, coroutines
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250214-3.14.0a5+-247f5bf-NOGIL/bm-20250214-vultr-x86_64-DinoV-set_add_nolock-3.14.0a5+-247f5bf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.077x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x