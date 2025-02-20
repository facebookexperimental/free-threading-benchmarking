# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 32a747e
- commit date: 2025-02-19
- overall geometric mean: 1.001x slower
- HPT reliability: 95.06%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 300 ms                                                                 | 303 ms: 1.01x slower                                              |
| docutils       | 2.78 sec                                                               | 2.73 sec: 1.02x faster                                            |
| html5lib       | 70.2 ms                                                                | 72.2 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| coroutines                | 23.4 ms                                                                | 23.1 ms: 1.01x faster                                             |
| asyncio_websockets        | 519 ms                                                                 | 514 ms: 1.01x faster                                              |
| async_tree_io_tg          | 550 ms                                                                 | 554 ms: 1.01x slower                                              |
| async_tree_memoization_tg | 305 ms                                                                 | 308 ms: 1.01x slower                                              |
| async_tree_memoization    | 338 ms                                                                 | 341 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed   | 525 ms                                                                 | 530 ms: 1.01x slower                                              |
| async_tree_io             | 580 ms                                                                 | 586 ms: 1.01x slower                                              |
| async_tree_none_tg        | 237 ms                                                                 | 240 ms: 1.01x slower                                              |
| async_tree_none           | 273 ms                                                                 | 278 ms: 1.02x slower                                              |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (2): async_generators, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 129 ms: 1.04x faster                                              |
| pidigits       | 204 ms                                                                 | 199 ms: 1.03x faster                                              |
| float          | 76.0 ms                                                                | 75.7 ms: 1.00x faster                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 24.0 ms                                                                | 23.5 ms: 1.02x faster                                             |
| regex_effbot   | 2.88 ms                                                                | 2.85 ms: 1.01x faster                                             |
| regex_compile  | 154 ms                                                                 | 154 ms: 1.00x slower                                              |
| regex_dna      | 179 ms                                                                 | 181 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 364 us                                                                 | 360 us: 1.01x faster                                              |
| unpickle_pure_python | 247 us                                                                 | 245 us: 1.01x faster                                              |
| json_loads           | 31.8 us                                                                | 31.5 us: 1.01x faster                                             |
| json_dumps           | 12.8 ms                                                                | 12.7 ms: 1.00x faster                                             |
| xml_etree_process    | 69.2 ms                                                                | 69.6 ms: 1.01x slower                                             |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                              |
| xml_etree_generate   | 95.1 ms                                                                | 96.3 ms: 1.01x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (2): xml_etree_iterparse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.5 ms                                                                | 15.6 ms: 1.00x slower                                             |
| python_startup_no_site | 9.57 ms                                                                | 9.76 ms: 1.02x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 43.0 ms                                                                | 43.7 ms: 1.02x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (3): mako, genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20250219-vultr-x86_64-python-73801864d866c76ae26a-3.14.0a5+-7380186 | bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-32a747e |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| meteor_contest            | 132 ms                                                                 | 125 ms: 1.06x faster                                              |
| nbody                     | 134 ms                                                                 | 129 ms: 1.04x faster                                              |
| pidigits                  | 204 ms                                                                 | 199 ms: 1.03x faster                                              |
| scimark_sparse_mat_mult   | 5.83 ms                                                                | 5.71 ms: 1.02x faster                                             |
| regex_v8                  | 24.0 ms                                                                | 23.5 ms: 1.02x faster                                             |
| spectral_norm             | 112 ms                                                                 | 110 ms: 1.02x faster                                              |
| logging_silent            | 110 ns                                                                 | 108 ns: 1.02x faster                                              |
| docutils                  | 2.78 sec                                                               | 2.73 sec: 1.02x faster                                            |
| nqueens                   | 96.2 ms                                                                | 94.8 ms: 1.01x faster                                             |
| telco                     | 8.87 ms                                                                | 8.75 ms: 1.01x faster                                             |
| typing_runtime_protocols  | 199 us                                                                 | 196 us: 1.01x faster                                              |
| richards_super            | 63.8 ms                                                                | 63.0 ms: 1.01x faster                                             |
| richards                  | 54.8 ms                                                                | 54.1 ms: 1.01x faster                                             |
| generators                | 31.6 ms                                                                | 31.3 ms: 1.01x faster                                             |
| regex_effbot              | 2.88 ms                                                                | 2.85 ms: 1.01x faster                                             |
| pickle_pure_python        | 364 us                                                                 | 360 us: 1.01x faster                                              |
| fannkuch                  | 488 ms                                                                 | 483 ms: 1.01x faster                                              |
| go                        | 139 ms                                                                 | 137 ms: 1.01x faster                                              |
| coroutines                | 23.4 ms                                                                | 23.1 ms: 1.01x faster                                             |
| asyncio_websockets        | 519 ms                                                                 | 514 ms: 1.01x faster                                              |
| chaos                     | 70.9 ms                                                                | 70.4 ms: 1.01x faster                                             |
| unpickle_pure_python      | 247 us                                                                 | 245 us: 1.01x faster                                              |
| json_loads                | 31.8 us                                                                | 31.5 us: 1.01x faster                                             |
| deepcopy_memo             | 37.8 us                                                                | 37.6 us: 1.01x faster                                             |
| pathlib                   | 19.8 ms                                                                | 19.6 ms: 1.01x faster                                             |
| hexiom                    | 7.29 ms                                                                | 7.24 ms: 1.01x faster                                             |
| raytrace                  | 324 ms                                                                 | 323 ms: 1.01x faster                                              |
| scimark_fft               | 392 ms                                                                 | 390 ms: 1.01x faster                                              |
| sqlalchemy_declarative    | 156 ms                                                                 | 155 ms: 1.01x faster                                              |
| float                     | 76.0 ms                                                                | 75.7 ms: 1.00x faster                                             |
| json_dumps                | 12.8 ms                                                                | 12.7 ms: 1.00x faster                                             |
| regex_compile             | 154 ms                                                                 | 154 ms: 1.00x slower                                              |
| bpe_tokeniser             | 4.71 sec                                                               | 4.72 sec: 1.00x slower                                            |
| python_startup            | 15.5 ms                                                                | 15.6 ms: 1.00x slower                                             |
| sympy_str                 | 334 ms                                                                 | 336 ms: 1.01x slower                                              |
| xml_etree_process         | 69.2 ms                                                                | 69.6 ms: 1.01x slower                                             |
| async_tree_io_tg          | 550 ms                                                                 | 554 ms: 1.01x slower                                              |
| pyflate                   | 487 ms                                                                 | 490 ms: 1.01x slower                                              |
| 2to3                      | 300 ms                                                                 | 303 ms: 1.01x slower                                              |
| logging_format            | 8.24 us                                                                | 8.30 us: 1.01x slower                                             |
| subparsers                | 25.3 ms                                                                | 25.5 ms: 1.01x slower                                             |
| async_tree_memoization_tg | 305 ms                                                                 | 308 ms: 1.01x slower                                              |
| pycparser                 | 1.18 sec                                                               | 1.19 sec: 1.01x slower                                            |
| pprint_safe_repr          | 822 ms                                                                 | 829 ms: 1.01x slower                                              |
| async_tree_memoization    | 338 ms                                                                 | 341 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed   | 525 ms                                                                 | 530 ms: 1.01x slower                                              |
| pprint_pformat            | 1.70 sec                                                               | 1.72 sec: 1.01x slower                                            |
| bench_thread_pool         | 3.30 ms                                                                | 3.34 ms: 1.01x slower                                             |
| scimark_lu                | 138 ms                                                                 | 140 ms: 1.01x slower                                              |
| xml_etree_parse           | 128 ms                                                                 | 129 ms: 1.01x slower                                              |
| deepcopy_reduce           | 3.16 us                                                                | 3.20 us: 1.01x slower                                             |
| bench_mp_pool             | 94.9 ms                                                                | 96.0 ms: 1.01x slower                                             |
| async_tree_io             | 580 ms                                                                 | 586 ms: 1.01x slower                                              |
| regex_dna                 | 179 ms                                                                 | 181 ms: 1.01x slower                                              |
| xml_etree_generate        | 95.1 ms                                                                | 96.3 ms: 1.01x slower                                             |
| async_tree_none_tg        | 237 ms                                                                 | 240 ms: 1.01x slower                                              |
| coverage                  | 97.0 ms                                                                | 98.5 ms: 1.01x slower                                             |
| scimark_monte_carlo       | 82.0 ms                                                                | 83.3 ms: 1.02x slower                                             |
| async_tree_none           | 273 ms                                                                 | 278 ms: 1.02x slower                                              |
| django_template           | 43.0 ms                                                                | 43.7 ms: 1.02x slower                                             |
| gc_traversal              | 1.72 ms                                                                | 1.75 ms: 1.02x slower                                             |
| crypto_pyaes              | 86.9 ms                                                                | 88.6 ms: 1.02x slower                                             |
| logging_simple            | 7.23 us                                                                | 7.37 us: 1.02x slower                                             |
| sqlglot_transpile         | 1.91 ms                                                                | 1.95 ms: 1.02x slower                                             |
| create_gc_cycles          | 1.36 ms                                                                | 1.39 ms: 1.02x slower                                             |
| python_startup_no_site    | 9.57 ms                                                                | 9.76 ms: 1.02x slower                                             |
| html5lib                  | 70.2 ms                                                                | 72.2 ms: 1.03x slower                                             |
| sqlglot_parse             | 1.58 ms                                                                | 1.63 ms: 1.03x slower                                             |
| mdp                       | 2.66 sec                                                               | 2.80 sec: 1.05x slower                                            |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (27): thrift, json, sphinx, scimark_sor, many_optionals, k_core, deltablue, sympy_expand, comprehensions, async_generators, sympy_integrate, mako, deepcopy, sympy_sum, genshi_text, async_tree_cpu_io_mixed_tg, dulwich_log, sqlglot_normalize, xml_etree_iterparse, tomli_loads, connected_components, genshi_xml, shortest_path, pylint, sqlglot_optimize, sqlite_synth, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 95.06% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x