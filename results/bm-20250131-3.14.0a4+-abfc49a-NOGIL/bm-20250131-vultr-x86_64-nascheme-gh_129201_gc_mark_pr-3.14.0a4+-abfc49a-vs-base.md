# Results vs. base

- fork: nascheme
- ref: gh_129201_gc_mark_pr
- machine: linux-x86_64
- commit hash: abfc49a
- commit date: 2025-01-31
- overall geometric mean: 1.005x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-abfc49a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 2.76 sec                                                               | 2.78 sec: 1.01x slower                                                   |
| html5lib       | 68.4 ms                                                                | 70.2 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-abfc49a |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 579 ms                                                                 | 571 ms: 1.02x faster                                                     |
| async_generators           | 376 ms                                                                 | 374 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 505 ms: 1.01x slower                                                     |
| coroutines                 | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 529 ms                                                                 | 539 ms: 1.02x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (6): async_tree_none_tg, asyncio_websockets, async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-abfc49a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 203 ms                                                                 | 194 ms: 1.04x faster                                                     |
| nbody          | 134 ms                                                                 | 130 ms: 1.03x faster                                                     |
| float          | 75.9 ms                                                                | 75.2 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-abfc49a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 149 ms                                                                 | 148 ms: 1.01x faster                                                     |
| regex_dna      | 183 ms                                                                 | 181 ms: 1.01x faster                                                     |
| regex_v8       | 23.1 ms                                                                | 23.6 ms: 1.02x slower                                                    |
| regex_effbot   | 2.74 ms                                                                | 2.81 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-abfc49a |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.32 sec                                                               | 2.27 sec: 1.02x faster                                                   |
| unpickle_pure_python | 246 us                                                                 | 242 us: 1.02x faster                                                     |
| pickle_pure_python   | 376 us                                                                 | 371 us: 1.01x faster                                                     |
| xml_etree_process    | 69.1 ms                                                                | 68.8 ms: 1.00x faster                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (5): xml_etree_generate, json_dumps, json_loads, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-abfc49a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup | 15.3 ms                                                                | 15.3 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-abfc49a |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 61.5 ms                                                                | 59.9 ms: 1.03x faster                                                    |
| genshi_text     | 28.2 ms                                                                | 27.6 ms: 1.02x faster                                                    |
| django_template | 43.2 ms                                                                | 42.4 ms: 1.02x faster                                                    |
| mako            | 15.9 ms                                                                | 15.6 ms: 1.02x faster                                                    |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-abfc49a |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| spectral_norm              | 112 ms                                                                 | 107 ms: 1.05x faster                                                     |
| pidigits                   | 203 ms                                                                 | 194 ms: 1.04x faster                                                     |
| nbody                      | 134 ms                                                                 | 130 ms: 1.03x faster                                                     |
| typing_runtime_protocols   | 203 us                                                                 | 197 us: 1.03x faster                                                     |
| genshi_xml                 | 61.5 ms                                                                | 59.9 ms: 1.03x faster                                                    |
| comprehensions             | 20.3 us                                                                | 19.8 us: 1.02x faster                                                    |
| genshi_text                | 28.2 ms                                                                | 27.6 ms: 1.02x faster                                                    |
| tomli_loads                | 2.32 sec                                                               | 2.27 sec: 1.02x faster                                                   |
| django_template            | 43.2 ms                                                                | 42.4 ms: 1.02x faster                                                    |
| hexiom                     | 7.38 ms                                                                | 7.25 ms: 1.02x faster                                                    |
| raytrace                   | 325 ms                                                                 | 319 ms: 1.02x faster                                                     |
| scimark_sparse_mat_mult    | 5.53 ms                                                                | 5.44 ms: 1.02x faster                                                    |
| mako                       | 15.9 ms                                                                | 15.6 ms: 1.02x faster                                                    |
| nqueens                    | 96.7 ms                                                                | 95.2 ms: 1.02x faster                                                    |
| async_tree_io_tg           | 579 ms                                                                 | 571 ms: 1.02x faster                                                     |
| generators                 | 33.7 ms                                                                | 33.1 ms: 1.02x faster                                                    |
| unpickle_pure_python       | 246 us                                                                 | 242 us: 1.02x faster                                                     |
| pickle_pure_python         | 376 us                                                                 | 371 us: 1.01x faster                                                     |
| go                         | 136 ms                                                                 | 134 ms: 1.01x faster                                                     |
| pprint_pformat             | 1.71 sec                                                               | 1.69 sec: 1.01x faster                                                   |
| pprint_safe_repr           | 829 ms                                                                 | 817 ms: 1.01x faster                                                     |
| pyflate                    | 491 ms                                                                 | 485 ms: 1.01x faster                                                     |
| chaos                      | 68.9 ms                                                                | 68.1 ms: 1.01x faster                                                    |
| deltablue                  | 4.63 ms                                                                | 4.57 ms: 1.01x faster                                                    |
| dulwich_log                | 82.7 ms                                                                | 81.7 ms: 1.01x faster                                                    |
| thrift                     | 912 us                                                                 | 901 us: 1.01x faster                                                     |
| bench_thread_pool          | 3.33 ms                                                                | 3.29 ms: 1.01x faster                                                    |
| float                      | 75.9 ms                                                                | 75.2 ms: 1.01x faster                                                    |
| connected_components       | 493 ms                                                                 | 488 ms: 1.01x faster                                                     |
| fannkuch                   | 486 ms                                                                 | 481 ms: 1.01x faster                                                     |
| regex_compile              | 149 ms                                                                 | 148 ms: 1.01x faster                                                     |
| regex_dna                  | 183 ms                                                                 | 181 ms: 1.01x faster                                                     |
| bpe_tokeniser              | 4.67 sec                                                               | 4.63 sec: 1.01x faster                                                   |
| many_optionals             | 1.18 ms                                                                | 1.17 ms: 1.01x faster                                                    |
| coverage                   | 97.4 ms                                                                | 96.7 ms: 1.01x faster                                                    |
| sqlglot_parse              | 1.57 ms                                                                | 1.56 ms: 1.01x faster                                                    |
| shortest_path              | 546 ms                                                                 | 542 ms: 1.01x faster                                                     |
| sqlglot_optimize           | 61.2 ms                                                                | 60.8 ms: 1.01x faster                                                    |
| async_generators           | 376 ms                                                                 | 374 ms: 1.01x faster                                                     |
| pathlib                    | 18.9 ms                                                                | 18.9 ms: 1.00x faster                                                    |
| xml_etree_process          | 69.1 ms                                                                | 68.8 ms: 1.00x faster                                                    |
| deepcopy                   | 313 us                                                                 | 312 us: 1.00x faster                                                     |
| mdp                        | 2.76 sec                                                               | 2.76 sec: 1.00x faster                                                   |
| python_startup             | 15.3 ms                                                                | 15.3 ms: 1.00x faster                                                    |
| scimark_lu                 | 134 ms                                                                 | 135 ms: 1.01x slower                                                     |
| docutils                   | 2.76 sec                                                               | 2.78 sec: 1.01x slower                                                   |
| deepcopy_reduce            | 3.21 us                                                                | 3.24 us: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 505 ms: 1.01x slower                                                     |
| coroutines                 | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.02 us                                                                | 2.04 us: 1.01x slower                                                    |
| crypto_pyaes               | 87.4 ms                                                                | 88.4 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 529 ms                                                                 | 539 ms: 1.02x slower                                                     |
| create_gc_cycles           | 1.35 ms                                                                | 1.38 ms: 1.02x slower                                                    |
| logging_simple             | 7.21 us                                                                | 7.36 us: 1.02x slower                                                    |
| regex_v8                   | 23.1 ms                                                                | 23.6 ms: 1.02x slower                                                    |
| regex_effbot               | 2.74 ms                                                                | 2.81 ms: 1.03x slower                                                    |
| html5lib                   | 68.4 ms                                                                | 70.2 ms: 1.03x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (39): meteor_contest, sqlglot_transpile, pycparser, async_tree_none_tg, subparsers, asyncio_websockets, telco, async_tree_memoization, sqlalchemy_imperative, logging_format, sqlglot_normalize, richards_super, xml_etree_generate, async_tree_io, deepcopy_memo, python_startup_no_site, async_tree_memoization_tg, 2to3, scimark_monte_carlo, bench_mp_pool, json_dumps, scimark_fft, sqlalchemy_declarative, pylint, json_loads, json, xml_etree_parse, k_core, sympy_integrate, sympy_str, scimark_sor, sympy_sum, sympy_expand, async_tree_none, sphinx, gc_traversal, richards, xml_etree_iterparse, logging_silent

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x