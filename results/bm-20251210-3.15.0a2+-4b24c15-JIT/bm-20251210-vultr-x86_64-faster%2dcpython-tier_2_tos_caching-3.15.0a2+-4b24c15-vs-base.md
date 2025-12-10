# Results vs. base

- fork: faster-cpython
- ref: tier_2_tos_caching
- machine: linux-x86_64
- commit hash: 4b24c15
- commit date: 2025-12-10
- overall geometric mean: 1.003x faster
- HPT reliability: 55.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2+-4629567 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| html5lib       | 66.1 ms                                                                | 67.8 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2+-4629567 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_generators          | 365 ms                                                                 | 357 ms: 1.02x faster                                                           |
| async_tree_memoization_tg | 306 ms                                                                 | 302 ms: 1.01x faster                                                           |
| coroutines                | 23.9 ms                                                                | 23.7 ms: 1.01x faster                                                          |
| async_tree_io_tg          | 581 ms                                                                 | 587 ms: 1.01x slower                                                           |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                                   |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_io, asyncio_websockets, async_tree_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2+-4629567 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 84.4 ms                                                                | 70.8 ms: 1.19x faster                                                          |
| float          | 60.9 ms                                                                | 58.8 ms: 1.04x faster                                                          |
| pidigits       | 194 ms                                                                 | 191 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2+-4629567 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 124 ms                                                                 | 123 ms: 1.01x faster                                                           |
| regex_v8       | 22.4 ms                                                                | 22.5 ms: 1.01x slower                                                          |
| regex_effbot   | 2.78 ms                                                                | 2.92 ms: 1.05x slower                                                          |
| regex_dna      | 176 ms                                                                 | 186 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2+-4629567 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_pure_python   | 292 us                                                                 | 284 us: 1.03x faster                                                           |
| xml_etree_generate   | 78.7 ms                                                                | 76.8 ms: 1.02x faster                                                          |
| xml_etree_process    | 54.5 ms                                                                | 53.6 ms: 1.02x faster                                                          |
| unpickle_pure_python | 186 us                                                                 | 184 us: 1.01x faster                                                           |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                           |
| json_dumps           | 9.36 ms                                                                | 9.44 ms: 1.01x slower                                                          |
| json_loads           | 28.4 us                                                                | 28.9 us: 1.02x slower                                                          |
| xml_etree_iterparse  | 82.6 ms                                                                | 84.1 ms: 1.02x slower                                                          |
| tomli_loads          | 2.28 sec                                                               | 2.33 sec: 1.02x slower                                                         |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2+-4629567 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 7.36 ms                                                                | 7.35 ms: 1.00x faster                                                          |
| python_startup         | 12.6 ms                                                                | 12.6 ms: 1.00x slower                                                          |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2+-4629567 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako           | 10.4 ms                                                                | 10.5 ms: 1.01x slower                                                          |
| genshi_text    | 20.9 ms                                                                | 21.2 ms: 1.01x slower                                                          |
| genshi_xml     | 53.3 ms                                                                | 55.1 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                 | bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2+-4629567 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody                     | 84.4 ms                                                                | 70.8 ms: 1.19x faster                                                          |
| richards                  | 21.2 ms                                                                | 19.9 ms: 1.07x faster                                                          |
| richards_super            | 25.6 ms                                                                | 24.3 ms: 1.05x faster                                                          |
| logging_format            | 6.72 us                                                                | 6.48 us: 1.04x faster                                                          |
| float                     | 60.9 ms                                                                | 58.8 ms: 1.04x faster                                                          |
| raytrace                  | 267 ms                                                                 | 257 ms: 1.04x faster                                                           |
| pyflate                   | 380 ms                                                                 | 368 ms: 1.03x faster                                                           |
| pickle_pure_python        | 292 us                                                                 | 284 us: 1.03x faster                                                           |
| crypto_pyaes              | 68.2 ms                                                                | 66.4 ms: 1.03x faster                                                          |
| logging_simple            | 5.86 us                                                                | 5.71 us: 1.03x faster                                                          |
| pprint_pformat            | 1.37 sec                                                               | 1.33 sec: 1.03x faster                                                         |
| spectral_norm             | 84.6 ms                                                                | 82.5 ms: 1.03x faster                                                          |
| xml_etree_generate        | 78.7 ms                                                                | 76.8 ms: 1.02x faster                                                          |
| async_generators          | 365 ms                                                                 | 357 ms: 1.02x faster                                                           |
| thrift                    | 747 us                                                                 | 731 us: 1.02x faster                                                           |
| create_gc_cycles          | 1.89 ms                                                                | 1.85 ms: 1.02x faster                                                          |
| go                        | 101 ms                                                                 | 99.5 ms: 1.02x faster                                                          |
| xml_etree_process         | 54.5 ms                                                                | 53.6 ms: 1.02x faster                                                          |
| pathlib                   | 17.8 ms                                                                | 17.5 ms: 1.02x faster                                                          |
| pidigits                  | 194 ms                                                                 | 191 ms: 1.02x faster                                                           |
| generators                | 28.4 ms                                                                | 28.0 ms: 1.02x faster                                                          |
| unpickle_pure_python      | 186 us                                                                 | 184 us: 1.01x faster                                                           |
| regex_compile             | 124 ms                                                                 | 123 ms: 1.01x faster                                                           |
| async_tree_memoization_tg | 306 ms                                                                 | 302 ms: 1.01x faster                                                           |
| telco                     | 161 ms                                                                 | 160 ms: 1.01x faster                                                           |
| shortest_path             | 427 ms                                                                 | 423 ms: 1.01x faster                                                           |
| deltablue                 | 2.84 ms                                                                | 2.82 ms: 1.01x faster                                                          |
| coroutines                | 23.9 ms                                                                | 23.7 ms: 1.01x faster                                                          |
| pycparser                 | 1.11 sec                                                               | 1.11 sec: 1.01x faster                                                         |
| scimark_fft               | 255 ms                                                                 | 253 ms: 1.01x faster                                                           |
| connected_components      | 376 ms                                                                 | 375 ms: 1.00x faster                                                           |
| logging_silent            | 86.6 ns                                                                | 86.3 ns: 1.00x faster                                                          |
| python_startup_no_site    | 7.36 ms                                                                | 7.35 ms: 1.00x faster                                                          |
| python_startup            | 12.6 ms                                                                | 12.6 ms: 1.00x slower                                                          |
| sqlglot_v2_normalize      | 108 ms                                                                 | 109 ms: 1.01x slower                                                           |
| bpe_tokeniser             | 4.00 sec                                                               | 4.02 sec: 1.01x slower                                                         |
| sqlglot_v2_transpile      | 1.50 ms                                                                | 1.51 ms: 1.01x slower                                                          |
| regex_v8                  | 22.4 ms                                                                | 22.5 ms: 1.01x slower                                                          |
| scimark_sor               | 97.7 ms                                                                | 98.4 ms: 1.01x slower                                                          |
| xml_etree_parse           | 129 ms                                                                 | 130 ms: 1.01x slower                                                           |
| mako                      | 10.4 ms                                                                | 10.5 ms: 1.01x slower                                                          |
| json_dumps                | 9.36 ms                                                                | 9.44 ms: 1.01x slower                                                          |
| nqueens                   | 84.4 ms                                                                | 85.2 ms: 1.01x slower                                                          |
| coverage                  | 80.8 ms                                                                | 81.6 ms: 1.01x slower                                                          |
| scimark_lu                | 102 ms                                                                 | 104 ms: 1.01x slower                                                           |
| async_tree_io_tg          | 581 ms                                                                 | 587 ms: 1.01x slower                                                           |
| sympy_expand              | 505 ms                                                                 | 510 ms: 1.01x slower                                                           |
| genshi_text               | 20.9 ms                                                                | 21.2 ms: 1.01x slower                                                          |
| json_loads                | 28.4 us                                                                | 28.9 us: 1.02x slower                                                          |
| sympy_sum                 | 172 ms                                                                 | 174 ms: 1.02x slower                                                           |
| json                      | 5.03 ms                                                                | 5.12 ms: 1.02x slower                                                          |
| sympy_str                 | 308 ms                                                                 | 314 ms: 1.02x slower                                                           |
| xml_etree_iterparse       | 82.6 ms                                                                | 84.1 ms: 1.02x slower                                                          |
| comprehensions            | 15.9 us                                                                | 16.2 us: 1.02x slower                                                          |
| sympy_integrate           | 20.8 ms                                                                | 21.2 ms: 1.02x slower                                                          |
| sqlite_synth              | 2.18 us                                                                | 2.23 us: 1.02x slower                                                          |
| tomli_loads               | 2.28 sec                                                               | 2.33 sec: 1.02x slower                                                         |
| hexiom                    | 6.06 ms                                                                | 6.21 ms: 1.03x slower                                                          |
| html5lib                  | 66.1 ms                                                                | 67.8 ms: 1.03x slower                                                          |
| scimark_sparse_mat_mult   | 4.24 ms                                                                | 4.36 ms: 1.03x slower                                                          |
| genshi_xml                | 53.3 ms                                                                | 55.1 ms: 1.03x slower                                                          |
| regex_effbot              | 2.78 ms                                                                | 2.92 ms: 1.05x slower                                                          |
| regex_dna                 | 176 ms                                                                 | 186 ms: 1.06x slower                                                           |
| gc_traversal              | 4.20 ms                                                                | 4.70 ms: 1.12x slower                                                          |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                                   |

Benchmark hidden because not significant (29): bench_mp_pool, scimark_monte_carlo, django_template, deepcopy, async_tree_cpu_io_mixed, chaos, sphinx, async_tree_cpu_io_mixed_tg, async_tree_none, subparsers, async_tree_io, k_core, bench_thread_pool, 2to3, asyncio_websockets, many_optionals, meteor_contest, sqlglot_v2_optimize, sqlglot_v2_parse, deepcopy_reduce, dulwich_log, mdp, fannkuch, deepcopy_memo, typing_runtime_protocols, async_tree_memoization, pylint, async_tree_none_tg, pprint_safe_repr
Ignored benchmarks (1) of results/bm-20251210-3.15.0a2+-4629567-JIT/bm-20251210-vultr-x86_64-python-46295677a13f141b8d52-3.15.0a2+-4629567.json: docutils

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 55.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x