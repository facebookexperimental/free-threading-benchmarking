# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 68b535b
- commit date: 2025-02-13
- overall geometric mean: 1.023x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 297 ms: 1.03x faster                                              |
| docutils       | 2.81 sec                                                               | 2.74 sec: 1.02x faster                                            |
| html5lib       | 69.9 ms                                                                | 70.3 ms: 1.01x slower                                             |
| sphinx         | 1.11 sec                                                               | 1.09 sec: 1.01x faster                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| coroutines                 | 23.7 ms                                                                | 22.1 ms: 1.07x faster                                             |
| async_tree_none_tg         | 261 ms                                                                 | 254 ms: 1.03x faster                                              |
| async_tree_io_tg           | 581 ms                                                                 | 566 ms: 1.03x faster                                              |
| async_tree_memoization_tg  | 319 ms                                                                 | 311 ms: 1.03x faster                                              |
| async_tree_none            | 290 ms                                                                 | 283 ms: 1.02x faster                                              |
| async_tree_memoization     | 353 ms                                                                 | 346 ms: 1.02x faster                                              |
| async_tree_io              | 610 ms                                                                 | 598 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed    | 535 ms                                                                 | 526 ms: 1.02x faster                                              |
| async_generators           | 374 ms                                                                 | 368 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 494 ms: 1.01x faster                                              |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 135 ms                                                                 | 125 ms: 1.08x faster                                              |
| pidigits       | 203 ms                                                                 | 193 ms: 1.05x faster                                              |
| float          | 75.3 ms                                                                | 74.1 ms: 1.02x faster                                             |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 151 ms                                                                 | 145 ms: 1.04x faster                                              |
| regex_effbot   | 2.83 ms                                                                | 2.82 ms: 1.01x faster                                             |
| regex_dna      | 182 ms                                                                 | 181 ms: 1.00x faster                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_pure_python | 248 us                                                                 | 237 us: 1.05x faster                                              |
| tomli_loads          | 2.33 sec                                                               | 2.23 sec: 1.04x faster                                            |
| pickle_pure_python   | 360 us                                                                 | 347 us: 1.04x faster                                              |
| xml_etree_process    | 70.5 ms                                                                | 68.8 ms: 1.02x faster                                             |
| xml_etree_generate   | 97.0 ms                                                                | 94.9 ms: 1.02x faster                                             |
| json_dumps           | 13.0 ms                                                                | 12.8 ms: 1.02x faster                                             |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                      |

Benchmark hidden because not significant (2): json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.5 ms: 1.01x slower                                             |
| python_startup_no_site | 9.64 ms                                                                | 9.72 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 59.5 ms                                                                | 56.7 ms: 1.05x faster                                             |
| genshi_text     | 27.8 ms                                                                | 27.0 ms: 1.03x faster                                             |
| django_template | 42.5 ms                                                                | 41.3 ms: 1.03x faster                                             |
| mako            | 15.7 ms                                                                | 15.5 ms: 1.02x faster                                             |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody                      | 135 ms                                                                 | 125 ms: 1.08x faster                                              |
| pyflate                    | 511 ms                                                                 | 474 ms: 1.08x faster                                              |
| scimark_sparse_mat_mult    | 5.80 ms                                                                | 5.41 ms: 1.07x faster                                             |
| coroutines                 | 23.7 ms                                                                | 22.1 ms: 1.07x faster                                             |
| generators                 | 31.7 ms                                                                | 29.9 ms: 1.06x faster                                             |
| chaos                      | 70.0 ms                                                                | 66.3 ms: 1.06x faster                                             |
| scimark_sor                | 133 ms                                                                 | 127 ms: 1.05x faster                                              |
| go                         | 140 ms                                                                 | 134 ms: 1.05x faster                                              |
| genshi_xml                 | 59.5 ms                                                                | 56.7 ms: 1.05x faster                                             |
| pidigits                   | 203 ms                                                                 | 193 ms: 1.05x faster                                              |
| nqueens                    | 97.2 ms                                                                | 92.9 ms: 1.05x faster                                             |
| hexiom                     | 7.40 ms                                                                | 7.08 ms: 1.05x faster                                             |
| unpickle_pure_python       | 248 us                                                                 | 237 us: 1.05x faster                                              |
| deltablue                  | 3.96 ms                                                                | 3.79 ms: 1.04x faster                                             |
| tomli_loads                | 2.33 sec                                                               | 2.23 sec: 1.04x faster                                            |
| regex_compile              | 151 ms                                                                 | 145 ms: 1.04x faster                                              |
| scimark_fft                | 393 ms                                                                 | 376 ms: 1.04x faster                                              |
| richards                   | 57.5 ms                                                                | 55.1 ms: 1.04x faster                                             |
| deepcopy_reduce            | 3.21 us                                                                | 3.08 us: 1.04x faster                                             |
| deepcopy                   | 315 us                                                                 | 302 us: 1.04x faster                                              |
| spectral_norm              | 110 ms                                                                 | 106 ms: 1.04x faster                                              |
| deepcopy_memo              | 38.9 us                                                                | 37.4 us: 1.04x faster                                             |
| raytrace                   | 329 ms                                                                 | 316 ms: 1.04x faster                                              |
| logging_silent             | 115 ns                                                                 | 111 ns: 1.04x faster                                              |
| scimark_lu                 | 138 ms                                                                 | 133 ms: 1.04x faster                                              |
| pickle_pure_python         | 360 us                                                                 | 347 us: 1.04x faster                                              |
| richards_super             | 66.3 ms                                                                | 64.0 ms: 1.03x faster                                             |
| pprint_safe_repr           | 826 ms                                                                 | 798 ms: 1.03x faster                                              |
| mdp                        | 2.71 sec                                                               | 2.62 sec: 1.03x faster                                            |
| fannkuch                   | 492 ms                                                                 | 477 ms: 1.03x faster                                              |
| sqlglot_normalize          | 121 ms                                                                 | 117 ms: 1.03x faster                                              |
| genshi_text                | 27.8 ms                                                                | 27.0 ms: 1.03x faster                                             |
| logging_format             | 8.16 us                                                                | 7.92 us: 1.03x faster                                             |
| pprint_pformat             | 1.70 sec                                                               | 1.65 sec: 1.03x faster                                            |
| crypto_pyaes               | 89.2 ms                                                                | 86.7 ms: 1.03x faster                                             |
| django_template            | 42.5 ms                                                                | 41.3 ms: 1.03x faster                                             |
| async_tree_none_tg         | 261 ms                                                                 | 254 ms: 1.03x faster                                              |
| 2to3                       | 305 ms                                                                 | 297 ms: 1.03x faster                                              |
| async_tree_io_tg           | 581 ms                                                                 | 566 ms: 1.03x faster                                              |
| async_tree_memoization_tg  | 319 ms                                                                 | 311 ms: 1.03x faster                                              |
| connected_components       | 496 ms                                                                 | 484 ms: 1.03x faster                                              |
| pycparser                  | 1.19 sec                                                               | 1.16 sec: 1.03x faster                                            |
| scimark_monte_carlo        | 82.8 ms                                                                | 80.8 ms: 1.03x faster                                             |
| xml_etree_process          | 70.5 ms                                                                | 68.8 ms: 1.02x faster                                             |
| docutils                   | 2.81 sec                                                               | 2.74 sec: 1.02x faster                                            |
| async_tree_none            | 290 ms                                                                 | 283 ms: 1.02x faster                                              |
| logging_simple             | 7.18 us                                                                | 7.02 us: 1.02x faster                                             |
| dulwich_log                | 82.5 ms                                                                | 80.7 ms: 1.02x faster                                             |
| xml_etree_generate         | 97.0 ms                                                                | 94.9 ms: 1.02x faster                                             |
| sqlglot_optimize           | 61.3 ms                                                                | 60.1 ms: 1.02x faster                                             |
| async_tree_memoization     | 353 ms                                                                 | 346 ms: 1.02x faster                                              |
| json_dumps                 | 13.0 ms                                                                | 12.8 ms: 1.02x faster                                             |
| shortest_path              | 548 ms                                                                 | 537 ms: 1.02x faster                                              |
| async_tree_io              | 610 ms                                                                 | 598 ms: 1.02x faster                                              |
| comprehensions             | 19.9 us                                                                | 19.5 us: 1.02x faster                                             |
| float                      | 75.3 ms                                                                | 74.1 ms: 1.02x faster                                             |
| async_tree_cpu_io_mixed    | 535 ms                                                                 | 526 ms: 1.02x faster                                              |
| sqlalchemy_declarative     | 157 ms                                                                 | 154 ms: 1.02x faster                                              |
| async_generators           | 374 ms                                                                 | 368 ms: 1.02x faster                                              |
| mako                       | 15.7 ms                                                                | 15.5 ms: 1.02x faster                                             |
| sqlglot_transpile          | 1.91 ms                                                                | 1.89 ms: 1.01x faster                                             |
| bpe_tokeniser              | 4.66 sec                                                               | 4.60 sec: 1.01x faster                                            |
| k_core                     | 2.31 sec                                                               | 2.29 sec: 1.01x faster                                            |
| sphinx                     | 1.11 sec                                                               | 1.09 sec: 1.01x faster                                            |
| sympy_str                  | 334 ms                                                                 | 331 ms: 1.01x faster                                              |
| bench_thread_pool          | 3.33 ms                                                                | 3.30 ms: 1.01x faster                                             |
| pathlib                    | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                             |
| many_optionals             | 1.18 ms                                                                | 1.17 ms: 1.01x faster                                             |
| sympy_expand               | 545 ms                                                                 | 540 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 494 ms: 1.01x faster                                              |
| create_gc_cycles           | 1.41 ms                                                                | 1.40 ms: 1.01x faster                                             |
| thrift                     | 888 us                                                                 | 881 us: 1.01x faster                                              |
| subparsers                 | 25.5 ms                                                                | 25.4 ms: 1.01x faster                                             |
| regex_effbot               | 2.83 ms                                                                | 2.82 ms: 1.01x faster                                             |
| gc_traversal               | 1.76 ms                                                                | 1.75 ms: 1.01x faster                                             |
| sympy_sum                  | 184 ms                                                                 | 183 ms: 1.00x faster                                              |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                              |
| regex_dna                  | 182 ms                                                                 | 181 ms: 1.00x faster                                              |
| sympy_integrate            | 24.0 ms                                                                | 23.9 ms: 1.00x faster                                             |
| html5lib                   | 69.9 ms                                                                | 70.3 ms: 1.01x slower                                             |
| python_startup             | 15.3 ms                                                                | 15.5 ms: 1.01x slower                                             |
| json                       | 5.34 ms                                                                | 5.39 ms: 1.01x slower                                             |
| python_startup_no_site     | 9.64 ms                                                                | 9.72 ms: 1.01x slower                                             |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                              |
| coverage                   | 95.2 ms                                                                | 96.7 ms: 1.02x slower                                             |
| telco                      | 8.48 ms                                                                | 8.81 ms: 1.04x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                      |

Benchmark hidden because not significant (10): pylint, meteor_contest, sqlglot_parse, typing_runtime_protocols, regex_v8, bench_mp_pool, json_loads, sqlalchemy_imperative, xml_etree_iterparse, sqlite_synth

- Geometric mean (including insignificant results): 1.023x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x