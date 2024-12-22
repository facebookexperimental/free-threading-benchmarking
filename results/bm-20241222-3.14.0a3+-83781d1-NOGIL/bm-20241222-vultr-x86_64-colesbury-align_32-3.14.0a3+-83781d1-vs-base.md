# Results vs. base

- fork: colesbury
- ref: align_32
- machine: linux-x86_64
- commit hash: 83781d1
- commit date: 2024-12-22
- overall geometric mean: 1.012x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 360 ms                                                                 | 357 ms: 1.01x faster                                          |
| docutils       | 3.03 sec                                                               | 2.99 sec: 1.01x faster                                        |
| html5lib       | 94.6 ms                                                                | 93.0 ms: 1.02x faster                                         |
| sphinx         | 1.16 sec                                                               | 1.15 sec: 1.01x faster                                        |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 569 ms                                                                 | 563 ms: 1.01x faster                                          |
| async_generators           | 450 ms                                                                 | 446 ms: 1.01x faster                                          |
| coroutines                 | 24.4 ms                                                                | 24.6 ms: 1.01x slower                                         |
| async_tree_memoization_tg  | 401 ms                                                                 | 406 ms: 1.01x slower                                          |
| async_tree_io              | 754 ms                                                                 | 766 ms: 1.02x slower                                          |
| async_tree_memoization     | 426 ms                                                                 | 435 ms: 1.02x slower                                          |
| async_tree_none            | 350 ms                                                                 | 357 ms: 1.02x slower                                          |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                  |

Benchmark hidden because not significant (4): asyncio_websockets, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| nbody          | 128 ms                                                                 | 120 ms: 1.07x faster                                          |
| float          | 113 ms                                                                 | 109 ms: 1.04x faster                                          |
| pidigits       | 184 ms                                                                 | 181 ms: 1.02x faster                                          |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_v8       | 24.7 ms                                                                | 22.4 ms: 1.10x faster                                         |
| regex_effbot   | 2.76 ms                                                                | 2.63 ms: 1.05x faster                                         |
| regex_dna      | 186 ms                                                                 | 178 ms: 1.04x faster                                          |
| regex_compile  | 169 ms                                                                 | 168 ms: 1.01x faster                                          |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| json_dumps           | 14.1 ms                                                                | 13.3 ms: 1.05x faster                                         |
| tomli_loads          | 2.56 sec                                                               | 2.47 sec: 1.04x faster                                        |
| json_loads           | 28.2 us                                                                | 27.5 us: 1.02x faster                                         |
| pickle_pure_python   | 503 us                                                                 | 495 us: 1.02x faster                                          |
| xml_etree_process    | 73.8 ms                                                                | 73.5 ms: 1.00x faster                                         |
| xml_etree_generate   | 98.1 ms                                                                | 97.8 ms: 1.00x faster                                         |
| xml_etree_iterparse  | 90.4 ms                                                                | 90.1 ms: 1.00x faster                                         |
| unpickle_pure_python | 326 us                                                                 | 327 us: 1.00x slower                                          |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                  |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 17.0 ms: 1.01x faster                                         |
| python_startup_no_site | 10.2 ms                                                                | 10.1 ms: 1.01x faster                                         |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| mako            | 16.9 ms                                                                | 16.5 ms: 1.02x faster                                         |
| genshi_text     | 30.6 ms                                                                | 30.2 ms: 1.01x faster                                         |
| genshi_xml      | 63.4 ms                                                                | 64.0 ms: 1.01x slower                                         |
| django_template | 49.9 ms                                                                | 51.2 ms: 1.02x slower                                         |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd | bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3+-83781d1 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_v8                   | 24.7 ms                                                                | 22.4 ms: 1.10x faster                                         |
| scimark_sparse_mat_mult    | 5.45 ms                                                                | 4.97 ms: 1.10x faster                                         |
| scimark_fft                | 381 ms                                                                 | 355 ms: 1.07x faster                                          |
| nbody                      | 128 ms                                                                 | 120 ms: 1.07x faster                                          |
| json_dumps                 | 14.1 ms                                                                | 13.3 ms: 1.05x faster                                         |
| regex_effbot               | 2.76 ms                                                                | 2.63 ms: 1.05x faster                                         |
| generators                 | 38.3 ms                                                                | 36.7 ms: 1.04x faster                                         |
| spectral_norm              | 113 ms                                                                 | 108 ms: 1.04x faster                                          |
| regex_dna                  | 186 ms                                                                 | 178 ms: 1.04x faster                                          |
| create_gc_cycles           | 1.81 ms                                                                | 1.74 ms: 1.04x faster                                         |
| deepcopy_memo              | 41.0 us                                                                | 39.4 us: 1.04x faster                                         |
| tomli_loads                | 2.56 sec                                                               | 2.47 sec: 1.04x faster                                        |
| float                      | 113 ms                                                                 | 109 ms: 1.04x faster                                          |
| go                         | 239 ms                                                                 | 231 ms: 1.03x faster                                          |
| chaos                      | 96.4 ms                                                                | 93.6 ms: 1.03x faster                                         |
| scimark_sor                | 217 ms                                                                 | 211 ms: 1.03x faster                                          |
| json_loads                 | 28.2 us                                                                | 27.5 us: 1.02x faster                                         |
| raytrace                   | 489 ms                                                                 | 477 ms: 1.02x faster                                          |
| pyflate                    | 653 ms                                                                 | 637 ms: 1.02x faster                                          |
| comprehensions             | 27.1 us                                                                | 26.5 us: 1.02x faster                                         |
| mako                       | 16.9 ms                                                                | 16.5 ms: 1.02x faster                                         |
| deltablue                  | 7.31 ms                                                                | 7.15 ms: 1.02x faster                                         |
| gc_traversal               | 3.28 ms                                                                | 3.21 ms: 1.02x faster                                         |
| scimark_monte_carlo        | 106 ms                                                                 | 104 ms: 1.02x faster                                          |
| html5lib                   | 94.6 ms                                                                | 93.0 ms: 1.02x faster                                         |
| pidigits                   | 184 ms                                                                 | 181 ms: 1.02x faster                                          |
| nqueens                    | 99.9 ms                                                                | 98.3 ms: 1.02x faster                                         |
| hexiom                     | 9.52 ms                                                                | 9.37 ms: 1.02x faster                                         |
| pickle_pure_python         | 503 us                                                                 | 495 us: 1.02x faster                                          |
| sqlglot_parse              | 2.34 ms                                                                | 2.31 ms: 1.01x faster                                         |
| crypto_pyaes               | 90.4 ms                                                                | 89.3 ms: 1.01x faster                                         |
| sphinx                     | 1.16 sec                                                               | 1.15 sec: 1.01x faster                                        |
| meteor_contest             | 132 ms                                                                 | 130 ms: 1.01x faster                                          |
| genshi_text                | 30.6 ms                                                                | 30.2 ms: 1.01x faster                                         |
| docutils                   | 3.03 sec                                                               | 2.99 sec: 1.01x faster                                        |
| bpe_tokeniser              | 5.03 sec                                                               | 4.97 sec: 1.01x faster                                        |
| sqlglot_transpile          | 2.72 ms                                                                | 2.69 ms: 1.01x faster                                         |
| bench_mp_pool              | 108 ms                                                                 | 107 ms: 1.01x faster                                          |
| async_tree_cpu_io_mixed_tg | 569 ms                                                                 | 563 ms: 1.01x faster                                          |
| python_startup             | 17.2 ms                                                                | 17.0 ms: 1.01x faster                                         |
| pycparser                  | 1.40 sec                                                               | 1.39 sec: 1.01x faster                                        |
| python_startup_no_site     | 10.2 ms                                                                | 10.1 ms: 1.01x faster                                         |
| regex_compile              | 169 ms                                                                 | 168 ms: 1.01x faster                                          |
| async_generators           | 450 ms                                                                 | 446 ms: 1.01x faster                                          |
| 2to3                       | 360 ms                                                                 | 357 ms: 1.01x faster                                          |
| k_core                     | 2.36 sec                                                               | 2.34 sec: 1.01x faster                                        |
| deepcopy                   | 329 us                                                                 | 326 us: 1.01x faster                                          |
| scimark_lu                 | 158 ms                                                                 | 158 ms: 1.01x faster                                          |
| sqlalchemy_declarative     | 197 ms                                                                 | 196 ms: 1.01x faster                                          |
| sympy_sum                  | 351 ms                                                                 | 350 ms: 1.00x faster                                          |
| sympy_expand               | 961 ms                                                                 | 957 ms: 1.00x faster                                          |
| sympy_integrate            | 29.8 ms                                                                | 29.7 ms: 1.00x faster                                         |
| xml_etree_process          | 73.8 ms                                                                | 73.5 ms: 1.00x faster                                         |
| xml_etree_generate         | 98.1 ms                                                                | 97.8 ms: 1.00x faster                                         |
| xml_etree_iterparse        | 90.4 ms                                                                | 90.1 ms: 1.00x faster                                         |
| unpickle_pure_python       | 326 us                                                                 | 327 us: 1.00x slower                                          |
| coroutines                 | 24.4 ms                                                                | 24.6 ms: 1.01x slower                                         |
| many_optionals             | 1.25 ms                                                                | 1.26 ms: 1.01x slower                                         |
| telco                      | 8.72 ms                                                                | 8.80 ms: 1.01x slower                                         |
| genshi_xml                 | 63.4 ms                                                                | 64.0 ms: 1.01x slower                                         |
| thrift                     | 999 us                                                                 | 1.01 ms: 1.01x slower                                         |
| async_tree_memoization_tg  | 401 ms                                                                 | 406 ms: 1.01x slower                                          |
| logging_format             | 10.2 us                                                                | 10.4 us: 1.01x slower                                         |
| pathlib                    | 19.6 ms                                                                | 19.9 ms: 1.01x slower                                         |
| dulwich_log                | 91.2 ms                                                                | 92.5 ms: 1.01x slower                                         |
| typing_runtime_protocols   | 205 us                                                                 | 208 us: 1.02x slower                                          |
| async_tree_io              | 754 ms                                                                 | 766 ms: 1.02x slower                                          |
| async_tree_memoization     | 426 ms                                                                 | 435 ms: 1.02x slower                                          |
| async_tree_none            | 350 ms                                                                 | 357 ms: 1.02x slower                                          |
| django_template            | 49.9 ms                                                                | 51.2 ms: 1.02x slower                                         |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                  |

Benchmark hidden because not significant (26): richards_super, asyncio_websockets, richards, async_tree_cpu_io_mixed, deepcopy_reduce, pprint_safe_repr, logging_silent, async_tree_none_tg, mdp, sqlglot_normalize, pprint_pformat, logging_simple, sympy_str, coverage, pylint, connected_components, fannkuch, bench_thread_pool, sqlglot_optimize, shortest_path, async_tree_io_tg, xml_etree_parse, subparsers, json, sqlite_synth, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x