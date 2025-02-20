# Results vs. base

- fork: DinoV
- ref: nolock_loadattr_with
- machine: linux-x86_64
- commit hash: 6a1fe7e
- commit date: 2025-02-19
- overall geometric mean: 1.006x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 303 ms                                                                 | 300 ms: 1.01x faster                                                  |
| html5lib       | 70.0 ms                                                                | 69.5 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 23.5 ms                                                                | 23.1 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed    | 529 ms                                                                 | 521 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                 | 488 ms: 1.01x faster                                                  |
| async_generators           | 372 ms                                                                 | 370 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (7): async_tree_io, asyncio_websockets, async_tree_memoization, async_tree_io_tg, async_tree_none_tg, async_tree_none, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.8 ms                                                                | 76.1 ms: 1.01x faster                                                 |
| nbody          | 130 ms                                                                 | 132 ms: 1.02x slower                                                  |
| pidigits       | 191 ms                                                                 | 196 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 155 ms                                                                 | 154 ms: 1.01x faster                                                  |
| regex_dna      | 172 ms                                                                 | 176 ms: 1.02x slower                                                  |
| regex_v8       | 23.1 ms                                                                | 23.6 ms: 1.02x slower                                                 |
| regex_effbot   | 2.76 ms                                                                | 2.88 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 250 us                                                                 | 244 us: 1.03x faster                                                  |
| pickle_pure_python   | 363 us                                                                 | 355 us: 1.02x faster                                                  |
| tomli_loads          | 2.35 sec                                                               | 2.33 sec: 1.01x faster                                                |
| xml_etree_process    | 69.8 ms                                                                | 69.2 ms: 1.01x faster                                                 |
| json_loads           | 31.6 us                                                                | 31.5 us: 1.00x faster                                                 |
| json_dumps           | 12.8 ms                                                                | 12.8 ms: 1.00x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 128 ms: 1.00x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_generate

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
| django_template | 42.5 ms                                                                | 41.8 ms: 1.02x faster                                                 |
| mako            | 15.7 ms                                                                | 15.7 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 | bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5+-6a1fe7e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| logging_silent             | 115 ns                                                                 | 108 ns: 1.07x faster                                                  |
| logging_format             | 8.37 us                                                                | 7.98 us: 1.05x faster                                                 |
| mdp                        | 2.77 sec                                                               | 2.67 sec: 1.04x faster                                                |
| thrift                     | 910 us                                                                 | 882 us: 1.03x faster                                                  |
| nqueens                    | 97.1 ms                                                                | 94.5 ms: 1.03x faster                                                 |
| unpickle_pure_python       | 250 us                                                                 | 244 us: 1.03x faster                                                  |
| pickle_pure_python         | 363 us                                                                 | 355 us: 1.02x faster                                                  |
| pyflate                    | 500 ms                                                                 | 491 ms: 1.02x faster                                                  |
| go                         | 140 ms                                                                 | 137 ms: 1.02x faster                                                  |
| pathlib                    | 20.0 ms                                                                | 19.7 ms: 1.02x faster                                                 |
| logging_simple             | 7.22 us                                                                | 7.10 us: 1.02x faster                                                 |
| coroutines                 | 23.5 ms                                                                | 23.1 ms: 1.02x faster                                                 |
| richards                   | 55.4 ms                                                                | 54.5 ms: 1.02x faster                                                 |
| deltablue                  | 3.87 ms                                                                | 3.81 ms: 1.02x faster                                                 |
| hexiom                     | 7.35 ms                                                                | 7.23 ms: 1.02x faster                                                 |
| django_template            | 42.5 ms                                                                | 41.8 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed    | 529 ms                                                                 | 521 ms: 1.02x faster                                                  |
| raytrace                   | 325 ms                                                                 | 320 ms: 1.01x faster                                                  |
| sympy_expand               | 550 ms                                                                 | 542 ms: 1.01x faster                                                  |
| subparsers                 | 25.8 ms                                                                | 25.5 ms: 1.01x faster                                                 |
| sqlglot_normalize          | 121 ms                                                                 | 119 ms: 1.01x faster                                                  |
| scimark_monte_carlo        | 83.1 ms                                                                | 82.0 ms: 1.01x faster                                                 |
| deepcopy                   | 314 us                                                                 | 310 us: 1.01x faster                                                  |
| generators                 | 31.9 ms                                                                | 31.5 ms: 1.01x faster                                                 |
| richards_super             | 64.8 ms                                                                | 64.0 ms: 1.01x faster                                                 |
| sqlalchemy_imperative      | 23.8 ms                                                                | 23.5 ms: 1.01x faster                                                 |
| sqlglot_transpile          | 1.92 ms                                                                | 1.90 ms: 1.01x faster                                                 |
| spectral_norm              | 110 ms                                                                 | 109 ms: 1.01x faster                                                  |
| sqlglot_parse              | 1.59 ms                                                                | 1.58 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                 | 488 ms: 1.01x faster                                                  |
| sqlalchemy_declarative     | 157 ms                                                                 | 156 ms: 1.01x faster                                                  |
| float                      | 76.8 ms                                                                | 76.1 ms: 1.01x faster                                                 |
| deepcopy_reduce            | 3.24 us                                                                | 3.20 us: 1.01x faster                                                 |
| deepcopy_memo              | 38.5 us                                                                | 38.2 us: 1.01x faster                                                 |
| sympy_str                  | 334 ms                                                                 | 331 ms: 1.01x faster                                                  |
| tomli_loads                | 2.35 sec                                                               | 2.33 sec: 1.01x faster                                                |
| 2to3                       | 303 ms                                                                 | 300 ms: 1.01x faster                                                  |
| xml_etree_process          | 69.8 ms                                                                | 69.2 ms: 1.01x faster                                                 |
| regex_compile              | 155 ms                                                                 | 154 ms: 1.01x faster                                                  |
| gc_traversal               | 1.73 ms                                                                | 1.72 ms: 1.01x faster                                                 |
| html5lib                   | 70.0 ms                                                                | 69.5 ms: 1.01x faster                                                 |
| bpe_tokeniser              | 4.71 sec                                                               | 4.67 sec: 1.01x faster                                                |
| scimark_sor                | 132 ms                                                                 | 131 ms: 1.01x faster                                                  |
| many_optionals             | 1.18 ms                                                                | 1.17 ms: 1.01x faster                                                 |
| async_generators           | 372 ms                                                                 | 370 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.37 ms                                                                | 1.36 ms: 1.01x faster                                                 |
| chaos                      | 70.5 ms                                                                | 70.1 ms: 1.01x faster                                                 |
| sympy_sum                  | 187 ms                                                                 | 186 ms: 1.01x faster                                                  |
| pycparser                  | 1.19 sec                                                               | 1.19 sec: 1.00x faster                                                |
| sympy_integrate            | 24.0 ms                                                                | 23.9 ms: 1.00x faster                                                 |
| python_startup_no_site     | 9.62 ms                                                                | 9.59 ms: 1.00x faster                                                 |
| json_loads                 | 31.6 us                                                                | 31.5 us: 1.00x faster                                                 |
| json_dumps                 | 12.8 ms                                                                | 12.8 ms: 1.00x faster                                                 |
| fannkuch                   | 491 ms                                                                 | 489 ms: 1.00x faster                                                  |
| bench_thread_pool          | 3.31 ms                                                                | 3.30 ms: 1.00x faster                                                 |
| python_startup             | 15.6 ms                                                                | 15.5 ms: 1.00x faster                                                 |
| crypto_pyaes               | 87.2 ms                                                                | 86.9 ms: 1.00x faster                                                 |
| xml_etree_parse            | 128 ms                                                                 | 128 ms: 1.00x slower                                                  |
| mako                       | 15.7 ms                                                                | 15.7 ms: 1.01x slower                                                 |
| comprehensions             | 19.7 us                                                                | 19.8 us: 1.01x slower                                                 |
| coverage                   | 97.4 ms                                                                | 98.2 ms: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 5.71 ms                                                                | 5.76 ms: 1.01x slower                                                 |
| telco                      | 8.63 ms                                                                | 8.70 ms: 1.01x slower                                                 |
| connected_components       | 495 ms                                                                 | 500 ms: 1.01x slower                                                  |
| nbody                      | 130 ms                                                                 | 132 ms: 1.02x slower                                                  |
| regex_dna                  | 172 ms                                                                 | 176 ms: 1.02x slower                                                  |
| regex_v8                   | 23.1 ms                                                                | 23.6 ms: 1.02x slower                                                 |
| pidigits                   | 191 ms                                                                 | 196 ms: 1.03x slower                                                  |
| regex_effbot               | 2.76 ms                                                                | 2.88 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (27): sphinx, async_tree_io, genshi_xml, asyncio_websockets, sqlglot_optimize, shortest_path, typing_runtime_protocols, dulwich_log, json, async_tree_memoization, scimark_lu, docutils, genshi_text, scimark_fft, pylint, pprint_safe_repr, async_tree_io_tg, xml_etree_iterparse, xml_etree_generate, pprint_pformat, bench_mp_pool, k_core, async_tree_none_tg, async_tree_none, meteor_contest, async_tree_memoization_tg, sqlite_synth

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x