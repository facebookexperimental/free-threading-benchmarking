# Results vs. base

- fork: nascheme
- ref: mcache_str_hash
- machine: linux-x86_64
- commit hash: 8335fa1
- commit date: 2025-05-08
- overall geometric mean: 1.003x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 284 ms                                                                | 286 ms: 1.01x slower                                               |
| docutils       | 2.71 sec                                                              | 2.69 sec: 1.01x faster                                             |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                       |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 484 ms                                                                | 474 ms: 1.02x faster                                               |
| async_tree_cpu_io_mixed    | 510 ms                                                                | 502 ms: 1.02x faster                                               |
| coroutines                 | 23.5 ms                                                               | 23.4 ms: 1.00x faster                                              |
| async_generators           | 364 ms                                                                | 366 ms: 1.01x slower                                               |
| async_tree_memoization_tg  | 282 ms                                                                | 284 ms: 1.01x slower                                               |
| async_tree_memoization     | 310 ms                                                                | 313 ms: 1.01x slower                                               |
| Geometric mean             | (ref)                                                                 | 1.00x faster                                                       |

Benchmark hidden because not significant (5): async_tree_io_tg, async_tree_none, asyncio_websockets, async_tree_none_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 198 ms                                                                | 191 ms: 1.04x faster                                               |
| float          | 70.0 ms                                                               | 70.7 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                       |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 2.82 ms                                                               | 2.73 ms: 1.03x faster                                              |
| regex_dna      | 180 ms                                                                | 177 ms: 1.02x faster                                               |
| regex_v8       | 21.2 ms                                                               | 21.0 ms: 1.01x faster                                              |
| regex_compile  | 144 ms                                                                | 145 ms: 1.00x slower                                               |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| pickle_pure_python   | 339 us                                                                | 334 us: 1.02x faster                                               |
| xml_etree_parse      | 131 ms                                                                | 129 ms: 1.02x faster                                               |
| unpickle_pure_python | 234 us                                                                | 232 us: 1.01x faster                                               |
| tomli_loads          | 2.12 sec                                                              | 2.13 sec: 1.00x slower                                             |
| xml_etree_generate   | 96.1 ms                                                               | 96.6 ms: 1.01x slower                                              |
| json_dumps           | 13.2 ms                                                               | 13.4 ms: 1.01x slower                                              |
| xml_etree_process    | 68.6 ms                                                               | 69.8 ms: 1.02x slower                                              |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                       |

Benchmark hidden because not significant (2): json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| mako            | 16.0 ms                                                               | 15.7 ms: 1.02x faster                                              |
| genshi_xml      | 54.9 ms                                                               | 55.4 ms: 1.01x slower                                              |
| django_template | 40.5 ms                                                               | 40.9 ms: 1.01x slower                                              |
| genshi_text     | 26.2 ms                                                               | 26.5 ms: 1.01x slower                                              |
| Geometric mean  | (ref)                                                                 | 1.00x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits                   | 198 ms                                                                | 191 ms: 1.04x faster                                               |
| regex_effbot               | 2.82 ms                                                               | 2.73 ms: 1.03x faster                                              |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                | 474 ms: 1.02x faster                                               |
| regex_dna                  | 180 ms                                                                | 177 ms: 1.02x faster                                               |
| pickle_pure_python         | 339 us                                                                | 334 us: 1.02x faster                                               |
| logging_format             | 8.76 us                                                               | 8.62 us: 1.02x faster                                              |
| async_tree_cpu_io_mixed    | 510 ms                                                                | 502 ms: 1.02x faster                                               |
| create_gc_cycles           | 1.51 ms                                                               | 1.48 ms: 1.02x faster                                              |
| mako                       | 16.0 ms                                                               | 15.7 ms: 1.02x faster                                              |
| xml_etree_parse            | 131 ms                                                                | 129 ms: 1.02x faster                                               |
| gc_traversal               | 1.93 ms                                                               | 1.90 ms: 1.01x faster                                              |
| regex_v8                   | 21.2 ms                                                               | 21.0 ms: 1.01x faster                                              |
| deepcopy_memo              | 35.8 us                                                               | 35.4 us: 1.01x faster                                              |
| unpickle_pure_python       | 234 us                                                                | 232 us: 1.01x faster                                               |
| bench_mp_pool              | 104 ms                                                                | 103 ms: 1.01x faster                                               |
| docutils                   | 2.71 sec                                                              | 2.69 sec: 1.01x faster                                             |
| coroutines                 | 23.5 ms                                                               | 23.4 ms: 1.00x faster                                              |
| deepcopy                   | 293 us                                                                | 292 us: 1.00x faster                                               |
| sqlglot_v2_normalize       | 116 ms                                                                | 116 ms: 1.00x faster                                               |
| bpe_tokeniser              | 4.43 sec                                                              | 4.42 sec: 1.00x faster                                             |
| nqueens                    | 87.9 ms                                                               | 88.1 ms: 1.00x slower                                              |
| hexiom                     | 6.66 ms                                                               | 6.68 ms: 1.00x slower                                              |
| pprint_safe_repr           | 778 ms                                                                | 780 ms: 1.00x slower                                               |
| pprint_pformat             | 1.61 sec                                                              | 1.62 sec: 1.00x slower                                             |
| tomli_loads                | 2.12 sec                                                              | 2.13 sec: 1.00x slower                                             |
| chaos                      | 62.7 ms                                                               | 62.9 ms: 1.00x slower                                              |
| scimark_sor                | 122 ms                                                                | 122 ms: 1.00x slower                                               |
| k_core                     | 2.23 sec                                                              | 2.24 sec: 1.00x slower                                             |
| regex_compile              | 144 ms                                                                | 145 ms: 1.00x slower                                               |
| sympy_integrate            | 22.2 ms                                                               | 22.3 ms: 1.00x slower                                              |
| xml_etree_generate         | 96.1 ms                                                               | 96.6 ms: 1.01x slower                                              |
| raytrace                   | 296 ms                                                                | 297 ms: 1.01x slower                                               |
| 2to3                       | 284 ms                                                                | 286 ms: 1.01x slower                                               |
| fannkuch                   | 471 ms                                                                | 473 ms: 1.01x slower                                               |
| shortest_path              | 531 ms                                                                | 534 ms: 1.01x slower                                               |
| async_generators           | 364 ms                                                                | 366 ms: 1.01x slower                                               |
| sympy_str                  | 316 ms                                                                | 318 ms: 1.01x slower                                               |
| deepcopy_reduce            | 3.02 us                                                               | 3.04 us: 1.01x slower                                              |
| coverage                   | 110 ms                                                                | 111 ms: 1.01x slower                                               |
| logging_silent             | 533 ns                                                                | 536 ns: 1.01x slower                                               |
| async_tree_memoization_tg  | 282 ms                                                                | 284 ms: 1.01x slower                                               |
| mdp                        | 1.32 sec                                                              | 1.34 sec: 1.01x slower                                             |
| async_tree_memoization     | 310 ms                                                                | 313 ms: 1.01x slower                                               |
| connected_components       | 481 ms                                                                | 486 ms: 1.01x slower                                               |
| genshi_xml                 | 54.9 ms                                                               | 55.4 ms: 1.01x slower                                              |
| django_template            | 40.5 ms                                                               | 40.9 ms: 1.01x slower                                              |
| float                      | 70.0 ms                                                               | 70.7 ms: 1.01x slower                                              |
| go                         | 123 ms                                                                | 124 ms: 1.01x slower                                               |
| scimark_lu                 | 129 ms                                                                | 131 ms: 1.01x slower                                               |
| crypto_pyaes               | 85.5 ms                                                               | 86.5 ms: 1.01x slower                                              |
| scimark_fft                | 365 ms                                                                | 369 ms: 1.01x slower                                               |
| genshi_text                | 26.2 ms                                                               | 26.5 ms: 1.01x slower                                              |
| thrift                     | 878 us                                                                | 889 us: 1.01x slower                                               |
| richards_super             | 57.6 ms                                                               | 58.3 ms: 1.01x slower                                              |
| json_dumps                 | 13.2 ms                                                               | 13.4 ms: 1.01x slower                                              |
| pyflate                    | 474 ms                                                                | 481 ms: 1.01x slower                                               |
| generators                 | 30.3 ms                                                               | 30.7 ms: 1.02x slower                                              |
| sqlglot_v2_parse           | 1.44 ms                                                               | 1.47 ms: 1.02x slower                                              |
| richards                   | 50.0 ms                                                               | 50.7 ms: 1.02x slower                                              |
| sympy_sum                  | 178 ms                                                                | 181 ms: 1.02x slower                                               |
| xml_etree_process          | 68.6 ms                                                               | 69.8 ms: 1.02x slower                                              |
| sympy_expand               | 528 ms                                                                | 538 ms: 1.02x slower                                               |
| telco                      | 8.62 ms                                                               | 8.79 ms: 1.02x slower                                              |
| comprehensions             | 19.2 us                                                               | 19.6 us: 1.02x slower                                              |
| spectral_norm              | 108 ms                                                                | 111 ms: 1.04x slower                                               |
| scimark_sparse_mat_mult    | 5.25 ms                                                               | 5.62 ms: 1.07x slower                                              |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                       |

Benchmark hidden because not significant (28): meteor_contest, subparsers, typing_runtime_protocols, json_loads, async_tree_io_tg, sqlglot_v2_optimize, async_tree_none, xml_etree_iterparse, many_optionals, sqlite_synth, nbody, dulwich_log, pathlib, json, bench_thread_pool, scimark_monte_carlo, python_startup_no_site, python_startup, asyncio_websockets, logging_simple, deltablue, sphinx, pycparser, async_tree_none_tg, html5lib, async_tree_io, sqlglot_v2_transpile, pylint

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x