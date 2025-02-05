# Results vs. 3.13.0rc2

- fork: DinoV
- ref: noclock_clear
- machine: linux-x86_64
- commit hash: 08975df
- commit date: 2025-02-04
- overall geometric mean: 1.088x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 304 ms: 1.17x slower                                           |
| docutils       | 2.62 sec                                                     | 2.83 sec: 1.08x slower                                         |
| html5lib       | 67.0 ms                                                      | 71.3 ms: 1.06x slower                                          |
| Geometric mean | (ref)                                                        | 1.10x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 578 ms: 1.58x faster                                           |
| async_tree_io              | 876 ms                                                       | 608 ms: 1.44x faster                                           |
| async_tree_none_tg         | 336 ms                                                       | 251 ms: 1.34x faster                                           |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 320 ms: 1.29x faster                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 514 ms: 1.24x faster                                           |
| async_tree_none            | 354 ms                                                       | 289 ms: 1.23x faster                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 545 ms: 1.22x faster                                           |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                           |
| async_generators           | 377 ms                                                       | 374 ms: 1.01x faster                                           |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                          |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                           |
| float          | 77.5 ms                                                      | 77.1 ms: 1.00x faster                                          |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                           |
| Geometric mean | (ref)                                                        | 1.10x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.90 ms: 1.06x faster                                          |
| regex_v8       | 22.7 ms                                                      | 24.4 ms: 1.07x slower                                          |
| regex_compile  | 132 ms                                                       | 150 ms: 1.14x slower                                           |
| Geometric mean | (ref)                                                        | 1.03x slower                                                   |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                          |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                           |
| xml_etree_generate   | 85.4 ms                                                      | 98.2 ms: 1.15x slower                                          |
| tomli_loads          | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                         |
| json_loads           | 27.0 us                                                      | 31.7 us: 1.17x slower                                          |
| xml_etree_process    | 59.3 ms                                                      | 70.3 ms: 1.19x slower                                          |
| unpickle_pure_python | 210 us                                                       | 251 us: 1.19x slower                                           |
| json_dumps           | 10.5 ms                                                      | 12.7 ms: 1.21x slower                                          |
| pickle_pure_python   | 294 us                                                       | 379 us: 1.29x slower                                           |
| Geometric mean       | (ref)                                                        | 1.13x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.62 ms: 1.30x slower                                          |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                          |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.6 ms: 1.22x slower                                          |
| django_template | 34.1 ms                                                      | 42.8 ms: 1.25x slower                                          |
| genshi_text     | 21.5 ms                                                      | 27.8 ms: 1.29x slower                                          |
| mako            | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                          |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.65 ms: 1.90x faster                                          |
| async_tree_io_tg           | 913 ms                                                       | 578 ms: 1.58x faster                                           |
| async_tree_io              | 876 ms                                                       | 608 ms: 1.44x faster                                           |
| async_tree_none_tg         | 336 ms                                                       | 251 ms: 1.34x faster                                           |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 320 ms: 1.29x faster                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 514 ms: 1.24x faster                                           |
| async_tree_none            | 354 ms                                                       | 289 ms: 1.23x faster                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 545 ms: 1.22x faster                                           |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                           |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                          |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                          |
| deepcopy                   | 355 us                                                       | 333 us: 1.07x faster                                           |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                           |
| regex_effbot               | 3.08 ms                                                      | 2.90 ms: 1.06x faster                                          |
| deepcopy_memo              | 39.1 us                                                      | 38.5 us: 1.01x faster                                          |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                           |
| async_generators           | 377 ms                                                       | 374 ms: 1.01x faster                                           |
| scimark_sor                | 134 ms                                                       | 133 ms: 1.01x faster                                           |
| go                         | 141 ms                                                       | 140 ms: 1.01x faster                                           |
| pathlib                    | 19.2 ms                                                      | 19.0 ms: 1.01x faster                                          |
| create_gc_cycles           | 1.34 ms                                                      | 1.33 ms: 1.01x faster                                          |
| float                      | 77.5 ms                                                      | 77.1 ms: 1.00x faster                                          |
| spectral_norm              | 111 ms                                                       | 112 ms: 1.01x slower                                           |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                          |
| bpe_tokeniser              | 4.45 sec                                                     | 4.66 sec: 1.05x slower                                         |
| html5lib                   | 67.0 ms                                                      | 71.3 ms: 1.06x slower                                          |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.07x slower                                         |
| regex_v8                   | 22.7 ms                                                      | 24.4 ms: 1.07x slower                                          |
| docutils                   | 2.62 sec                                                     | 2.83 sec: 1.08x slower                                         |
| telco                      | 7.82 ms                                                      | 8.58 ms: 1.10x slower                                          |
| scimark_fft                | 349 ms                                                       | 384 ms: 1.10x slower                                           |
| json                       | 4.93 ms                                                      | 5.41 ms: 1.10x slower                                          |
| dulwich_log                | 74.8 ms                                                      | 82.5 ms: 1.10x slower                                          |
| pprint_safe_repr           | 738 ms                                                       | 818 ms: 1.11x slower                                           |
| deepcopy_reduce            | 3.11 us                                                      | 3.46 us: 1.11x slower                                          |
| pyflate                    | 449 ms                                                       | 502 ms: 1.12x slower                                           |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.13x slower                                         |
| logging_silent             | 103 ns                                                       | 116 ns: 1.13x slower                                           |
| regex_compile              | 132 ms                                                       | 150 ms: 1.14x slower                                           |
| sqlglot_normalize          | 106 ms                                                       | 120 ms: 1.14x slower                                           |
| xml_etree_generate         | 85.4 ms                                                      | 98.2 ms: 1.15x slower                                          |
| mdp                        | 2.36 sec                                                     | 2.71 sec: 1.15x slower                                         |
| thrift                     | 778 us                                                       | 903 us: 1.16x slower                                           |
| sqlglot_optimize           | 52.7 ms                                                      | 61.2 ms: 1.16x slower                                          |
| tomli_loads                | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                         |
| 2to3                       | 260 ms                                                       | 304 ms: 1.17x slower                                           |
| generators                 | 28.8 ms                                                      | 33.7 ms: 1.17x slower                                          |
| json_loads                 | 27.0 us                                                      | 31.7 us: 1.17x slower                                          |
| coverage                   | 83.0 ms                                                      | 97.7 ms: 1.18x slower                                          |
| xml_etree_process          | 59.3 ms                                                      | 70.3 ms: 1.19x slower                                          |
| unpickle_pure_python       | 210 us                                                       | 251 us: 1.19x slower                                           |
| chaos                      | 57.3 ms                                                      | 68.5 ms: 1.20x slower                                          |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.20x slower                                           |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.65 ms: 1.20x slower                                          |
| json_dumps                 | 10.5 ms                                                      | 12.7 ms: 1.21x slower                                          |
| sympy_expand               | 457 ms                                                       | 553 ms: 1.21x slower                                           |
| comprehensions             | 16.5 us                                                      | 20.0 us: 1.21x slower                                          |
| genshi_xml                 | 48.8 ms                                                      | 59.6 ms: 1.22x slower                                          |
| sympy_integrate            | 19.8 ms                                                      | 24.2 ms: 1.22x slower                                          |
| sqlglot_transpile          | 1.56 ms                                                      | 1.91 ms: 1.23x slower                                          |
| scimark_lu                 | 113 ms                                                       | 138 ms: 1.23x slower                                           |
| nqueens                    | 78.6 ms                                                      | 96.6 ms: 1.23x slower                                          |
| sympy_str                  | 275 ms                                                       | 338 ms: 1.23x slower                                           |
| django_template            | 34.1 ms                                                      | 42.8 ms: 1.25x slower                                          |
| hexiom                     | 5.99 ms                                                      | 7.54 ms: 1.26x slower                                          |
| sqlglot_parse              | 1.25 ms                                                      | 1.59 ms: 1.27x slower                                          |
| scimark_monte_carlo        | 65.4 ms                                                      | 83.1 ms: 1.27x slower                                          |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                           |
| richards                   | 45.2 ms                                                      | 57.9 ms: 1.28x slower                                          |
| pickle_pure_python         | 294 us                                                       | 379 us: 1.29x slower                                           |
| genshi_text                | 21.5 ms                                                      | 27.8 ms: 1.29x slower                                          |
| crypto_pyaes               | 67.9 ms                                                      | 88.0 ms: 1.30x slower                                          |
| raytrace                   | 253 ms                                                       | 329 ms: 1.30x slower                                           |
| python_startup_no_site     | 7.39 ms                                                      | 9.62 ms: 1.30x slower                                          |
| richards_super             | 51.6 ms                                                      | 67.5 ms: 1.31x slower                                          |
| typing_runtime_protocols   | 155 us                                                       | 203 us: 1.31x slower                                           |
| fannkuch                   | 370 ms                                                       | 489 ms: 1.32x slower                                           |
| logging_simple             | 6.16 us                                                      | 8.23 us: 1.34x slower                                          |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                          |
| mako                       | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                          |
| logging_format             | 6.84 us                                                      | 10.3 us: 1.51x slower                                          |
| deltablue                  | 3.12 ms                                                      | 4.74 ms: 1.52x slower                                          |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                           |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.62x slower                                          |
| bench_mp_pool              | 11.0 ms                                                      | 94.5 ms: 8.60x slower                                          |
| Geometric mean             | (ref)                                                        | 1.14x slower                                                   |

Benchmark hidden because not significant (2): pylint, regex_dna
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250204-3.14.0a4+-08975df-NOGIL/bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.088x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.43x