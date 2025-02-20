# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: aa60561
- commit date: 2025-02-20
- overall geometric mean: 1.005x slower
- HPT reliability: 99.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 300 ms                                                                 | 304 ms: 1.01x slower                                              |
| html5lib       | 70.2 ms                                                                | 73.2 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_generators           | 371 ms                                                                 | 372 ms: 1.00x slower                                              |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 532 ms: 1.01x slower                                              |
| async_tree_io_tg           | 550 ms                                                                 | 559 ms: 1.02x slower                                              |
| async_tree_memoization     | 338 ms                                                                 | 344 ms: 1.02x slower                                              |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 501 ms: 1.02x slower                                              |
| coroutines                 | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                             |
| async_tree_none_tg         | 237 ms                                                                 | 243 ms: 1.03x slower                                              |
| async_tree_memoization_tg  | 305 ms                                                                 | 313 ms: 1.03x slower                                              |
| async_tree_none            | 273 ms                                                                 | 283 ms: 1.04x slower                                              |
| async_tree_io              | 580 ms                                                                 | 602 ms: 1.04x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 128 ms: 1.04x faster                                              |
| pidigits       | 204 ms                                                                 | 198 ms: 1.03x faster                                              |
| float          | 76.0 ms                                                                | 74.7 ms: 1.02x faster                                             |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 24.0 ms                                                                | 23.5 ms: 1.02x faster                                             |
| regex_dna      | 179 ms                                                                 | 176 ms: 1.02x faster                                              |
| regex_compile  | 154 ms                                                                 | 155 ms: 1.01x slower                                              |
| regex_effbot   | 2.88 ms                                                                | 2.91 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_pure_python | 247 us                                                                 | 243 us: 1.01x faster                                              |
| json_loads           | 31.8 us                                                                | 31.4 us: 1.01x faster                                             |
| xml_etree_iterparse  | 88.2 ms                                                                | 87.7 ms: 1.01x faster                                             |
| tomli_loads          | 2.33 sec                                                               | 2.31 sec: 1.01x faster                                            |
| json_dumps           | 12.8 ms                                                                | 13.0 ms: 1.02x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (4): pickle_pure_python, xml_etree_process, xml_etree_generate, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.5 ms                                                                | 15.9 ms: 1.02x slower                                             |
| python_startup_no_site | 9.57 ms                                                                | 9.82 ms: 1.03x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 59.0 ms                                                                | 59.7 ms: 1.01x slower                                             |
| mako            | 15.7 ms                                                                | 15.9 ms: 1.01x slower                                             |
| django_template | 43.0 ms                                                                | 43.9 ms: 1.02x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-aa60561 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| spectral_norm              | 112 ms                                                                 | 107 ms: 1.04x faster                                              |
| nbody                      | 134 ms                                                                 | 128 ms: 1.04x faster                                              |
| pidigits                   | 204 ms                                                                 | 198 ms: 1.03x faster                                              |
| telco                      | 8.87 ms                                                                | 8.62 ms: 1.03x faster                                             |
| chaos                      | 70.9 ms                                                                | 69.2 ms: 1.02x faster                                             |
| regex_v8                   | 24.0 ms                                                                | 23.5 ms: 1.02x faster                                             |
| scimark_sparse_mat_mult    | 5.83 ms                                                                | 5.71 ms: 1.02x faster                                             |
| logging_format             | 8.24 us                                                                | 8.09 us: 1.02x faster                                             |
| float                      | 76.0 ms                                                                | 74.7 ms: 1.02x faster                                             |
| raytrace                   | 324 ms                                                                 | 319 ms: 1.02x faster                                              |
| regex_dna                  | 179 ms                                                                 | 176 ms: 1.02x faster                                              |
| deepcopy_reduce            | 3.16 us                                                                | 3.12 us: 1.02x faster                                             |
| unpickle_pure_python       | 247 us                                                                 | 243 us: 1.01x faster                                              |
| go                         | 139 ms                                                                 | 137 ms: 1.01x faster                                              |
| nqueens                    | 96.2 ms                                                                | 95.0 ms: 1.01x faster                                             |
| json_loads                 | 31.8 us                                                                | 31.4 us: 1.01x faster                                             |
| hexiom                     | 7.29 ms                                                                | 7.22 ms: 1.01x faster                                             |
| generators                 | 31.6 ms                                                                | 31.4 ms: 1.01x faster                                             |
| xml_etree_iterparse        | 88.2 ms                                                                | 87.7 ms: 1.01x faster                                             |
| tomli_loads                | 2.33 sec                                                               | 2.31 sec: 1.01x faster                                            |
| deltablue                  | 3.81 ms                                                                | 3.79 ms: 1.00x faster                                             |
| richards                   | 54.8 ms                                                                | 54.6 ms: 1.00x faster                                             |
| comprehensions             | 19.8 us                                                                | 19.8 us: 1.00x faster                                             |
| scimark_fft                | 392 ms                                                                 | 391 ms: 1.00x faster                                              |
| async_generators           | 371 ms                                                                 | 372 ms: 1.00x slower                                              |
| fannkuch                   | 488 ms                                                                 | 489 ms: 1.00x slower                                              |
| logging_silent             | 110 ns                                                                 | 110 ns: 1.00x slower                                              |
| scimark_monte_carlo        | 82.0 ms                                                                | 82.2 ms: 1.00x slower                                             |
| shortest_path              | 543 ms                                                                 | 546 ms: 1.01x slower                                              |
| dulwich_log                | 82.4 ms                                                                | 82.8 ms: 1.01x slower                                             |
| crypto_pyaes               | 86.9 ms                                                                | 87.4 ms: 1.01x slower                                             |
| sympy_sum                  | 186 ms                                                                 | 187 ms: 1.01x slower                                              |
| regex_compile              | 154 ms                                                                 | 155 ms: 1.01x slower                                              |
| regex_effbot               | 2.88 ms                                                                | 2.91 ms: 1.01x slower                                             |
| coverage                   | 97.0 ms                                                                | 98.0 ms: 1.01x slower                                             |
| 2to3                       | 300 ms                                                                 | 304 ms: 1.01x slower                                              |
| pycparser                  | 1.18 sec                                                               | 1.20 sec: 1.01x slower                                            |
| genshi_xml                 | 59.0 ms                                                                | 59.7 ms: 1.01x slower                                             |
| mako                       | 15.7 ms                                                                | 15.9 ms: 1.01x slower                                             |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 532 ms: 1.01x slower                                              |
| pyflate                    | 487 ms                                                                 | 494 ms: 1.01x slower                                              |
| pprint_pformat             | 1.70 sec                                                               | 1.72 sec: 1.01x slower                                            |
| subparsers                 | 25.3 ms                                                                | 25.7 ms: 1.02x slower                                             |
| gc_traversal               | 1.72 ms                                                                | 1.75 ms: 1.02x slower                                             |
| async_tree_io_tg           | 550 ms                                                                 | 559 ms: 1.02x slower                                              |
| scimark_lu                 | 138 ms                                                                 | 141 ms: 1.02x slower                                              |
| pprint_safe_repr           | 822 ms                                                                 | 836 ms: 1.02x slower                                              |
| many_optionals             | 1.18 ms                                                                | 1.20 ms: 1.02x slower                                             |
| async_tree_memoization     | 338 ms                                                                 | 344 ms: 1.02x slower                                              |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 501 ms: 1.02x slower                                              |
| sympy_str                  | 334 ms                                                                 | 340 ms: 1.02x slower                                              |
| bench_mp_pool              | 94.9 ms                                                                | 96.7 ms: 1.02x slower                                             |
| create_gc_cycles           | 1.36 ms                                                                | 1.38 ms: 1.02x slower                                             |
| json_dumps                 | 12.8 ms                                                                | 13.0 ms: 1.02x slower                                             |
| django_template            | 43.0 ms                                                                | 43.9 ms: 1.02x slower                                             |
| coroutines                 | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                             |
| python_startup             | 15.5 ms                                                                | 15.9 ms: 1.02x slower                                             |
| async_tree_none_tg         | 237 ms                                                                 | 243 ms: 1.03x slower                                              |
| python_startup_no_site     | 9.57 ms                                                                | 9.82 ms: 1.03x slower                                             |
| async_tree_memoization_tg  | 305 ms                                                                 | 313 ms: 1.03x slower                                              |
| sqlalchemy_imperative      | 23.7 ms                                                                | 24.5 ms: 1.03x slower                                             |
| mdp                        | 2.66 sec                                                               | 2.76 sec: 1.04x slower                                            |
| async_tree_none            | 273 ms                                                                 | 283 ms: 1.04x slower                                              |
| async_tree_io              | 580 ms                                                                 | 602 ms: 1.04x slower                                              |
| html5lib                   | 70.2 ms                                                                | 73.2 ms: 1.04x slower                                             |
| sqlglot_parse              | 1.58 ms                                                                | 1.67 ms: 1.06x slower                                             |
| sqlglot_transpile          | 1.91 ms                                                                | 2.06 ms: 1.08x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (29): json, typing_runtime_protocols, pickle_pure_python, genshi_text, sqlglot_normalize, deepcopy, richards_super, scimark_sor, xml_etree_process, sympy_expand, bench_thread_pool, meteor_contest, k_core, sqlglot_optimize, sqlalchemy_declarative, bpe_tokeniser, thrift, xml_etree_generate, sympy_integrate, asyncio_websockets, sqlite_synth, sphinx, xml_etree_parse, docutils, deepcopy_memo, pathlib, logging_simple, connected_components, pylint

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 99.85% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x