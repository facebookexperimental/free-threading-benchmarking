# Results vs. base

- fork: DinoV
- ref: nolock_loadattr_with
- machine: linux-x86_64
- commit hash: 6a1fe7e
- commit date: 2025-02-19
- overall geometric mean: 1.004x faster
- HPT reliability: 99.93%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 303 ms                                                                 | 301 ms: 1.01x faster                                                  |
| html5lib       | 70.0 ms                                                                | 71.2 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 23.5 ms                                                                | 23.1 ms: 1.02x faster                                                 |
| async_generators           | 372 ms                                                                 | 367 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                 | 490 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed    | 529 ms                                                                 | 525 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (7): async_tree_io, async_tree_memoization_tg, asyncio_websockets, async_tree_io_tg, async_tree_memoization, async_tree_none, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 130 ms                                                                 | 125 ms: 1.04x faster                                                  |
| float          | 76.8 ms                                                                | 74.9 ms: 1.03x faster                                                 |
| pidigits       | 191 ms                                                                 | 192 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 155 ms                                                                 | 154 ms: 1.00x faster                                                  |
| regex_v8       | 23.1 ms                                                                | 23.9 ms: 1.04x slower                                                 |
| regex_dna      | 172 ms                                                                 | 180 ms: 1.04x slower                                                  |
| regex_effbot   | 2.76 ms                                                                | 2.90 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 250 us                                                                 | 246 us: 1.02x faster                                                  |
| tomli_loads          | 2.35 sec                                                               | 2.31 sec: 1.02x faster                                                |
| xml_etree_process    | 69.8 ms                                                                | 69.1 ms: 1.01x faster                                                 |
| pickle_pure_python   | 363 us                                                                 | 360 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 87.9 ms                                                                | 87.6 ms: 1.00x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): json_dumps, json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.62 ms                                                                | 9.59 ms: 1.00x faster                                                 |
| python_startup         | 15.6 ms                                                                | 15.5 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 59.2 ms                                                                | 58.8 ms: 1.01x faster                                                 |
| django_template | 42.5 ms                                                                | 42.3 ms: 1.01x faster                                                 |
| mako            | 15.7 ms                                                                | 15.7 ms: 1.00x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.77 sec                                                               | 2.59 sec: 1.07x faster                                                |
| nbody                      | 130 ms                                                                 | 125 ms: 1.04x faster                                                  |
| chaos                      | 70.5 ms                                                                | 68.5 ms: 1.03x faster                                                 |
| spectral_norm              | 110 ms                                                                 | 107 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.24 us                                                                | 3.15 us: 1.03x faster                                                 |
| logging_format             | 8.37 us                                                                | 8.15 us: 1.03x faster                                                 |
| float                      | 76.8 ms                                                                | 74.9 ms: 1.03x faster                                                 |
| subparsers                 | 25.8 ms                                                                | 25.2 ms: 1.02x faster                                                 |
| deepcopy_memo              | 38.5 us                                                                | 37.7 us: 1.02x faster                                                 |
| pathlib                    | 20.0 ms                                                                | 19.6 ms: 1.02x faster                                                 |
| typing_runtime_protocols   | 200 us                                                                 | 196 us: 1.02x faster                                                  |
| deltablue                  | 3.87 ms                                                                | 3.80 ms: 1.02x faster                                                 |
| generators                 | 31.9 ms                                                                | 31.3 ms: 1.02x faster                                                 |
| coroutines                 | 23.5 ms                                                                | 23.1 ms: 1.02x faster                                                 |
| unpickle_pure_python       | 250 us                                                                 | 246 us: 1.02x faster                                                  |
| bpe_tokeniser              | 4.71 sec                                                               | 4.63 sec: 1.02x faster                                                |
| async_generators           | 372 ms                                                                 | 367 ms: 1.02x faster                                                  |
| nqueens                    | 97.1 ms                                                                | 95.7 ms: 1.02x faster                                                 |
| tomli_loads                | 2.35 sec                                                               | 2.31 sec: 1.02x faster                                                |
| deepcopy                   | 314 us                                                                 | 309 us: 1.01x faster                                                  |
| sympy_expand               | 550 ms                                                                 | 542 ms: 1.01x faster                                                  |
| hexiom                     | 7.35 ms                                                                | 7.26 ms: 1.01x faster                                                 |
| sqlglot_parse              | 1.59 ms                                                                | 1.58 ms: 1.01x faster                                                 |
| go                         | 140 ms                                                                 | 138 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.92 ms                                                                | 1.90 ms: 1.01x faster                                                 |
| crypto_pyaes               | 87.2 ms                                                                | 86.2 ms: 1.01x faster                                                 |
| xml_etree_process          | 69.8 ms                                                                | 69.1 ms: 1.01x faster                                                 |
| thrift                     | 910 us                                                                 | 901 us: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                 | 490 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed    | 529 ms                                                                 | 525 ms: 1.01x faster                                                  |
| 2to3                       | 303 ms                                                                 | 301 ms: 1.01x faster                                                  |
| pickle_pure_python         | 363 us                                                                 | 360 us: 1.01x faster                                                  |
| genshi_xml                 | 59.2 ms                                                                | 58.8 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 5.71 ms                                                                | 5.68 ms: 1.01x faster                                                 |
| django_template            | 42.5 ms                                                                | 42.3 ms: 1.01x faster                                                 |
| sympy_integrate            | 24.0 ms                                                                | 23.9 ms: 1.01x faster                                                 |
| many_optionals             | 1.18 ms                                                                | 1.18 ms: 1.01x faster                                                 |
| sqlalchemy_declarative     | 157 ms                                                                 | 157 ms: 1.00x faster                                                  |
| comprehensions             | 19.7 us                                                                | 19.6 us: 1.00x faster                                                 |
| raytrace                   | 325 ms                                                                 | 323 ms: 1.00x faster                                                  |
| json                       | 5.35 ms                                                                | 5.33 ms: 1.00x faster                                                 |
| scimark_fft                | 390 ms                                                                 | 388 ms: 1.00x faster                                                  |
| sympy_str                  | 334 ms                                                                 | 333 ms: 1.00x faster                                                  |
| regex_compile              | 155 ms                                                                 | 154 ms: 1.00x faster                                                  |
| fannkuch                   | 491 ms                                                                 | 489 ms: 1.00x faster                                                  |
| python_startup_no_site     | 9.62 ms                                                                | 9.59 ms: 1.00x faster                                                 |
| xml_etree_iterparse        | 87.9 ms                                                                | 87.6 ms: 1.00x faster                                                 |
| bench_thread_pool          | 3.31 ms                                                                | 3.30 ms: 1.00x faster                                                 |
| python_startup             | 15.6 ms                                                                | 15.5 ms: 1.00x faster                                                 |
| coverage                   | 97.4 ms                                                                | 97.7 ms: 1.00x slower                                                 |
| mako                       | 15.7 ms                                                                | 15.7 ms: 1.00x slower                                                 |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| pidigits                   | 191 ms                                                                 | 192 ms: 1.01x slower                                                  |
| pprint_safe_repr           | 833 ms                                                                 | 840 ms: 1.01x slower                                                  |
| pprint_pformat             | 1.71 sec                                                               | 1.74 sec: 1.01x slower                                                |
| telco                      | 8.63 ms                                                                | 8.73 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.03 us                                                                | 2.05 us: 1.01x slower                                                 |
| sqlalchemy_imperative      | 23.8 ms                                                                | 24.2 ms: 1.01x slower                                                 |
| meteor_contest             | 130 ms                                                                 | 132 ms: 1.02x slower                                                  |
| html5lib                   | 70.0 ms                                                                | 71.2 ms: 1.02x slower                                                 |
| regex_v8                   | 23.1 ms                                                                | 23.9 ms: 1.04x slower                                                 |
| regex_dna                  | 172 ms                                                                 | 180 ms: 1.04x slower                                                  |
| regex_effbot               | 2.76 ms                                                                | 2.90 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (33): logging_silent, async_tree_io, pycparser, sqlglot_optimize, richards_super, pylint, shortest_path, sphinx, sympy_sum, bench_mp_pool, richards, gc_traversal, k_core, create_gc_cycles, json_dumps, scimark_sor, async_tree_memoization_tg, sqlglot_normalize, scimark_monte_carlo, docutils, json_loads, asyncio_websockets, logging_simple, dulwich_log, xml_etree_generate, async_tree_io_tg, genshi_text, async_tree_memoization, pyflate, scimark_lu, connected_components, async_tree_none, async_tree_none_tg

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 99.93% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x