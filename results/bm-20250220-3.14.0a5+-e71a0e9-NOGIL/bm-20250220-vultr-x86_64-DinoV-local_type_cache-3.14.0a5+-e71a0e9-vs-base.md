# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: e71a0e9
- commit date: 2025-02-20
- overall geometric mean: 1.007x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 300 ms                                                                 | 303 ms: 1.01x slower                                              |
| docutils       | 2.78 sec                                                               | 2.80 sec: 1.01x slower                                            |
| html5lib       | 70.2 ms                                                                | 73.0 ms: 1.04x slower                                             |
| sphinx         | 1.09 sec                                                               | 1.10 sec: 1.01x slower                                            |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_generators           | 371 ms                                                                 | 373 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 496 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 530 ms: 1.01x slower                                              |
| coroutines                 | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                             |
| async_tree_memoization_tg  | 305 ms                                                                 | 313 ms: 1.02x slower                                              |
| async_tree_io              | 580 ms                                                                 | 597 ms: 1.03x slower                                              |
| async_tree_io_tg           | 550 ms                                                                 | 568 ms: 1.03x slower                                              |
| async_tree_none_tg         | 237 ms                                                                 | 244 ms: 1.03x slower                                              |
| async_tree_none            | 273 ms                                                                 | 282 ms: 1.03x slower                                              |
| async_tree_memoization     | 338 ms                                                                 | 350 ms: 1.03x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 204 ms                                                                 | 191 ms: 1.07x faster                                              |
| nbody          | 134 ms                                                                 | 132 ms: 1.01x faster                                              |
| float          | 76.0 ms                                                                | 76.3 ms: 1.00x slower                                             |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 24.0 ms                                                                | 23.5 ms: 1.02x faster                                             |
| regex_dna      | 179 ms                                                                 | 176 ms: 1.01x faster                                              |
| regex_compile  | 154 ms                                                                 | 155 ms: 1.01x slower                                              |
| regex_effbot   | 2.88 ms                                                                | 2.92 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_loads           | 31.8 us                                                                | 31.3 us: 1.01x faster                                             |
| xml_etree_process    | 69.2 ms                                                                | 69.8 ms: 1.01x slower                                             |
| xml_etree_generate   | 95.1 ms                                                                | 96.1 ms: 1.01x slower                                             |
| unpickle_pure_python | 247 us                                                                 | 250 us: 1.01x slower                                              |
| tomli_loads          | 2.33 sec                                                               | 2.36 sec: 1.01x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (4): pickle_pure_python, xml_etree_parse, json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.5 ms                                                                | 15.5 ms: 1.00x faster                                             |
| python_startup_no_site | 9.57 ms                                                                | 9.72 ms: 1.02x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 15.7 ms                                                                | 15.9 ms: 1.01x slower                                             |
| django_template | 43.0 ms                                                                | 44.3 ms: 1.03x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250220-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-e71a0e9 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits                   | 204 ms                                                                 | 191 ms: 1.07x faster                                              |
| spectral_norm              | 112 ms                                                                 | 109 ms: 1.03x faster                                              |
| scimark_sparse_mat_mult    | 5.83 ms                                                                | 5.69 ms: 1.03x faster                                             |
| regex_v8                   | 24.0 ms                                                                | 23.5 ms: 1.02x faster                                             |
| chaos                      | 70.9 ms                                                                | 69.8 ms: 1.02x faster                                             |
| json                       | 5.38 ms                                                                | 5.30 ms: 1.01x faster                                             |
| json_loads                 | 31.8 us                                                                | 31.3 us: 1.01x faster                                             |
| regex_dna                  | 179 ms                                                                 | 176 ms: 1.01x faster                                              |
| nbody                      | 134 ms                                                                 | 132 ms: 1.01x faster                                              |
| telco                      | 8.87 ms                                                                | 8.78 ms: 1.01x faster                                             |
| richards                   | 54.8 ms                                                                | 54.2 ms: 1.01x faster                                             |
| sqlglot_normalize          | 121 ms                                                                 | 120 ms: 1.01x faster                                              |
| scimark_fft                | 392 ms                                                                 | 388 ms: 1.01x faster                                              |
| scimark_sor                | 131 ms                                                                 | 130 ms: 1.01x faster                                              |
| richards_super             | 63.8 ms                                                                | 63.4 ms: 1.01x faster                                             |
| go                         | 139 ms                                                                 | 138 ms: 1.01x faster                                              |
| deepcopy                   | 309 us                                                                 | 307 us: 1.01x faster                                              |
| python_startup             | 15.5 ms                                                                | 15.5 ms: 1.00x faster                                             |
| float                      | 76.0 ms                                                                | 76.3 ms: 1.00x slower                                             |
| dulwich_log                | 82.4 ms                                                                | 82.7 ms: 1.00x slower                                             |
| deepcopy_memo              | 37.8 us                                                                | 38.0 us: 1.01x slower                                             |
| async_generators           | 371 ms                                                                 | 373 ms: 1.01x slower                                              |
| comprehensions             | 19.8 us                                                                | 19.9 us: 1.01x slower                                             |
| sympy_sum                  | 186 ms                                                                 | 187 ms: 1.01x slower                                              |
| shortest_path              | 543 ms                                                                 | 547 ms: 1.01x slower                                              |
| regex_compile              | 154 ms                                                                 | 155 ms: 1.01x slower                                              |
| sqlalchemy_declarative     | 156 ms                                                                 | 157 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 496 ms: 1.01x slower                                              |
| docutils                   | 2.78 sec                                                               | 2.80 sec: 1.01x slower                                            |
| xml_etree_process          | 69.2 ms                                                                | 69.8 ms: 1.01x slower                                             |
| 2to3                       | 300 ms                                                                 | 303 ms: 1.01x slower                                              |
| bench_mp_pool              | 94.9 ms                                                                | 95.8 ms: 1.01x slower                                             |
| scimark_monte_carlo        | 82.0 ms                                                                | 82.7 ms: 1.01x slower                                             |
| mako                       | 15.7 ms                                                                | 15.9 ms: 1.01x slower                                             |
| xml_etree_generate         | 95.1 ms                                                                | 96.1 ms: 1.01x slower                                             |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 530 ms: 1.01x slower                                              |
| generators                 | 31.6 ms                                                                | 32.0 ms: 1.01x slower                                             |
| deltablue                  | 3.81 ms                                                                | 3.85 ms: 1.01x slower                                             |
| coroutines                 | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                             |
| pathlib                    | 19.8 ms                                                                | 20.0 ms: 1.01x slower                                             |
| sphinx                     | 1.09 sec                                                               | 1.10 sec: 1.01x slower                                            |
| many_optionals             | 1.18 ms                                                                | 1.19 ms: 1.01x slower                                             |
| scimark_lu                 | 138 ms                                                                 | 140 ms: 1.01x slower                                              |
| nqueens                    | 96.2 ms                                                                | 97.4 ms: 1.01x slower                                             |
| connected_components       | 492 ms                                                                 | 498 ms: 1.01x slower                                              |
| unpickle_pure_python       | 247 us                                                                 | 250 us: 1.01x slower                                              |
| crypto_pyaes               | 86.9 ms                                                                | 88.0 ms: 1.01x slower                                             |
| pyflate                    | 487 ms                                                                 | 494 ms: 1.01x slower                                              |
| sympy_integrate            | 24.0 ms                                                                | 24.3 ms: 1.01x slower                                             |
| regex_effbot               | 2.88 ms                                                                | 2.92 ms: 1.01x slower                                             |
| hexiom                     | 7.29 ms                                                                | 7.39 ms: 1.01x slower                                             |
| tomli_loads                | 2.33 sec                                                               | 2.36 sec: 1.01x slower                                            |
| sympy_expand               | 548 ms                                                                 | 557 ms: 1.02x slower                                              |
| subparsers                 | 25.3 ms                                                                | 25.7 ms: 1.02x slower                                             |
| python_startup_no_site     | 9.57 ms                                                                | 9.72 ms: 1.02x slower                                             |
| gc_traversal               | 1.72 ms                                                                | 1.75 ms: 1.02x slower                                             |
| sympy_str                  | 334 ms                                                                 | 340 ms: 1.02x slower                                              |
| pycparser                  | 1.18 sec                                                               | 1.20 sec: 1.02x slower                                            |
| logging_silent             | 110 ns                                                                 | 112 ns: 1.02x slower                                              |
| coverage                   | 97.0 ms                                                                | 98.9 ms: 1.02x slower                                             |
| sqlalchemy_imperative      | 23.7 ms                                                                | 24.2 ms: 1.02x slower                                             |
| create_gc_cycles           | 1.36 ms                                                                | 1.39 ms: 1.02x slower                                             |
| async_tree_memoization_tg  | 305 ms                                                                 | 313 ms: 1.02x slower                                              |
| async_tree_io              | 580 ms                                                                 | 597 ms: 1.03x slower                                              |
| django_template            | 43.0 ms                                                                | 44.3 ms: 1.03x slower                                             |
| async_tree_io_tg           | 550 ms                                                                 | 568 ms: 1.03x slower                                              |
| async_tree_none_tg         | 237 ms                                                                 | 244 ms: 1.03x slower                                              |
| async_tree_none            | 273 ms                                                                 | 282 ms: 1.03x slower                                              |
| async_tree_memoization     | 338 ms                                                                 | 350 ms: 1.03x slower                                              |
| html5lib                   | 70.2 ms                                                                | 73.0 ms: 1.04x slower                                             |
| sqlglot_transpile          | 1.91 ms                                                                | 1.99 ms: 1.04x slower                                             |
| mdp                        | 2.66 sec                                                               | 2.78 sec: 1.04x slower                                            |
| sqlglot_parse              | 1.58 ms                                                                | 1.68 ms: 1.06x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (23): typing_runtime_protocols, pickle_pure_python, meteor_contest, xml_etree_parse, logging_format, asyncio_websockets, genshi_text, fannkuch, k_core, bench_thread_pool, bpe_tokeniser, pprint_pformat, pprint_safe_repr, json_dumps, raytrace, sqlite_synth, sqlglot_optimize, logging_simple, xml_etree_iterparse, deepcopy_reduce, thrift, genshi_xml, pylint

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x