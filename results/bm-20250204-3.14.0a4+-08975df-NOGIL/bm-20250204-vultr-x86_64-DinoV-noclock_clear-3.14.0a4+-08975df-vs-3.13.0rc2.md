# Results vs. 3.13.0rc2

- fork: DinoV
- ref: noclock_clear
- machine: linux-x86_64
- commit hash: 08975df
- commit date: 2025-02-04
- overall geometric mean: 1.079x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 303 ms: 1.17x slower                                           |
| docutils       | 2.62 sec                                                     | 2.78 sec: 1.06x slower                                         |
| html5lib       | 67.0 ms                                                      | 69.0 ms: 1.03x slower                                          |
| Geometric mean | (ref)                                                        | 1.09x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 577 ms: 1.58x faster                                           |
| async_tree_io              | 876 ms                                                       | 608 ms: 1.44x faster                                           |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                           |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.31x faster                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 499 ms: 1.28x faster                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 531 ms: 1.25x faster                                           |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                           |
| async_generators           | 377 ms                                                       | 373 ms: 1.01x faster                                           |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                           |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                   |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                           |
| float          | 77.5 ms                                                      | 76.7 ms: 1.01x faster                                          |
| nbody          | 85.1 ms                                                      | 132 ms: 1.56x slower                                           |
| Geometric mean | (ref)                                                        | 1.11x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                          |
| regex_dna      | 180 ms                                                       | 185 ms: 1.02x slower                                           |
| regex_v8       | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                          |
| regex_compile  | 132 ms                                                       | 148 ms: 1.12x slower                                           |
| Geometric mean | (ref)                                                        | 1.02x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.9 ms: 1.08x faster                                          |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                           |
| xml_etree_generate   | 85.4 ms                                                      | 96.5 ms: 1.13x slower                                          |
| tomli_loads          | 2.01 sec                                                     | 2.30 sec: 1.15x slower                                         |
| xml_etree_process    | 59.3 ms                                                      | 68.9 ms: 1.16x slower                                          |
| json_loads           | 27.0 us                                                      | 31.6 us: 1.17x slower                                          |
| unpickle_pure_python | 210 us                                                       | 246 us: 1.17x slower                                           |
| json_dumps           | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                          |
| pickle_pure_python   | 294 us                                                       | 369 us: 1.25x slower                                           |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.62 ms: 1.30x slower                                          |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.40x slower                                          |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.0 ms: 1.23x slower                                          |
| django_template | 34.1 ms                                                      | 42.6 ms: 1.25x slower                                          |
| genshi_text     | 21.5 ms                                                      | 27.5 ms: 1.28x slower                                          |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                          |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.76 ms: 1.78x faster                                          |
| async_tree_io_tg           | 913 ms                                                       | 577 ms: 1.58x faster                                           |
| async_tree_io              | 876 ms                                                       | 608 ms: 1.44x faster                                           |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                           |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.31x faster                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 318 ms: 1.30x faster                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 499 ms: 1.28x faster                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 531 ms: 1.25x faster                                           |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                           |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                           |
| regex_effbot               | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                          |
| deepcopy                   | 355 us                                                       | 328 us: 1.08x faster                                           |
| sqlite_synth               | 2.21 us                                                      | 2.04 us: 1.08x faster                                          |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.9 ms: 1.08x faster                                          |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                           |
| spectral_norm              | 111 ms                                                       | 106 ms: 1.05x faster                                           |
| scimark_sor                | 134 ms                                                       | 130 ms: 1.04x faster                                           |
| deepcopy_memo              | 39.1 us                                                      | 37.8 us: 1.03x faster                                          |
| go                         | 141 ms                                                       | 136 ms: 1.03x faster                                           |
| pathlib                    | 19.2 ms                                                      | 18.9 ms: 1.01x faster                                          |
| async_generators           | 377 ms                                                       | 373 ms: 1.01x faster                                           |
| float                      | 77.5 ms                                                      | 76.7 ms: 1.01x faster                                          |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                           |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.02x slower                                           |
| regex_v8                   | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                          |
| html5lib                   | 67.0 ms                                                      | 69.0 ms: 1.03x slower                                          |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                         |
| bpe_tokeniser              | 4.45 sec                                                     | 4.68 sec: 1.05x slower                                         |
| scimark_fft                | 349 ms                                                       | 371 ms: 1.06x slower                                           |
| docutils                   | 2.62 sec                                                     | 2.78 sec: 1.06x slower                                         |
| pyflate                    | 449 ms                                                       | 491 ms: 1.09x slower                                           |
| telco                      | 7.82 ms                                                      | 8.56 ms: 1.09x slower                                          |
| pprint_safe_repr           | 738 ms                                                       | 808 ms: 1.10x slower                                           |
| logging_silent             | 103 ns                                                       | 112 ns: 1.10x slower                                           |
| deepcopy_reduce            | 3.11 us                                                      | 3.42 us: 1.10x slower                                          |
| json                       | 4.93 ms                                                      | 5.45 ms: 1.11x slower                                          |
| dulwich_log                | 74.8 ms                                                      | 82.8 ms: 1.11x slower                                          |
| mdp                        | 2.36 sec                                                     | 2.63 sec: 1.12x slower                                         |
| regex_compile              | 132 ms                                                       | 148 ms: 1.12x slower                                           |
| pprint_pformat             | 1.50 sec                                                     | 1.68 sec: 1.12x slower                                         |
| xml_etree_generate         | 85.4 ms                                                      | 96.5 ms: 1.13x slower                                          |
| sqlglot_normalize          | 106 ms                                                       | 120 ms: 1.14x slower                                           |
| tomli_loads                | 2.01 sec                                                     | 2.30 sec: 1.15x slower                                         |
| thrift                     | 778 us                                                       | 896 us: 1.15x slower                                           |
| generators                 | 28.8 ms                                                      | 33.2 ms: 1.15x slower                                          |
| sqlglot_optimize           | 52.7 ms                                                      | 60.9 ms: 1.15x slower                                          |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.45 ms: 1.16x slower                                          |
| xml_etree_process          | 59.3 ms                                                      | 68.9 ms: 1.16x slower                                          |
| 2to3                       | 260 ms                                                       | 303 ms: 1.17x slower                                           |
| json_loads                 | 27.0 us                                                      | 31.6 us: 1.17x slower                                          |
| unpickle_pure_python       | 210 us                                                       | 246 us: 1.17x slower                                           |
| chaos                      | 57.3 ms                                                      | 68.1 ms: 1.19x slower                                          |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.19x slower                                           |
| scimark_lu                 | 113 ms                                                       | 135 ms: 1.20x slower                                           |
| coverage                   | 83.0 ms                                                      | 99.3 ms: 1.20x slower                                          |
| json_dumps                 | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                          |
| sympy_integrate            | 19.8 ms                                                      | 24.1 ms: 1.21x slower                                          |
| sympy_expand               | 457 ms                                                       | 556 ms: 1.22x slower                                           |
| nqueens                    | 78.6 ms                                                      | 96.2 ms: 1.22x slower                                          |
| comprehensions             | 16.5 us                                                      | 20.2 us: 1.23x slower                                          |
| sympy_str                  | 275 ms                                                       | 337 ms: 1.23x slower                                           |
| sqlglot_transpile          | 1.56 ms                                                      | 1.92 ms: 1.23x slower                                          |
| genshi_xml                 | 48.8 ms                                                      | 60.0 ms: 1.23x slower                                          |
| scimark_monte_carlo        | 65.4 ms                                                      | 80.5 ms: 1.23x slower                                          |
| hexiom                     | 5.99 ms                                                      | 7.43 ms: 1.24x slower                                          |
| richards                   | 45.2 ms                                                      | 56.4 ms: 1.25x slower                                          |
| django_template            | 34.1 ms                                                      | 42.6 ms: 1.25x slower                                          |
| pickle_pure_python         | 294 us                                                       | 369 us: 1.25x slower                                           |
| raytrace                   | 253 ms                                                       | 318 ms: 1.26x slower                                           |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                           |
| sqlglot_parse              | 1.25 ms                                                      | 1.59 ms: 1.27x slower                                          |
| genshi_text                | 21.5 ms                                                      | 27.5 ms: 1.28x slower                                          |
| richards_super             | 51.6 ms                                                      | 66.3 ms: 1.28x slower                                          |
| logging_simple             | 6.16 us                                                      | 7.96 us: 1.29x slower                                          |
| crypto_pyaes               | 67.9 ms                                                      | 87.9 ms: 1.30x slower                                          |
| python_startup_no_site     | 7.39 ms                                                      | 9.62 ms: 1.30x slower                                          |
| typing_runtime_protocols   | 155 us                                                       | 201 us: 1.30x slower                                           |
| fannkuch                   | 370 ms                                                       | 490 ms: 1.32x slower                                           |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.40x slower                                          |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                          |
| deltablue                  | 3.12 ms                                                      | 4.65 ms: 1.49x slower                                          |
| logging_format             | 6.84 us                                                      | 10.3 us: 1.50x slower                                          |
| nbody                      | 85.1 ms                                                      | 132 ms: 1.56x slower                                           |
| bench_thread_pool          | 919 us                                                       | 3.29 ms: 3.58x slower                                          |
| bench_mp_pool              | 11.0 ms                                                      | 94.6 ms: 8.60x slower                                          |
| Geometric mean             | (ref)                                                        | 1.13x slower                                                   |

Benchmark hidden because not significant (3): pylint, coroutines, create_gc_cycles
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250204-3.14.0a4+-08975df-NOGIL/bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.079x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.43x