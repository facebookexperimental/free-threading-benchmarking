# Results vs. base

- fork: colesbury
- ref: gh_127582_resurrecti
- machine: linux-x86_64
- commit hash: a7b41c8
- commit date: 2024-12-04
- overall geometric mean: 1.000x slower
- HPT reliability: 80.74%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2+-6bc3e83 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|---------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators          | 460 ms                                                                 | 447 ms: 1.03x faster                                                      |
| async_tree_io             | 849 ms                                                                 | 853 ms: 1.00x slower                                                      |
| async_tree_memoization_tg | 447 ms                                                                 | 450 ms: 1.01x slower                                                      |
| async_tree_io_tg          | 824 ms                                                                 | 831 ms: 1.01x slower                                                      |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed_tg, async_tree_none_tg, asyncio_websockets, coroutines, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2+-6bc3e83 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 139 ms                                                                 | 137 ms: 1.01x faster                                                      |
| nbody          | 130 ms                                                                 | 133 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2+-6bc3e83 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 24.6 ms                                                                | 23.9 ms: 1.03x faster                                                     |
| regex_effbot   | 2.83 ms                                                                | 2.84 ms: 1.00x slower                                                     |
| regex_dna      | 184 ms                                                                 | 185 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2+-6bc3e83 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 14.4 ms                                                                | 14.2 ms: 1.02x faster                                                     |
| pickle_pure_python   | 520 us                                                                 | 510 us: 1.02x faster                                                      |
| xml_etree_generate   | 97.5 ms                                                                | 97.3 ms: 1.00x faster                                                     |
| tomli_loads          | 2.64 sec                                                               | 2.66 sec: 1.01x slower                                                    |
| unpickle_pure_python | 331 us                                                                 | 333 us: 1.01x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (4): xml_etree_process, xml_etree_parse, json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2+-6bc3e83 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 10.2 ms                                                                | 10.2 ms: 1.00x faster                                                     |
| python_startup         | 17.4 ms                                                                | 17.4 ms: 1.00x faster                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2+-6bc3e83 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 32.0 ms                                                                | 31.6 ms: 1.01x faster                                                     |
| genshi_xml      | 63.0 ms                                                                | 63.8 ms: 1.01x slower                                                     |
| django_template | 51.2 ms                                                                | 51.9 ms: 1.01x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                 | bm-20241204-vultr-x86_64-python-6bc3e830a518112a4e24-3.14.0a2+-6bc3e83 | bm-20241204-vultr-x86_64-colesbury-gh_127582_resurrecti-3.14.0a2+-a7b41c8 |
|---------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| logging_silent            | 190 ns                                                                 | 183 ns: 1.04x faster                                                      |
| deltablue                 | 8.13 ms                                                                | 7.85 ms: 1.04x faster                                                     |
| async_generators          | 460 ms                                                                 | 447 ms: 1.03x faster                                                      |
| regex_v8                  | 24.6 ms                                                                | 23.9 ms: 1.03x faster                                                     |
| raytrace                  | 561 ms                                                                 | 547 ms: 1.03x faster                                                      |
| pyflate                   | 697 ms                                                                 | 681 ms: 1.02x faster                                                      |
| json_dumps                | 14.4 ms                                                                | 14.2 ms: 1.02x faster                                                     |
| pickle_pure_python        | 520 us                                                                 | 510 us: 1.02x faster                                                      |
| coverage                  | 101 ms                                                                 | 99.5 ms: 1.02x faster                                                     |
| sqlite_synth              | 2.31 us                                                                | 2.27 us: 1.02x faster                                                     |
| deepcopy_reduce           | 3.55 us                                                                | 3.50 us: 1.01x faster                                                     |
| float                     | 139 ms                                                                 | 137 ms: 1.01x faster                                                      |
| comprehensions            | 27.4 us                                                                | 27.0 us: 1.01x faster                                                     |
| genshi_text               | 32.0 ms                                                                | 31.6 ms: 1.01x faster                                                     |
| generators                | 38.4 ms                                                                | 37.9 ms: 1.01x faster                                                     |
| go                        | 273 ms                                                                 | 269 ms: 1.01x faster                                                      |
| subparsers                | 31.8 ms                                                                | 31.5 ms: 1.01x faster                                                     |
| create_gc_cycles          | 1.80 ms                                                                | 1.79 ms: 1.01x faster                                                     |
| hexiom                    | 9.82 ms                                                                | 9.75 ms: 1.01x faster                                                     |
| richards_super            | 87.2 ms                                                                | 86.7 ms: 1.01x faster                                                     |
| bench_thread_pool         | 3.38 ms                                                                | 3.36 ms: 1.01x faster                                                     |
| fannkuch                  | 497 ms                                                                 | 495 ms: 1.00x faster                                                      |
| python_startup_no_site    | 10.2 ms                                                                | 10.2 ms: 1.00x faster                                                     |
| xml_etree_generate        | 97.5 ms                                                                | 97.3 ms: 1.00x faster                                                     |
| python_startup            | 17.4 ms                                                                | 17.4 ms: 1.00x faster                                                     |
| sqlalchemy_declarative    | 204 ms                                                                 | 204 ms: 1.00x slower                                                      |
| regex_effbot              | 2.83 ms                                                                | 2.84 ms: 1.00x slower                                                     |
| sympy_sum                 | 349 ms                                                                 | 350 ms: 1.00x slower                                                      |
| async_tree_io             | 849 ms                                                                 | 853 ms: 1.00x slower                                                      |
| deepcopy                  | 329 us                                                                 | 331 us: 1.00x slower                                                      |
| scimark_lu                | 182 ms                                                                 | 183 ms: 1.01x slower                                                      |
| dulwich_log               | 95.4 ms                                                                | 96.0 ms: 1.01x slower                                                     |
| regex_dna                 | 184 ms                                                                 | 185 ms: 1.01x slower                                                      |
| sympy_str                 | 475 ms                                                                 | 478 ms: 1.01x slower                                                      |
| crypto_pyaes              | 91.3 ms                                                                | 91.9 ms: 1.01x slower                                                     |
| k_core                    | 2.40 sec                                                               | 2.42 sec: 1.01x slower                                                    |
| async_tree_memoization_tg | 447 ms                                                                 | 450 ms: 1.01x slower                                                      |
| tomli_loads               | 2.64 sec                                                               | 2.66 sec: 1.01x slower                                                    |
| unpickle_pure_python      | 331 us                                                                 | 333 us: 1.01x slower                                                      |
| deepcopy_memo             | 39.7 us                                                                | 40.0 us: 1.01x slower                                                     |
| scimark_fft               | 398 ms                                                                 | 402 ms: 1.01x slower                                                      |
| async_tree_io_tg          | 824 ms                                                                 | 831 ms: 1.01x slower                                                      |
| pprint_pformat            | 2.02 sec                                                               | 2.04 sec: 1.01x slower                                                    |
| json                      | 5.05 ms                                                                | 5.11 ms: 1.01x slower                                                     |
| genshi_xml                | 63.0 ms                                                                | 63.8 ms: 1.01x slower                                                     |
| django_template           | 51.2 ms                                                                | 51.9 ms: 1.01x slower                                                     |
| pprint_safe_repr          | 973 ms                                                                 | 985 ms: 1.01x slower                                                      |
| bpe_tokeniser             | 4.98 sec                                                               | 5.04 sec: 1.01x slower                                                    |
| typing_runtime_protocols  | 201 us                                                                 | 204 us: 1.01x slower                                                      |
| spectral_norm             | 121 ms                                                                 | 123 ms: 1.02x slower                                                      |
| nbody                     | 130 ms                                                                 | 133 ms: 1.02x slower                                                      |
| mdp                       | 2.83 sec                                                               | 2.90 sec: 1.02x slower                                                    |
| gc_traversal              | 3.17 ms                                                                | 3.26 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult   | 5.58 ms                                                                | 5.91 ms: 1.06x slower                                                     |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (42): sqlglot_parse, sqlglot_transpile, pylint, richards, docutils, async_tree_cpu_io_mixed_tg, sqlglot_optimize, bench_mp_pool, async_tree_none_tg, regex_compile, asyncio_websockets, nqueens, sqlglot_normalize, meteor_contest, sympy_integrate, pidigits, sqlalchemy_imperative, 2to3, coroutines, xml_etree_process, chaos, sympy_expand, xml_etree_parse, shortest_path, async_tree_memoization, async_tree_cpu_io_mixed, html5lib, mako, scimark_sor, logging_simple, async_tree_none, sphinx, connected_components, json_loads, xml_etree_iterparse, logging_format, pycparser, scimark_monte_carlo, many_optionals, telco, pathlib, thrift

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 80.74% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x