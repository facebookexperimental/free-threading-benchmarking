# Results vs. base

- fork: faster-cpython
- ref: use_stackrefs
- machine: linux-x86_64
- commit hash: e2f1387
- commit date: 2025-03-03
- overall geometric mean: 1.000x slower
- HPT reliability: 76.19%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250303-vultr-x86_64-python-b3c18bfd828ba90b9c71-3.14.0a5+-b3c18bf | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 307 ms: 1.01x slower                                                      |
| html5lib       | 71.6 ms                                                                | 70.6 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250303-vultr-x86_64-python-b3c18bfd828ba90b9c71-3.14.0a5+-b3c18bf | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators           | 378 ms                                                                 | 374 ms: 1.01x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.00x faster                                                     |
| async_tree_memoization_tg  | 304 ms                                                                 | 307 ms: 1.01x slower                                                      |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                 | 499 ms: 1.01x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (7): asyncio_websockets, async_tree_io, async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250303-vultr-x86_64-python-b3c18bfd828ba90b9c71-3.14.0a5+-b3c18bf | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 77.8 ms                                                                | 77.0 ms: 1.01x faster                                                     |
| pidigits       | 191 ms                                                                 | 191 ms: 1.00x slower                                                      |
| nbody          | 130 ms                                                                 | 131 ms: 1.00x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250303-vultr-x86_64-python-b3c18bfd828ba90b9c71-3.14.0a5+-b3c18bf | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 176 ms                                                                 | 170 ms: 1.03x faster                                                      |
| regex_v8       | 23.4 ms                                                                | 23.0 ms: 1.02x faster                                                     |
| regex_effbot   | 2.78 ms                                                                | 2.74 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20250303-vultr-x86_64-python-b3c18bfd828ba90b9c71-3.14.0a5+-b3c18bf | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|--------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps         | 12.9 ms                                                                | 12.7 ms: 1.02x faster                                                     |
| tomli_loads        | 2.36 sec                                                               | 2.33 sec: 1.01x faster                                                    |
| xml_etree_generate | 96.3 ms                                                                | 95.5 ms: 1.01x faster                                                     |
| xml_etree_process  | 70.1 ms                                                                | 69.7 ms: 1.01x faster                                                     |
| json_loads         | 29.4 us                                                                | 29.3 us: 1.00x faster                                                     |
| pickle_pure_python | 361 us                                                                 | 362 us: 1.00x slower                                                      |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250303-vultr-x86_64-python-b3c18bfd828ba90b9c71-3.14.0a5+-b3c18bf | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 9.62 ms                                                                | 9.68 ms: 1.01x slower                                                     |
| python_startup         | 15.5 ms                                                                | 15.7 ms: 1.01x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250303-vultr-x86_64-python-b3c18bfd828ba90b9c71-3.14.0a5+-b3c18bf | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 43.2 ms                                                                | 42.5 ms: 1.02x faster                                                     |
| genshi_text     | 28.3 ms                                                                | 28.2 ms: 1.00x faster                                                     |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250303-vultr-x86_64-python-b3c18bfd828ba90b9c71-3.14.0a5+-b3c18bf | bm-20250303-vultr-x86_64-faster%2dcpython-use_stackrefs-3.14.0a5+-e2f1387 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna                  | 176 ms                                                                 | 170 ms: 1.03x faster                                                      |
| create_gc_cycles           | 1.30 ms                                                                | 1.28 ms: 1.02x faster                                                     |
| json_dumps                 | 12.9 ms                                                                | 12.7 ms: 1.02x faster                                                     |
| django_template            | 43.2 ms                                                                | 42.5 ms: 1.02x faster                                                     |
| deltablue                  | 3.87 ms                                                                | 3.81 ms: 1.02x faster                                                     |
| regex_v8                   | 23.4 ms                                                                | 23.0 ms: 1.02x faster                                                     |
| tomli_loads                | 2.36 sec                                                               | 2.33 sec: 1.01x faster                                                    |
| regex_effbot               | 2.78 ms                                                                | 2.74 ms: 1.01x faster                                                     |
| html5lib                   | 71.6 ms                                                                | 70.6 ms: 1.01x faster                                                     |
| telco                      | 8.90 ms                                                                | 8.78 ms: 1.01x faster                                                     |
| logging_silent             | 112 ns                                                                 | 111 ns: 1.01x faster                                                      |
| gc_traversal               | 1.72 ms                                                                | 1.70 ms: 1.01x faster                                                     |
| float                      | 77.8 ms                                                                | 77.0 ms: 1.01x faster                                                     |
| mdp                        | 2.68 sec                                                               | 2.65 sec: 1.01x faster                                                    |
| async_generators           | 378 ms                                                                 | 374 ms: 1.01x faster                                                      |
| pyflate                    | 509 ms                                                                 | 504 ms: 1.01x faster                                                      |
| xml_etree_generate         | 96.3 ms                                                                | 95.5 ms: 1.01x faster                                                     |
| deepcopy                   | 314 us                                                                 | 311 us: 1.01x faster                                                      |
| scimark_lu                 | 141 ms                                                                 | 140 ms: 1.01x faster                                                      |
| many_optionals             | 1.18 ms                                                                | 1.17 ms: 1.01x faster                                                     |
| logging_simple             | 7.22 us                                                                | 7.17 us: 1.01x faster                                                     |
| hexiom                     | 7.46 ms                                                                | 7.40 ms: 1.01x faster                                                     |
| xml_etree_process          | 70.1 ms                                                                | 69.7 ms: 1.01x faster                                                     |
| deepcopy_reduce            | 3.20 us                                                                | 3.18 us: 1.01x faster                                                     |
| genshi_text                | 28.3 ms                                                                | 28.2 ms: 1.00x faster                                                     |
| dulwich_log                | 83.2 ms                                                                | 82.8 ms: 1.00x faster                                                     |
| pprint_safe_repr           | 838 ms                                                                 | 834 ms: 1.00x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.00x faster                                                     |
| json_loads                 | 29.4 us                                                                | 29.3 us: 1.00x faster                                                     |
| crypto_pyaes               | 87.8 ms                                                                | 87.7 ms: 1.00x faster                                                     |
| pidigits                   | 191 ms                                                                 | 191 ms: 1.00x slower                                                      |
| pickle_pure_python         | 361 us                                                                 | 362 us: 1.00x slower                                                      |
| nbody                      | 130 ms                                                                 | 131 ms: 1.00x slower                                                      |
| richards                   | 54.8 ms                                                                | 55.0 ms: 1.00x slower                                                     |
| sqlglot_parse              | 1.60 ms                                                                | 1.60 ms: 1.01x slower                                                     |
| 2to3                       | 305 ms                                                                 | 307 ms: 1.01x slower                                                      |
| fannkuch                   | 494 ms                                                                 | 497 ms: 1.01x slower                                                      |
| sympy_sum                  | 186 ms                                                                 | 187 ms: 1.01x slower                                                      |
| nqueens                    | 96.1 ms                                                                | 96.7 ms: 1.01x slower                                                     |
| go                         | 140 ms                                                                 | 141 ms: 1.01x slower                                                      |
| python_startup_no_site     | 9.62 ms                                                                | 9.68 ms: 1.01x slower                                                     |
| python_startup             | 15.5 ms                                                                | 15.7 ms: 1.01x slower                                                     |
| raytrace                   | 321 ms                                                                 | 324 ms: 1.01x slower                                                      |
| coverage                   | 97.0 ms                                                                | 97.7 ms: 1.01x slower                                                     |
| sqlalchemy_declarative     | 156 ms                                                                 | 157 ms: 1.01x slower                                                      |
| bench_mp_pool              | 94.7 ms                                                                | 95.6 ms: 1.01x slower                                                     |
| scimark_fft                | 395 ms                                                                 | 398 ms: 1.01x slower                                                      |
| async_tree_memoization_tg  | 304 ms                                                                 | 307 ms: 1.01x slower                                                      |
| chaos                      | 69.1 ms                                                                | 69.8 ms: 1.01x slower                                                     |
| meteor_contest             | 128 ms                                                                 | 130 ms: 1.01x slower                                                      |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                 | 499 ms: 1.01x slower                                                      |
| deepcopy_memo              | 38.4 us                                                                | 38.9 us: 1.01x slower                                                     |
| sympy_expand               | 551 ms                                                                 | 558 ms: 1.01x slower                                                      |
| scimark_monte_carlo        | 82.9 ms                                                                | 83.9 ms: 1.01x slower                                                     |
| sqlalchemy_imperative      | 23.6 ms                                                                | 23.9 ms: 1.01x slower                                                     |
| subparsers                 | 24.9 ms                                                                | 25.3 ms: 1.01x slower                                                     |
| scimark_sor                | 134 ms                                                                 | 136 ms: 1.01x slower                                                      |
| generators                 | 31.7 ms                                                                | 32.3 ms: 1.02x slower                                                     |
| comprehensions             | 20.0 us                                                                | 20.3 us: 1.02x slower                                                     |
| spectral_norm              | 110 ms                                                                 | 113 ms: 1.03x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (36): thrift, xml_etree_parse, logging_format, sqlglot_normalize, connected_components, typing_runtime_protocols, xml_etree_iterparse, k_core, sqlglot_optimize, docutils, regex_compile, sympy_integrate, sqlglot_transpile, asyncio_websockets, sphinx, pathlib, async_tree_io, shortest_path, bpe_tokeniser, scimark_sparse_mat_mult, mako, pprint_pformat, sympy_str, json, richards_super, pylint, bench_thread_pool, async_tree_none, unpickle_pure_python, async_tree_io_tg, async_tree_cpu_io_mixed, genshi_xml, pycparser, sqlite_synth, async_tree_memoization, async_tree_none_tg

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 76.19% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x