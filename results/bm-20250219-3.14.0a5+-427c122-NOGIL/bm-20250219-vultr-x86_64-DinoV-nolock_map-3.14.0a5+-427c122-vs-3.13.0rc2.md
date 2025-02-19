# Results vs. 3.13.0rc2

- fork: DinoV
- ref: nolock_map
- machine: linux-x86_64
- commit hash: 427c122
- commit date: 2025-02-19
- overall geometric mean: 1.074x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 301 ms: 1.16x slower                                        |
| docutils       | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                      |
| html5lib       | 68.6 ms                                                                | 70.8 ms: 1.03x slower                                       |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 554 ms: 1.63x faster                                        |
| async_tree_io              | 881 ms                                                                 | 582 ms: 1.51x faster                                        |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                        |
| async_tree_memoization     | 459 ms                                                                 | 340 ms: 1.35x faster                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 309 ms: 1.33x faster                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 493 ms: 1.29x faster                                        |
| async_tree_none            | 353 ms                                                                 | 278 ms: 1.27x faster                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 528 ms: 1.26x faster                                        |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                        |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 200 ms: 1.08x faster                                        |
| float          | 76.7 ms                                                                | 75.7 ms: 1.01x faster                                       |
| nbody          | 85.3 ms                                                                | 131 ms: 1.54x slower                                        |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.80 ms: 1.15x faster                                       |
| regex_dna      | 189 ms                                                                 | 185 ms: 1.02x faster                                        |
| regex_compile  | 131 ms                                                                 | 154 ms: 1.17x slower                                        |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.4 ms: 1.08x faster                                       |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                        |
| xml_etree_generate   | 85.4 ms                                                                | 95.6 ms: 1.12x slower                                       |
| tomli_loads          | 2.01 sec                                                               | 2.31 sec: 1.15x slower                                      |
| json_loads           | 27.3 us                                                                | 31.6 us: 1.16x slower                                       |
| xml_etree_process    | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                       |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                        |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                       |
| pickle_pure_python   | 292 us                                                                 | 362 us: 1.24x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                       |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                       |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.0 ms: 1.20x slower                                       |
| django_template | 34.2 ms                                                                | 42.3 ms: 1.24x slower                                       |
| genshi_text     | 21.7 ms                                                                | 27.7 ms: 1.27x slower                                       |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.40x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.74 ms: 1.91x faster                                       |
| async_tree_io_tg           | 901 ms                                                                 | 554 ms: 1.63x faster                                        |
| async_tree_io              | 881 ms                                                                 | 582 ms: 1.51x faster                                        |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                        |
| async_tree_memoization     | 459 ms                                                                 | 340 ms: 1.35x faster                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 309 ms: 1.33x faster                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 493 ms: 1.29x faster                                        |
| async_tree_none            | 353 ms                                                                 | 278 ms: 1.27x faster                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 528 ms: 1.26x faster                                        |
| regex_effbot               | 3.21 ms                                                                | 2.80 ms: 1.15x faster                                       |
| deepcopy                   | 357 us                                                                 | 313 us: 1.14x faster                                        |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                       |
| pidigits                   | 216 ms                                                                 | 200 ms: 1.08x faster                                        |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.4 ms: 1.08x faster                                       |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                        |
| regex_dna                  | 189 ms                                                                 | 185 ms: 1.02x faster                                        |
| scimark_sor                | 134 ms                                                                 | 132 ms: 1.01x faster                                        |
| float                      | 76.7 ms                                                                | 75.7 ms: 1.01x faster                                       |
| go                         | 141 ms                                                                 | 139 ms: 1.01x faster                                        |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                        |
| deepcopy_memo              | 38.1 us                                                                | 38.4 us: 1.01x slower                                       |
| html5lib                   | 68.6 ms                                                                | 70.8 ms: 1.03x slower                                       |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.04x slower                                       |
| pathlib                    | 19.3 ms                                                                | 20.0 ms: 1.04x slower                                       |
| docutils                   | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                      |
| bpe_tokeniser              | 4.46 sec                                                               | 4.72 sec: 1.06x slower                                      |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                      |
| json                       | 4.98 ms                                                                | 5.34 ms: 1.07x slower                                       |
| pyflate                    | 449 ms                                                                 | 491 ms: 1.09x slower                                        |
| generators                 | 28.5 ms                                                                | 31.2 ms: 1.09x slower                                       |
| dulwich_log                | 74.5 ms                                                                | 83.1 ms: 1.12x slower                                       |
| scimark_fft                | 348 ms                                                                 | 390 ms: 1.12x slower                                        |
| xml_etree_generate         | 85.4 ms                                                                | 95.6 ms: 1.12x slower                                       |
| telco                      | 7.77 ms                                                                | 8.79 ms: 1.13x slower                                       |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.14x slower                                        |
| logging_simple             | 6.14 us                                                                | 7.02 us: 1.14x slower                                       |
| tomli_loads                | 2.01 sec                                                               | 2.31 sec: 1.15x slower                                      |
| pprint_safe_repr           | 719 ms                                                                 | 830 ms: 1.16x slower                                        |
| json_loads                 | 27.3 us                                                                | 31.6 us: 1.16x slower                                       |
| thrift                     | 772 us                                                                 | 892 us: 1.16x slower                                        |
| logging_silent             | 98.2 ns                                                                | 114 ns: 1.16x slower                                        |
| 2to3                       | 259 ms                                                                 | 301 ms: 1.16x slower                                        |
| sqlglot_optimize           | 52.7 ms                                                                | 61.3 ms: 1.16x slower                                       |
| logging_format             | 6.92 us                                                                | 8.06 us: 1.17x slower                                       |
| xml_etree_process          | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                       |
| regex_compile              | 131 ms                                                                 | 154 ms: 1.17x slower                                        |
| pprint_pformat             | 1.46 sec                                                               | 1.71 sec: 1.18x slower                                      |
| comprehensions             | 16.6 us                                                                | 19.5 us: 1.18x slower                                       |
| coverage                   | 82.5 ms                                                                | 97.9 ms: 1.19x slower                                       |
| mdp                        | 2.34 sec                                                               | 2.78 sec: 1.19x slower                                      |
| sympy_expand               | 454 ms                                                                 | 544 ms: 1.20x slower                                        |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                        |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                       |
| genshi_xml                 | 49.1 ms                                                                | 59.0 ms: 1.20x slower                                       |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.72 ms: 1.20x slower                                       |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.21x slower                                        |
| sympy_integrate            | 19.7 ms                                                                | 23.9 ms: 1.21x slower                                       |
| sympy_str                  | 274 ms                                                                 | 333 ms: 1.21x slower                                        |
| deltablue                  | 3.10 ms                                                                | 3.79 ms: 1.22x slower                                       |
| sqlglot_transpile          | 1.55 ms                                                                | 1.91 ms: 1.23x slower                                       |
| hexiom                     | 5.95 ms                                                                | 7.32 ms: 1.23x slower                                       |
| nqueens                    | 77.7 ms                                                                | 95.9 ms: 1.23x slower                                       |
| django_template            | 34.2 ms                                                                | 42.3 ms: 1.24x slower                                       |
| chaos                      | 56.3 ms                                                                | 69.9 ms: 1.24x slower                                       |
| pickle_pure_python         | 292 us                                                                 | 362 us: 1.24x slower                                        |
| richards                   | 44.4 ms                                                                | 55.2 ms: 1.24x slower                                       |
| scimark_lu                 | 112 ms                                                                 | 140 ms: 1.24x slower                                        |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.6 ms: 1.25x slower                                       |
| typing_runtime_protocols   | 156 us                                                                 | 197 us: 1.27x slower                                        |
| sqlglot_parse              | 1.25 ms                                                                | 1.58 ms: 1.27x slower                                       |
| genshi_text                | 21.7 ms                                                                | 27.7 ms: 1.27x slower                                       |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                        |
| crypto_pyaes               | 68.2 ms                                                                | 87.9 ms: 1.29x slower                                       |
| raytrace                   | 250 ms                                                                 | 322 ms: 1.29x slower                                        |
| python_startup_no_site     | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                       |
| fannkuch                   | 376 ms                                                                 | 488 ms: 1.30x slower                                        |
| richards_super             | 50.4 ms                                                                | 66.3 ms: 1.31x slower                                       |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.40x slower                                       |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                       |
| nbody                      | 85.3 ms                                                                | 131 ms: 1.54x slower                                        |
| bench_thread_pool          | 924 us                                                                 | 3.31 ms: 3.58x slower                                       |
| bench_mp_pool              | 11.0 ms                                                                | 95.4 ms: 8.68x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                |

Benchmark hidden because not significant (6): pylint, asyncio_websockets, deepcopy_reduce, coroutines, regex_v8, spectral_norm
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250219-3.14.0a5+-427c122-NOGIL/bm-20250219-vultr-x86_64-DinoV-nolock_map-3.14.0a5+-427c122.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.074x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x