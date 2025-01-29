# Results vs. base

- fork: Yhg1s
- ref: load_const_defer
- machine: linux-x86_64
- commit hash: fcfb942
- commit date: 2025-01-29
- overall geometric mean: 1.004x slower
- HPT reliability: 86.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 311 ms: 1.00x slower                                              |
| docutils       | 2.83 sec                                                               | 2.85 sec: 1.01x slower                                            |
| html5lib       | 70.6 ms                                                                | 72.9 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| coroutines                 | 25.3 ms                                                                | 24.5 ms: 1.03x faster                                             |
| async_generators           | 384 ms                                                                 | 378 ms: 1.02x faster                                              |
| asyncio_websockets         | 519 ms                                                                 | 516 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed    | 550 ms                                                                 | 594 ms: 1.08x slower                                              |
| async_tree_cpu_io_mixed_tg | 518 ms                                                                 | 561 ms: 1.08x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (6): async_tree_none, async_tree_io, async_tree_io_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 79.2 ms                                                                | 77.8 ms: 1.02x faster                                             |
| nbody          | 138 ms                                                                 | 142 ms: 1.03x slower                                              |
| pidigits       | 198 ms                                                                 | 224 ms: 1.13x slower                                              |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 2.87 ms                                                                | 2.93 ms: 1.02x slower                                             |
| regex_dna      | 177 ms                                                                 | 182 ms: 1.03x slower                                              |
| regex_v8       | 23.1 ms                                                                | 24.7 ms: 1.07x slower                                             |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                      |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps           | 13.1 ms                                                                | 13.0 ms: 1.01x faster                                             |
| xml_etree_process    | 70.4 ms                                                                | 70.1 ms: 1.00x faster                                             |
| xml_etree_generate   | 97.9 ms                                                                | 97.7 ms: 1.00x faster                                             |
| unpickle_pure_python | 256 us                                                                 | 257 us: 1.01x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (5): tomli_loads, xml_etree_parse, pickle_pure_python, json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.3 ms: 1.00x faster                                             |
| python_startup_no_site | 9.59 ms                                                                | 9.57 ms: 1.00x faster                                             |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 16.2 ms                                                                | 16.1 ms: 1.01x faster                                             |
| django_template | 43.3 ms                                                                | 43.5 ms: 1.00x slower                                             |
| genshi_xml      | 61.5 ms                                                                | 62.5 ms: 1.01x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| spectral_norm              | 115 ms                                                                 | 110 ms: 1.04x faster                                              |
| coroutines                 | 25.3 ms                                                                | 24.5 ms: 1.03x faster                                             |
| nqueens                    | 98.9 ms                                                                | 96.6 ms: 1.02x faster                                             |
| telco                      | 8.75 ms                                                                | 8.58 ms: 1.02x faster                                             |
| float                      | 79.2 ms                                                                | 77.8 ms: 1.02x faster                                             |
| async_generators           | 384 ms                                                                 | 378 ms: 1.02x faster                                              |
| richards                   | 58.8 ms                                                                | 57.9 ms: 1.01x faster                                             |
| logging_simple             | 7.56 us                                                                | 7.47 us: 1.01x faster                                             |
| logging_format             | 8.52 us                                                                | 8.42 us: 1.01x faster                                             |
| generators                 | 33.7 ms                                                                | 33.3 ms: 1.01x faster                                             |
| mako                       | 16.2 ms                                                                | 16.1 ms: 1.01x faster                                             |
| json_dumps                 | 13.1 ms                                                                | 13.0 ms: 1.01x faster                                             |
| scimark_lu                 | 142 ms                                                                 | 140 ms: 1.01x faster                                              |
| bench_mp_pool              | 95.3 ms                                                                | 94.6 ms: 1.01x faster                                             |
| fannkuch                   | 493 ms                                                                 | 490 ms: 1.01x faster                                              |
| coverage                   | 98.4 ms                                                                | 97.8 ms: 1.01x faster                                             |
| asyncio_websockets         | 519 ms                                                                 | 516 ms: 1.01x faster                                              |
| scimark_sparse_mat_mult    | 5.77 ms                                                                | 5.74 ms: 1.00x faster                                             |
| xml_etree_process          | 70.4 ms                                                                | 70.1 ms: 1.00x faster                                             |
| crypto_pyaes               | 89.4 ms                                                                | 89.1 ms: 1.00x faster                                             |
| hexiom                     | 7.58 ms                                                                | 7.56 ms: 1.00x faster                                             |
| xml_etree_generate         | 97.9 ms                                                                | 97.7 ms: 1.00x faster                                             |
| python_startup             | 15.3 ms                                                                | 15.3 ms: 1.00x faster                                             |
| bpe_tokeniser              | 4.70 sec                                                               | 4.69 sec: 1.00x faster                                            |
| python_startup_no_site     | 9.59 ms                                                                | 9.57 ms: 1.00x faster                                             |
| gc_traversal               | 3.14 ms                                                                | 3.15 ms: 1.00x slower                                             |
| 2to3                       | 310 ms                                                                 | 311 ms: 1.00x slower                                              |
| deepcopy_memo              | 39.0 us                                                                | 39.1 us: 1.00x slower                                             |
| bench_thread_pool          | 3.31 ms                                                                | 3.32 ms: 1.00x slower                                             |
| comprehensions             | 20.3 us                                                                | 20.4 us: 1.00x slower                                             |
| django_template            | 43.3 ms                                                                | 43.5 ms: 1.00x slower                                             |
| unpickle_pure_python       | 256 us                                                                 | 257 us: 1.01x slower                                              |
| pyflate                    | 515 ms                                                                 | 518 ms: 1.01x slower                                              |
| scimark_fft                | 396 ms                                                                 | 398 ms: 1.01x slower                                              |
| go                         | 141 ms                                                                 | 142 ms: 1.01x slower                                              |
| sympy_str                  | 340 ms                                                                 | 342 ms: 1.01x slower                                              |
| sympy_expand               | 557 ms                                                                 | 561 ms: 1.01x slower                                              |
| logging_silent             | 122 ns                                                                 | 123 ns: 1.01x slower                                              |
| raytrace                   | 334 ms                                                                 | 337 ms: 1.01x slower                                              |
| pprint_safe_repr           | 826 ms                                                                 | 833 ms: 1.01x slower                                              |
| docutils                   | 2.83 sec                                                               | 2.85 sec: 1.01x slower                                            |
| typing_runtime_protocols   | 202 us                                                                 | 203 us: 1.01x slower                                              |
| pprint_pformat             | 1.71 sec                                                               | 1.73 sec: 1.01x slower                                            |
| scimark_monte_carlo        | 83.3 ms                                                                | 84.3 ms: 1.01x slower                                             |
| sqlite_synth               | 2.06 us                                                                | 2.08 us: 1.01x slower                                             |
| pycparser                  | 1.19 sec                                                               | 1.21 sec: 1.01x slower                                            |
| genshi_xml                 | 61.5 ms                                                                | 62.5 ms: 1.01x slower                                             |
| regex_effbot               | 2.87 ms                                                                | 2.93 ms: 1.02x slower                                             |
| regex_dna                  | 177 ms                                                                 | 182 ms: 1.03x slower                                              |
| nbody                      | 138 ms                                                                 | 142 ms: 1.03x slower                                              |
| html5lib                   | 70.6 ms                                                                | 72.9 ms: 1.03x slower                                             |
| regex_v8                   | 23.1 ms                                                                | 24.7 ms: 1.07x slower                                             |
| mdp                        | 2.62 sec                                                               | 2.79 sec: 1.07x slower                                            |
| async_tree_cpu_io_mixed    | 550 ms                                                                 | 594 ms: 1.08x slower                                              |
| async_tree_cpu_io_mixed_tg | 518 ms                                                                 | 561 ms: 1.08x slower                                              |
| pidigits                   | 198 ms                                                                 | 224 ms: 1.13x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (40): async_tree_none, sqlglot_optimize, json, regex_compile, async_tree_io, sqlalchemy_imperative, tomli_loads, create_gc_cycles, async_tree_io_tg, pylint, sqlglot_normalize, async_tree_memoization_tg, many_optionals, genshi_text, deepcopy_reduce, deltablue, k_core, async_tree_memoization, xml_etree_parse, dulwich_log, async_tree_none_tg, pickle_pure_python, sqlglot_parse, sympy_integrate, richards_super, sqlalchemy_declarative, chaos, sympy_sum, subparsers, thrift, scimark_sor, shortest_path, json_loads, xml_etree_iterparse, meteor_contest, connected_components, sphinx, pathlib, sqlglot_transpile, deepcopy

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 86.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x