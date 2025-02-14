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
| 2to3           | 305 ms                                                                 | 298 ms: 1.02x faster                                              |
| docutils       | 2.83 sec                                                               | 2.75 sec: 1.03x faster                                            |
| html5lib       | 72.0 ms                                                                | 70.5 ms: 1.02x faster                                             |
| sphinx         | 1.11 sec                                                               | 1.09 sec: 1.02x faster                                            |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 555 ms                                                                 | 504 ms: 1.10x faster                                              |
| async_tree_cpu_io_mixed    | 588 ms                                                                 | 535 ms: 1.10x faster                                              |
| coroutines                 | 23.7 ms                                                                | 22.1 ms: 1.07x faster                                             |
| async_tree_none            | 290 ms                                                                 | 282 ms: 1.03x faster                                              |
| async_tree_memoization     | 355 ms                                                                 | 346 ms: 1.03x faster                                              |
| async_tree_none_tg         | 262 ms                                                                 | 256 ms: 1.03x faster                                              |
| async_tree_memoization_tg  | 321 ms                                                                 | 314 ms: 1.02x faster                                              |
| async_tree_io              | 611 ms                                                                 | 599 ms: 1.02x faster                                              |
| async_generators           | 375 ms                                                                 | 368 ms: 1.02x faster                                              |
| async_tree_io_tg           | 578 ms                                                                 | 572 ms: 1.01x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 132 ms                                                                 | 129 ms: 1.02x faster                                              |
| pidigits       | 216 ms                                                                 | 212 ms: 1.02x faster                                              |
| float          | 75.6 ms                                                                | 76.1 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 151 ms                                                                 | 145 ms: 1.04x faster                                              |
| regex_effbot   | 2.77 ms                                                                | 2.79 ms: 1.01x slower                                             |
| regex_dna      | 178 ms                                                                 | 180 ms: 1.01x slower                                              |
| regex_v8       | 23.8 ms                                                                | 24.3 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_pure_python | 253 us                                                                 | 239 us: 1.06x faster                                              |
| pickle_pure_python   | 365 us                                                                 | 348 us: 1.05x faster                                              |
| tomli_loads          | 2.37 sec                                                               | 2.27 sec: 1.04x faster                                            |
| xml_etree_process    | 70.5 ms                                                                | 68.6 ms: 1.03x faster                                             |
| xml_etree_generate   | 96.9 ms                                                                | 94.5 ms: 1.03x faster                                             |
| json_dumps           | 13.0 ms                                                                | 12.7 ms: 1.02x faster                                             |
| xml_etree_iterparse  | 88.1 ms                                                                | 87.4 ms: 1.01x faster                                             |
| json_loads           | 31.3 us                                                                | 31.6 us: 1.01x slower                                             |
| xml_etree_parse      | 127 ms                                                                 | 128 ms: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                             |
| python_startup_no_site | 9.62 ms                                                                | 9.70 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text     | 28.0 ms                                                                | 26.7 ms: 1.05x faster                                             |
| django_template | 42.4 ms                                                                | 41.4 ms: 1.02x faster                                             |
| mako            | 15.8 ms                                                                | 15.6 ms: 1.01x faster                                             |
| genshi_xml      | 59.1 ms                                                                | 58.6 ms: 1.01x faster                                             |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-68b535b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 555 ms                                                                 | 504 ms: 1.10x faster                                              |
| async_tree_cpu_io_mixed    | 588 ms                                                                 | 535 ms: 1.10x faster                                              |
| spectral_norm              | 112 ms                                                                 | 102 ms: 1.09x faster                                              |
| generators                 | 32.5 ms                                                                | 30.2 ms: 1.07x faster                                             |
| coroutines                 | 23.7 ms                                                                | 22.1 ms: 1.07x faster                                             |
| scimark_sor                | 134 ms                                                                 | 125 ms: 1.07x faster                                              |
| unpickle_pure_python       | 253 us                                                                 | 239 us: 1.06x faster                                              |
| hexiom                     | 7.47 ms                                                                | 7.08 ms: 1.05x faster                                             |
| go                         | 141 ms                                                                 | 134 ms: 1.05x faster                                              |
| pickle_pure_python         | 365 us                                                                 | 348 us: 1.05x faster                                              |
| logging_simple             | 7.20 us                                                                | 6.87 us: 1.05x faster                                             |
| genshi_text                | 28.0 ms                                                                | 26.7 ms: 1.05x faster                                             |
| logging_format             | 8.22 us                                                                | 7.85 us: 1.05x faster                                             |
| tomli_loads                | 2.37 sec                                                               | 2.27 sec: 1.04x faster                                            |
| nqueens                    | 98.0 ms                                                                | 94.0 ms: 1.04x faster                                             |
| richards                   | 57.1 ms                                                                | 54.7 ms: 1.04x faster                                             |
| chaos                      | 70.3 ms                                                                | 67.6 ms: 1.04x faster                                             |
| regex_compile              | 151 ms                                                                 | 145 ms: 1.04x faster                                              |
| richards_super             | 65.8 ms                                                                | 63.3 ms: 1.04x faster                                             |
| fannkuch                   | 496 ms                                                                 | 477 ms: 1.04x faster                                              |
| deltablue                  | 3.94 ms                                                                | 3.80 ms: 1.04x faster                                             |
| raytrace                   | 330 ms                                                                 | 318 ms: 1.04x faster                                              |
| scimark_lu                 | 140 ms                                                                 | 135 ms: 1.03x faster                                              |
| pyflate                    | 511 ms                                                                 | 495 ms: 1.03x faster                                              |
| scimark_sparse_mat_mult    | 5.76 ms                                                                | 5.58 ms: 1.03x faster                                             |
| sqlglot_normalize          | 120 ms                                                                 | 117 ms: 1.03x faster                                              |
| docutils                   | 2.83 sec                                                               | 2.75 sec: 1.03x faster                                            |
| scimark_fft                | 391 ms                                                                 | 380 ms: 1.03x faster                                              |
| async_tree_none            | 290 ms                                                                 | 282 ms: 1.03x faster                                              |
| xml_etree_process          | 70.5 ms                                                                | 68.6 ms: 1.03x faster                                             |
| xml_etree_generate         | 96.9 ms                                                                | 94.5 ms: 1.03x faster                                             |
| many_optionals             | 1.19 ms                                                                | 1.16 ms: 1.03x faster                                             |
| async_tree_memoization     | 355 ms                                                                 | 346 ms: 1.03x faster                                              |
| subparsers                 | 25.6 ms                                                                | 25.0 ms: 1.03x faster                                             |
| async_tree_none_tg         | 262 ms                                                                 | 256 ms: 1.03x faster                                              |
| django_template            | 42.4 ms                                                                | 41.4 ms: 1.02x faster                                             |
| async_tree_memoization_tg  | 321 ms                                                                 | 314 ms: 1.02x faster                                              |
| logging_silent             | 115 ns                                                                 | 113 ns: 1.02x faster                                              |
| 2to3                       | 305 ms                                                                 | 298 ms: 1.02x faster                                              |
| meteor_contest             | 130 ms                                                                 | 127 ms: 1.02x faster                                              |
| nbody                      | 132 ms                                                                 | 129 ms: 1.02x faster                                              |
| sqlglot_optimize           | 61.3 ms                                                                | 59.9 ms: 1.02x faster                                             |
| async_tree_io              | 611 ms                                                                 | 599 ms: 1.02x faster                                              |
| telco                      | 8.62 ms                                                                | 8.44 ms: 1.02x faster                                             |
| pprint_pformat             | 1.71 sec                                                               | 1.68 sec: 1.02x faster                                            |
| html5lib                   | 72.0 ms                                                                | 70.5 ms: 1.02x faster                                             |
| json_dumps                 | 13.0 ms                                                                | 12.7 ms: 1.02x faster                                             |
| scimark_monte_carlo        | 83.7 ms                                                                | 82.1 ms: 1.02x faster                                             |
| async_generators           | 375 ms                                                                 | 368 ms: 1.02x faster                                              |
| crypto_pyaes               | 89.1 ms                                                                | 87.4 ms: 1.02x faster                                             |
| sqlglot_transpile          | 1.92 ms                                                                | 1.89 ms: 1.02x faster                                             |
| sphinx                     | 1.11 sec                                                               | 1.09 sec: 1.02x faster                                            |
| pidigits                   | 216 ms                                                                 | 212 ms: 1.02x faster                                              |
| shortest_path              | 548 ms                                                                 | 538 ms: 1.02x faster                                              |
| create_gc_cycles           | 1.39 ms                                                                | 1.37 ms: 1.02x faster                                             |
| sqlalchemy_declarative     | 157 ms                                                                 | 155 ms: 1.02x faster                                              |
| connected_components       | 494 ms                                                                 | 486 ms: 1.02x faster                                              |
| deepcopy                   | 310 us                                                                 | 305 us: 1.02x faster                                              |
| pycparser                  | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                            |
| pprint_safe_repr           | 827 ms                                                                 | 815 ms: 1.01x faster                                              |
| bpe_tokeniser              | 4.68 sec                                                               | 4.62 sec: 1.01x faster                                            |
| comprehensions             | 19.8 us                                                                | 19.5 us: 1.01x faster                                             |
| k_core                     | 2.32 sec                                                               | 2.29 sec: 1.01x faster                                            |
| gc_traversal               | 1.75 ms                                                                | 1.73 ms: 1.01x faster                                             |
| mako                       | 15.8 ms                                                                | 15.6 ms: 1.01x faster                                             |
| sympy_integrate            | 24.0 ms                                                                | 23.8 ms: 1.01x faster                                             |
| async_tree_io_tg           | 578 ms                                                                 | 572 ms: 1.01x faster                                              |
| typing_runtime_protocols   | 199 us                                                                 | 198 us: 1.01x faster                                              |
| sympy_sum                  | 185 ms                                                                 | 183 ms: 1.01x faster                                              |
| sympy_str                  | 333 ms                                                                 | 330 ms: 1.01x faster                                              |
| sqlglot_parse              | 1.59 ms                                                                | 1.58 ms: 1.01x faster                                             |
| genshi_xml                 | 59.1 ms                                                                | 58.6 ms: 1.01x faster                                             |
| dulwich_log                | 82.3 ms                                                                | 81.6 ms: 1.01x faster                                             |
| xml_etree_iterparse        | 88.1 ms                                                                | 87.4 ms: 1.01x faster                                             |
| deepcopy_memo              | 38.5 us                                                                | 38.3 us: 1.01x faster                                             |
| pathlib                    | 19.2 ms                                                                | 19.1 ms: 1.01x faster                                             |
| sympy_expand               | 543 ms                                                                 | 540 ms: 1.01x faster                                              |
| python_startup             | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                             |
| float                      | 75.6 ms                                                                | 76.1 ms: 1.01x slower                                             |
| json_loads                 | 31.3 us                                                                | 31.6 us: 1.01x slower                                             |
| python_startup_no_site     | 9.62 ms                                                                | 9.70 ms: 1.01x slower                                             |
| regex_effbot               | 2.77 ms                                                                | 2.79 ms: 1.01x slower                                             |
| mdp                        | 2.71 sec                                                               | 2.73 sec: 1.01x slower                                            |
| regex_dna                  | 178 ms                                                                 | 180 ms: 1.01x slower                                              |
| xml_etree_parse            | 127 ms                                                                 | 128 ms: 1.01x slower                                              |
| sqlite_synth               | 2.03 us                                                                | 2.06 us: 1.01x slower                                             |
| json                       | 5.35 ms                                                                | 5.43 ms: 1.02x slower                                             |
| coverage                   | 96.1 ms                                                                | 97.6 ms: 1.02x slower                                             |
| regex_v8                   | 23.8 ms                                                                | 24.3 ms: 1.02x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                      |

Benchmark hidden because not significant (7): pylint, sqlalchemy_imperative, asyncio_websockets, deepcopy_reduce, bench_thread_pool, bench_mp_pool, thrift

- Geometric mean (including insignificant results): 1.023x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x