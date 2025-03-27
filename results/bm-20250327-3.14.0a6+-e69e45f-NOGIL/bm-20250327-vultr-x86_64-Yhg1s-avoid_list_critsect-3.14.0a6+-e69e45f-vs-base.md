# Results vs. base

- fork: Yhg1s
- ref: avoid_list_critsect
- machine: linux-x86_64
- commit hash: e69e45f
- commit date: 2025-03-27
- overall geometric mean: 1.002x slower
- HPT reliability: 98.33%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                 | 299 ms: 1.00x faster                                                 |
| html5lib       | 69.9 ms                                                                | 72.2 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines                 | 24.0 ms                                                                | 23.7 ms: 1.01x faster                                                |
| async_generators           | 381 ms                                                                 | 383 ms: 1.00x slower                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                                 | 527 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 495 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (7): async_tree_io, asyncio_websockets, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 207 ms                                                                 | 193 ms: 1.07x faster                                                 |
| float          | 76.9 ms                                                                | 79.1 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                | 21.5 ms: 1.01x faster                                                |
| regex_compile  | 159 ms                                                                 | 159 ms: 1.01x slower                                                 |
| regex_effbot   | 2.77 ms                                                                | 2.86 ms: 1.03x slower                                                |
| regex_dna      | 169 ms                                                                 | 176 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 262 us                                                                 | 258 us: 1.01x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 129 ms: 1.00x faster                                                 |
| pickle_pure_python   | 365 us                                                                 | 363 us: 1.00x faster                                                 |
| json_dumps           | 12.9 ms                                                                | 12.9 ms: 1.00x faster                                                |
| xml_etree_generate   | 97.4 ms                                                                | 97.7 ms: 1.00x slower                                                |
| tomli_loads          | 2.38 sec                                                               | 2.40 sec: 1.01x slower                                               |
| json_loads           | 29.5 us                                                                | 30.8 us: 1.04x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 16.1 ms                                                                | 16.1 ms: 1.01x faster                                                |
| genshi_text     | 28.3 ms                                                                | 28.6 ms: 1.01x slower                                                |
| genshi_xml      | 60.2 ms                                                                | 61.1 ms: 1.01x slower                                                |
| django_template | 43.1 ms                                                                | 44.3 ms: 1.03x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6+-e69e45f |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits                   | 207 ms                                                                 | 193 ms: 1.07x faster                                                 |
| deepcopy_reduce            | 3.25 us                                                                | 3.19 us: 1.02x faster                                                |
| sqlite_synth               | 2.05 us                                                                | 2.01 us: 1.02x faster                                                |
| logging_format             | 8.49 us                                                                | 8.34 us: 1.02x faster                                                |
| logging_simple             | 7.44 us                                                                | 7.32 us: 1.02x faster                                                |
| unpickle_pure_python       | 262 us                                                                 | 258 us: 1.01x faster                                                 |
| nqueens                    | 98.8 ms                                                                | 97.6 ms: 1.01x faster                                                |
| coroutines                 | 24.0 ms                                                                | 23.7 ms: 1.01x faster                                                |
| scimark_lu                 | 145 ms                                                                 | 143 ms: 1.01x faster                                                 |
| logging_silent             | 115 ns                                                                 | 114 ns: 1.01x faster                                                 |
| pathlib                    | 19.9 ms                                                                | 19.7 ms: 1.01x faster                                                |
| sympy_str                  | 338 ms                                                                 | 335 ms: 1.01x faster                                                 |
| crypto_pyaes               | 88.4 ms                                                                | 87.8 ms: 1.01x faster                                                |
| regex_v8                   | 21.6 ms                                                                | 21.5 ms: 1.01x faster                                                |
| deepcopy                   | 315 us                                                                 | 313 us: 1.01x faster                                                 |
| sympy_sum                  | 187 ms                                                                 | 186 ms: 1.01x faster                                                 |
| thrift                     | 874 us                                                                 | 869 us: 1.01x faster                                                 |
| mako                       | 16.1 ms                                                                | 16.1 ms: 1.01x faster                                                |
| scimark_sparse_mat_mult    | 5.66 ms                                                                | 5.64 ms: 1.00x faster                                                |
| xml_etree_parse            | 129 ms                                                                 | 129 ms: 1.00x faster                                                 |
| pickle_pure_python         | 365 us                                                                 | 363 us: 1.00x faster                                                 |
| scimark_monte_carlo        | 84.9 ms                                                                | 84.6 ms: 1.00x faster                                                |
| many_optionals             | 1.18 ms                                                                | 1.18 ms: 1.00x faster                                                |
| json_dumps                 | 12.9 ms                                                                | 12.9 ms: 1.00x faster                                                |
| bench_thread_pool          | 3.17 ms                                                                | 3.16 ms: 1.00x faster                                                |
| fannkuch                   | 499 ms                                                                 | 498 ms: 1.00x faster                                                 |
| comprehensions             | 21.0 us                                                                | 21.0 us: 1.00x faster                                                |
| hexiom                     | 7.72 ms                                                                | 7.71 ms: 1.00x faster                                                |
| 2to3                       | 300 ms                                                                 | 299 ms: 1.00x faster                                                 |
| python_startup             | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                                |
| xml_etree_generate         | 97.4 ms                                                                | 97.7 ms: 1.00x slower                                                |
| gc_traversal               | 1.81 ms                                                                | 1.82 ms: 1.00x slower                                                |
| async_generators           | 381 ms                                                                 | 383 ms: 1.00x slower                                                 |
| deepcopy_memo              | 39.2 us                                                                | 39.4 us: 1.00x slower                                                |
| tomli_loads                | 2.38 sec                                                               | 2.40 sec: 1.01x slower                                               |
| regex_compile              | 159 ms                                                                 | 159 ms: 1.01x slower                                                 |
| spectral_norm              | 114 ms                                                                 | 115 ms: 1.01x slower                                                 |
| deltablue                  | 3.92 ms                                                                | 3.95 ms: 1.01x slower                                                |
| go                         | 146 ms                                                                 | 148 ms: 1.01x slower                                                 |
| genshi_text                | 28.3 ms                                                                | 28.6 ms: 1.01x slower                                                |
| richards_super             | 64.4 ms                                                                | 65.1 ms: 1.01x slower                                                |
| richards                   | 55.6 ms                                                                | 56.2 ms: 1.01x slower                                                |
| genshi_xml                 | 60.2 ms                                                                | 61.1 ms: 1.01x slower                                                |
| async_tree_cpu_io_mixed    | 519 ms                                                                 | 527 ms: 1.02x slower                                                 |
| mdp                        | 2.74 sec                                                               | 2.79 sec: 1.02x slower                                               |
| pprint_safe_repr           | 837 ms                                                                 | 855 ms: 1.02x slower                                                 |
| pprint_pformat             | 1.74 sec                                                               | 1.78 sec: 1.02x slower                                               |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 495 ms: 1.02x slower                                                 |
| django_template            | 43.1 ms                                                                | 44.3 ms: 1.03x slower                                                |
| float                      | 76.9 ms                                                                | 79.1 ms: 1.03x slower                                                |
| html5lib                   | 69.9 ms                                                                | 72.2 ms: 1.03x slower                                                |
| regex_effbot               | 2.77 ms                                                                | 2.86 ms: 1.03x slower                                                |
| regex_dna                  | 169 ms                                                                 | 176 ms: 1.04x slower                                                 |
| json_loads                 | 29.5 us                                                                | 30.8 us: 1.04x slower                                                |
| json                       | 5.07 ms                                                                | 5.32 ms: 1.05x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (41): sqlglot_v2_normalize, xml_etree_iterparse, scimark_sor, meteor_contest, pycparser, async_tree_io, sqlalchemy_imperative, connected_components, sqlalchemy_declarative, scimark_fft, xml_etree_process, sympy_integrate, generators, sqlglot_v2_transpile, typing_runtime_protocols, python_startup_no_site, nbody, sqlglot_v2_optimize, pylint, subparsers, sqlglot_v2_parse, bpe_tokeniser, asyncio_websockets, pyflate, k_core, sympy_expand, raytrace, coverage, async_tree_memoization, chaos, dulwich_log, async_tree_memoization_tg, bench_mp_pool, sphinx, telco, async_tree_none_tg, docutils, async_tree_io_tg, async_tree_none, shortest_path, create_gc_cycles

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 98.33% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x