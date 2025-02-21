# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 15d5533
- commit date: 2025-02-20
- overall geometric mean: 1.000x faster
- HPT reliability: 90.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 300 ms                                                                 | 302 ms: 1.01x slower                                              |
| docutils       | 2.78 sec                                                               | 2.72 sec: 1.02x faster                                            |
| html5lib       | 70.2 ms                                                                | 72.1 ms: 1.03x slower                                             |
| sphinx         | 1.09 sec                                                               | 1.08 sec: 1.01x faster                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 489 ms: 1.01x faster                                              |
| async_generators           | 371 ms                                                                 | 372 ms: 1.00x slower                                              |
| coroutines                 | 23.4 ms                                                                | 23.5 ms: 1.01x slower                                             |
| async_tree_memoization     | 338 ms                                                                 | 341 ms: 1.01x slower                                              |
| async_tree_io              | 580 ms                                                                 | 585 ms: 1.01x slower                                              |
| async_tree_none_tg         | 237 ms                                                                 | 240 ms: 1.01x slower                                              |
| async_tree_none            | 273 ms                                                                 | 277 ms: 1.01x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, asyncio_websockets, async_tree_memoization_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 204 ms                                                                 | 194 ms: 1.06x faster                                              |
| nbody          | 134 ms                                                                 | 128 ms: 1.05x faster                                              |
| float          | 76.0 ms                                                                | 76.4 ms: 1.00x slower                                             |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 24.0 ms                                                                | 23.9 ms: 1.01x faster                                             |
| regex_effbot   | 2.88 ms                                                                | 2.87 ms: 1.00x faster                                             |
| regex_compile  | 154 ms                                                                 | 154 ms: 1.00x slower                                              |
| regex_dna      | 179 ms                                                                 | 182 ms: 1.02x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_loads           | 31.8 us                                                                | 31.4 us: 1.01x faster                                             |
| xml_etree_iterparse  | 88.2 ms                                                                | 87.6 ms: 1.01x faster                                             |
| xml_etree_parse      | 128 ms                                                                 | 128 ms: 1.00x faster                                              |
| xml_etree_generate   | 95.1 ms                                                                | 94.9 ms: 1.00x faster                                             |
| json_dumps           | 12.8 ms                                                                | 12.8 ms: 1.00x slower                                             |
| pickle_pure_python   | 364 us                                                                 | 367 us: 1.01x slower                                              |
| unpickle_pure_python | 247 us                                                                 | 250 us: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (2): xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.5 ms                                                                | 15.8 ms: 1.02x slower                                             |
| python_startup_no_site | 9.57 ms                                                                | 9.75 ms: 1.02x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 43.0 ms                                                                | 42.3 ms: 1.02x faster                                             |
| mako            | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-15d5533 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits                   | 204 ms                                                                 | 194 ms: 1.06x faster                                              |
| nbody                      | 134 ms                                                                 | 128 ms: 1.05x faster                                              |
| spectral_norm              | 112 ms                                                                 | 109 ms: 1.03x faster                                              |
| thrift                     | 902 us                                                                 | 875 us: 1.03x faster                                              |
| docutils                   | 2.78 sec                                                               | 2.72 sec: 1.02x faster                                            |
| sqlalchemy_imperative      | 23.7 ms                                                                | 23.3 ms: 1.02x faster                                             |
| sympy_expand               | 548 ms                                                                 | 539 ms: 1.02x faster                                              |
| scimark_sparse_mat_mult    | 5.83 ms                                                                | 5.73 ms: 1.02x faster                                             |
| json                       | 5.38 ms                                                                | 5.30 ms: 1.02x faster                                             |
| django_template            | 43.0 ms                                                                | 42.3 ms: 1.02x faster                                             |
| sqlglot_normalize          | 121 ms                                                                 | 120 ms: 1.02x faster                                              |
| sqlalchemy_declarative     | 156 ms                                                                 | 154 ms: 1.02x faster                                              |
| chaos                      | 70.9 ms                                                                | 69.9 ms: 1.01x faster                                             |
| logging_format             | 8.24 us                                                                | 8.13 us: 1.01x faster                                             |
| deepcopy_reduce            | 3.16 us                                                                | 3.13 us: 1.01x faster                                             |
| sympy_integrate            | 24.0 ms                                                                | 23.7 ms: 1.01x faster                                             |
| logging_simple             | 7.23 us                                                                | 7.15 us: 1.01x faster                                             |
| json_loads                 | 31.8 us                                                                | 31.4 us: 1.01x faster                                             |
| sympy_sum                  | 186 ms                                                                 | 184 ms: 1.01x faster                                              |
| sphinx                     | 1.09 sec                                                               | 1.08 sec: 1.01x faster                                            |
| meteor_contest             | 132 ms                                                                 | 131 ms: 1.01x faster                                              |
| typing_runtime_protocols   | 199 us                                                                 | 197 us: 1.01x faster                                              |
| regex_v8                   | 24.0 ms                                                                | 23.9 ms: 1.01x faster                                             |
| sympy_str                  | 334 ms                                                                 | 332 ms: 1.01x faster                                              |
| sqlglot_optimize           | 61.5 ms                                                                | 61.1 ms: 1.01x faster                                             |
| xml_etree_iterparse        | 88.2 ms                                                                | 87.6 ms: 1.01x faster                                             |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 489 ms: 1.01x faster                                              |
| regex_effbot               | 2.88 ms                                                                | 2.87 ms: 1.00x faster                                             |
| deepcopy                   | 309 us                                                                 | 308 us: 1.00x faster                                              |
| scimark_fft                | 392 ms                                                                 | 390 ms: 1.00x faster                                              |
| xml_etree_parse            | 128 ms                                                                 | 128 ms: 1.00x faster                                              |
| k_core                     | 2.31 sec                                                               | 2.30 sec: 1.00x faster                                            |
| xml_etree_generate         | 95.1 ms                                                                | 94.9 ms: 1.00x faster                                             |
| crypto_pyaes               | 86.9 ms                                                                | 87.0 ms: 1.00x slower                                             |
| raytrace                   | 324 ms                                                                 | 325 ms: 1.00x slower                                              |
| bench_thread_pool          | 3.30 ms                                                                | 3.31 ms: 1.00x slower                                             |
| async_generators           | 371 ms                                                                 | 372 ms: 1.00x slower                                              |
| bpe_tokeniser              | 4.71 sec                                                               | 4.72 sec: 1.00x slower                                            |
| regex_compile              | 154 ms                                                                 | 154 ms: 1.00x slower                                              |
| json_dumps                 | 12.8 ms                                                                | 12.8 ms: 1.00x slower                                             |
| mako                       | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                             |
| float                      | 76.0 ms                                                                | 76.4 ms: 1.00x slower                                             |
| nqueens                    | 96.2 ms                                                                | 96.7 ms: 1.00x slower                                             |
| dulwich_log                | 82.4 ms                                                                | 82.8 ms: 1.01x slower                                             |
| create_gc_cycles           | 1.36 ms                                                                | 1.37 ms: 1.01x slower                                             |
| 2to3                       | 300 ms                                                                 | 302 ms: 1.01x slower                                              |
| fannkuch                   | 488 ms                                                                 | 490 ms: 1.01x slower                                              |
| hexiom                     | 7.29 ms                                                                | 7.34 ms: 1.01x slower                                             |
| gc_traversal               | 1.72 ms                                                                | 1.73 ms: 1.01x slower                                             |
| pycparser                  | 1.18 sec                                                               | 1.19 sec: 1.01x slower                                            |
| coroutines                 | 23.4 ms                                                                | 23.5 ms: 1.01x slower                                             |
| connected_components       | 492 ms                                                                 | 496 ms: 1.01x slower                                              |
| pathlib                    | 19.8 ms                                                                | 19.9 ms: 1.01x slower                                             |
| async_tree_memoization     | 338 ms                                                                 | 341 ms: 1.01x slower                                              |
| scimark_monte_carlo        | 82.0 ms                                                                | 82.6 ms: 1.01x slower                                             |
| comprehensions             | 19.8 us                                                                | 20.0 us: 1.01x slower                                             |
| pickle_pure_python         | 364 us                                                                 | 367 us: 1.01x slower                                              |
| async_tree_io              | 580 ms                                                                 | 585 ms: 1.01x slower                                              |
| bench_mp_pool              | 94.9 ms                                                                | 95.9 ms: 1.01x slower                                             |
| sqlglot_parse              | 1.58 ms                                                                | 1.60 ms: 1.01x slower                                             |
| scimark_lu                 | 138 ms                                                                 | 140 ms: 1.01x slower                                              |
| go                         | 139 ms                                                                 | 140 ms: 1.01x slower                                              |
| unpickle_pure_python       | 247 us                                                                 | 250 us: 1.01x slower                                              |
| coverage                   | 97.0 ms                                                                | 98.3 ms: 1.01x slower                                             |
| async_tree_none_tg         | 237 ms                                                                 | 240 ms: 1.01x slower                                              |
| async_tree_none            | 273 ms                                                                 | 277 ms: 1.01x slower                                              |
| pprint_pformat             | 1.70 sec                                                               | 1.73 sec: 1.02x slower                                            |
| scimark_sor                | 131 ms                                                                 | 133 ms: 1.02x slower                                              |
| deltablue                  | 3.81 ms                                                                | 3.87 ms: 1.02x slower                                             |
| python_startup             | 15.5 ms                                                                | 15.8 ms: 1.02x slower                                             |
| pyflate                    | 487 ms                                                                 | 496 ms: 1.02x slower                                              |
| python_startup_no_site     | 9.57 ms                                                                | 9.75 ms: 1.02x slower                                             |
| deepcopy_memo              | 37.8 us                                                                | 38.6 us: 1.02x slower                                             |
| regex_dna                  | 179 ms                                                                 | 182 ms: 1.02x slower                                              |
| pprint_safe_repr           | 822 ms                                                                 | 842 ms: 1.02x slower                                              |
| html5lib                   | 70.2 ms                                                                | 72.1 ms: 1.03x slower                                             |
| logging_silent             | 110 ns                                                                 | 114 ns: 1.03x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (19): pylint, telco, sqlite_synth, subparsers, async_tree_cpu_io_mixed, many_optionals, asyncio_websockets, mdp, genshi_xml, xml_etree_process, shortest_path, tomli_loads, richards, genshi_text, richards_super, generators, async_tree_memoization_tg, async_tree_io_tg, sqlglot_transpile

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 90.40% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x