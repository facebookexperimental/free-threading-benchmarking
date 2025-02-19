# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: d72f499
- commit date: 2025-02-18
- overall geometric mean: 1.009x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 302 ms                                                                 | 305 ms: 1.01x slower                                              |
| docutils       | 2.80 sec                                                               | 2.78 sec: 1.01x faster                                            |
| html5lib       | 72.1 ms                                                                | 72.5 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 547 ms                                                                 | 542 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 513 ms                                                                 | 511 ms: 1.00x faster                                              |
| async_generators           | 374 ms                                                                 | 373 ms: 1.00x faster                                              |
| async_tree_io              | 607 ms                                                                 | 610 ms: 1.01x slower                                              |
| coroutines                 | 23.8 ms                                                                | 23.9 ms: 1.01x slower                                             |
| async_tree_memoization     | 352 ms                                                                 | 356 ms: 1.01x slower                                              |
| async_tree_memoization_tg  | 319 ms                                                                 | 323 ms: 1.01x slower                                              |
| async_tree_io_tg           | 574 ms                                                                 | 582 ms: 1.01x slower                                              |
| async_tree_none            | 286 ms                                                                 | 290 ms: 1.01x slower                                              |
| async_tree_none_tg         | 248 ms                                                                 | 253 ms: 1.02x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 129 ms                                                                 | 131 ms: 1.01x slower                                              |
| pidigits       | 199 ms                                                                 | 203 ms: 1.02x slower                                              |
| float          | 75.8 ms                                                                | 77.4 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 23.6 ms                                                                | 23.2 ms: 1.02x faster                                             |
| regex_dna      | 183 ms                                                                 | 181 ms: 1.01x faster                                              |
| regex_compile  | 154 ms                                                                 | 155 ms: 1.01x slower                                              |
| regex_effbot   | 2.84 ms                                                                | 2.89 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_loads           | 31.2 us                                                                | 31.3 us: 1.00x slower                                             |
| json_dumps           | 12.9 ms                                                                | 12.9 ms: 1.00x slower                                             |
| xml_etree_generate   | 96.6 ms                                                                | 97.2 ms: 1.01x slower                                             |
| xml_etree_iterparse  | 88.0 ms                                                                | 88.9 ms: 1.01x slower                                             |
| unpickle_pure_python | 252 us                                                                 | 255 us: 1.01x slower                                              |
| pickle_pure_python   | 360 us                                                                 | 367 us: 1.02x slower                                              |
| tomli_loads          | 2.32 sec                                                               | 2.36 sec: 1.02x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                             |
| python_startup_no_site | 9.62 ms                                                                | 9.70 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text     | 28.1 ms                                                                | 27.8 ms: 1.01x faster                                             |
| genshi_xml      | 59.8 ms                                                                | 59.4 ms: 1.01x faster                                             |
| mako            | 15.7 ms                                                                | 15.7 ms: 1.00x slower                                             |
| django_template | 42.7 ms                                                                | 43.3 ms: 1.01x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5+-bcc9a5d | bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-d72f499 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8                   | 23.6 ms                                                                | 23.2 ms: 1.02x faster                                             |
| thrift                     | 893 us                                                                 | 881 us: 1.01x faster                                              |
| docutils                   | 2.80 sec                                                               | 2.78 sec: 1.01x faster                                            |
| async_tree_cpu_io_mixed    | 547 ms                                                                 | 542 ms: 1.01x faster                                              |
| genshi_text                | 28.1 ms                                                                | 27.8 ms: 1.01x faster                                             |
| regex_dna                  | 183 ms                                                                 | 181 ms: 1.01x faster                                              |
| genshi_xml                 | 59.8 ms                                                                | 59.4 ms: 1.01x faster                                             |
| generators                 | 32.3 ms                                                                | 32.1 ms: 1.01x faster                                             |
| async_tree_cpu_io_mixed_tg | 513 ms                                                                 | 511 ms: 1.00x faster                                              |
| fannkuch                   | 492 ms                                                                 | 490 ms: 1.00x faster                                              |
| async_generators           | 374 ms                                                                 | 373 ms: 1.00x faster                                              |
| json_loads                 | 31.2 us                                                                | 31.3 us: 1.00x slower                                             |
| comprehensions             | 19.9 us                                                                | 20.0 us: 1.00x slower                                             |
| json_dumps                 | 12.9 ms                                                                | 12.9 ms: 1.00x slower                                             |
| bench_thread_pool          | 3.30 ms                                                                | 3.31 ms: 1.00x slower                                             |
| mako                       | 15.7 ms                                                                | 15.7 ms: 1.00x slower                                             |
| sqlalchemy_declarative     | 157 ms                                                                 | 158 ms: 1.00x slower                                              |
| sqlglot_normalize          | 120 ms                                                                 | 121 ms: 1.01x slower                                              |
| bpe_tokeniser              | 4.68 sec                                                               | 4.71 sec: 1.01x slower                                            |
| deepcopy_memo              | 38.4 us                                                                | 38.6 us: 1.01x slower                                             |
| chaos                      | 70.0 ms                                                                | 70.4 ms: 1.01x slower                                             |
| async_tree_io              | 607 ms                                                                 | 610 ms: 1.01x slower                                              |
| coroutines                 | 23.8 ms                                                                | 23.9 ms: 1.01x slower                                             |
| xml_etree_generate         | 96.6 ms                                                                | 97.2 ms: 1.01x slower                                             |
| pyflate                    | 496 ms                                                                 | 499 ms: 1.01x slower                                              |
| html5lib                   | 72.1 ms                                                                | 72.5 ms: 1.01x slower                                             |
| pprint_safe_repr           | 825 ms                                                                 | 831 ms: 1.01x slower                                              |
| richards_super             | 64.3 ms                                                                | 64.8 ms: 1.01x slower                                             |
| python_startup             | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                             |
| bench_mp_pool              | 94.9 ms                                                                | 95.6 ms: 1.01x slower                                             |
| sqlglot_optimize           | 61.4 ms                                                                | 61.9 ms: 1.01x slower                                             |
| 2to3                       | 302 ms                                                                 | 305 ms: 1.01x slower                                              |
| python_startup_no_site     | 9.62 ms                                                                | 9.70 ms: 1.01x slower                                             |
| hexiom                     | 7.41 ms                                                                | 7.48 ms: 1.01x slower                                             |
| scimark_lu                 | 139 ms                                                                 | 141 ms: 1.01x slower                                              |
| xml_etree_iterparse        | 88.0 ms                                                                | 88.9 ms: 1.01x slower                                             |
| scimark_fft                | 386 ms                                                                 | 390 ms: 1.01x slower                                              |
| regex_compile              | 154 ms                                                                 | 155 ms: 1.01x slower                                              |
| async_tree_memoization     | 352 ms                                                                 | 356 ms: 1.01x slower                                              |
| unpickle_pure_python       | 252 us                                                                 | 255 us: 1.01x slower                                              |
| pprint_pformat             | 1.70 sec                                                               | 1.72 sec: 1.01x slower                                            |
| gc_traversal               | 1.73 ms                                                                | 1.75 ms: 1.01x slower                                             |
| async_tree_memoization_tg  | 319 ms                                                                 | 323 ms: 1.01x slower                                              |
| deepcopy_reduce            | 3.18 us                                                                | 3.22 us: 1.01x slower                                             |
| sympy_expand               | 546 ms                                                                 | 553 ms: 1.01x slower                                              |
| deepcopy                   | 310 us                                                                 | 314 us: 1.01x slower                                              |
| create_gc_cycles           | 1.37 ms                                                                | 1.39 ms: 1.01x slower                                             |
| nbody                      | 129 ms                                                                 | 131 ms: 1.01x slower                                              |
| coverage                   | 97.9 ms                                                                | 99.3 ms: 1.01x slower                                             |
| raytrace                   | 324 ms                                                                 | 328 ms: 1.01x slower                                              |
| many_optionals             | 1.18 ms                                                                | 1.19 ms: 1.01x slower                                             |
| scimark_sor                | 132 ms                                                                 | 134 ms: 1.01x slower                                              |
| subparsers                 | 25.4 ms                                                                | 25.8 ms: 1.01x slower                                             |
| async_tree_io_tg           | 574 ms                                                                 | 582 ms: 1.01x slower                                              |
| django_template            | 42.7 ms                                                                | 43.3 ms: 1.01x slower                                             |
| async_tree_none            | 286 ms                                                                 | 290 ms: 1.01x slower                                              |
| go                         | 140 ms                                                                 | 142 ms: 1.01x slower                                              |
| sympy_str                  | 334 ms                                                                 | 339 ms: 1.02x slower                                              |
| pidigits                   | 199 ms                                                                 | 203 ms: 1.02x slower                                              |
| pickle_pure_python         | 360 us                                                                 | 367 us: 1.02x slower                                              |
| nqueens                    | 96.3 ms                                                                | 98.0 ms: 1.02x slower                                             |
| tomli_loads                | 2.32 sec                                                               | 2.36 sec: 1.02x slower                                            |
| regex_effbot               | 2.84 ms                                                                | 2.89 ms: 1.02x slower                                             |
| logging_silent             | 114 ns                                                                 | 116 ns: 1.02x slower                                              |
| async_tree_none_tg         | 248 ms                                                                 | 253 ms: 1.02x slower                                              |
| float                      | 75.8 ms                                                                | 77.4 ms: 1.02x slower                                             |
| logging_simple             | 7.06 us                                                                | 7.21 us: 1.02x slower                                             |
| sympy_integrate            | 24.1 ms                                                                | 24.6 ms: 1.02x slower                                             |
| telco                      | 8.49 ms                                                                | 8.68 ms: 1.02x slower                                             |
| sqlalchemy_imperative      | 23.8 ms                                                                | 24.4 ms: 1.02x slower                                             |
| deltablue                  | 3.87 ms                                                                | 3.97 ms: 1.02x slower                                             |
| sqlglot_transpile          | 1.91 ms                                                                | 1.96 ms: 1.02x slower                                             |
| pylint                     | 313 ms                                                                 | 321 ms: 1.03x slower                                              |
| crypto_pyaes               | 87.2 ms                                                                | 89.4 ms: 1.03x slower                                             |
| sqlglot_parse              | 1.58 ms                                                                | 1.64 ms: 1.04x slower                                             |
| spectral_norm              | 109 ms                                                                 | 113 ms: 1.04x slower                                              |
| scimark_sparse_mat_mult    | 5.48 ms                                                                | 5.72 ms: 1.04x slower                                             |
| mdp                        | 2.61 sec                                                               | 2.77 sec: 1.06x slower                                            |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (18): shortest_path, pycparser, sphinx, scimark_monte_carlo, json, sqlite_synth, xml_etree_process, connected_components, richards, sympy_sum, k_core, xml_etree_parse, dulwich_log, asyncio_websockets, meteor_contest, pathlib, logging_format, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x