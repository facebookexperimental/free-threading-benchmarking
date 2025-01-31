# Results vs. base

- fork: nascheme
- ref: gh_129201_gc_mark_pr
- machine: linux-x86_64
- commit hash: e12dd2e
- commit date: 2025-01-30
- overall geometric mean: 1.006x slower
- HPT reliability: 99.66%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 302 ms                                                                 | 305 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|-------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines              | 23.5 ms                                                                | 23.1 ms: 1.02x faster                                                    |
| async_tree_io_tg        | 579 ms                                                                 | 574 ms: 1.01x faster                                                     |
| async_tree_io           | 610 ms                                                                 | 606 ms: 1.01x faster                                                     |
| async_generators        | 376 ms                                                                 | 376 ms: 1.00x faster                                                     |
| async_tree_cpu_io_mixed | 529 ms                                                                 | 532 ms: 1.00x slower                                                     |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_memoization_tg, async_tree_none, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 203 ms                                                                 | 191 ms: 1.06x faster                                                     |
| nbody          | 134 ms                                                                 | 131 ms: 1.03x faster                                                     |
| float          | 75.9 ms                                                                | 75.6 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 183 ms                                                                 | 181 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (3): regex_effbot, regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.32 sec                                                               | 2.29 sec: 1.02x faster                                                   |
| xml_etree_process    | 69.1 ms                                                                | 68.5 ms: 1.01x faster                                                    |
| unpickle_pure_python | 246 us                                                                 | 245 us: 1.01x faster                                                     |
| json_dumps           | 12.8 ms                                                                | 12.8 ms: 1.00x faster                                                    |
| json_loads           | 31.2 us                                                                | 31.4 us: 1.01x slower                                                    |
| pickle_pure_python   | 376 us                                                                 | 379 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.6 ms: 1.02x slower                                                    |
| python_startup_no_site | 9.62 ms                                                                | 9.82 ms: 1.02x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml     | 61.5 ms                                                                | 59.6 ms: 1.03x faster                                                    |
| genshi_text    | 28.2 ms                                                                | 27.5 ms: 1.03x faster                                                    |
| mako           | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4+-4ca9fc0 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                 | 203 ms                                                                 | 191 ms: 1.06x faster                                                     |
| mdp                      | 2.76 sec                                                               | 2.65 sec: 1.04x faster                                                   |
| genshi_xml               | 61.5 ms                                                                | 59.6 ms: 1.03x faster                                                    |
| genshi_text              | 28.2 ms                                                                | 27.5 ms: 1.03x faster                                                    |
| nbody                    | 134 ms                                                                 | 131 ms: 1.03x faster                                                     |
| coroutines               | 23.5 ms                                                                | 23.1 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult  | 5.53 ms                                                                | 5.43 ms: 1.02x faster                                                    |
| richards                 | 56.8 ms                                                                | 55.9 ms: 1.02x faster                                                    |
| generators               | 33.7 ms                                                                | 33.1 ms: 1.02x faster                                                    |
| spectral_norm            | 112 ms                                                                 | 110 ms: 1.02x faster                                                     |
| tomli_loads              | 2.32 sec                                                               | 2.29 sec: 1.02x faster                                                   |
| comprehensions           | 20.3 us                                                                | 20.0 us: 1.01x faster                                                    |
| deltablue                | 4.63 ms                                                                | 4.57 ms: 1.01x faster                                                    |
| typing_runtime_protocols | 203 us                                                                 | 201 us: 1.01x faster                                                     |
| thrift                   | 912 us                                                                 | 901 us: 1.01x faster                                                     |
| hexiom                   | 7.38 ms                                                                | 7.30 ms: 1.01x faster                                                    |
| pathlib                  | 18.9 ms                                                                | 18.7 ms: 1.01x faster                                                    |
| meteor_contest           | 131 ms                                                                 | 130 ms: 1.01x faster                                                     |
| async_tree_io_tg         | 579 ms                                                                 | 574 ms: 1.01x faster                                                     |
| regex_dna                | 183 ms                                                                 | 181 ms: 1.01x faster                                                     |
| bpe_tokeniser            | 4.67 sec                                                               | 4.63 sec: 1.01x faster                                                   |
| deepcopy_reduce          | 3.21 us                                                                | 3.18 us: 1.01x faster                                                    |
| xml_etree_process        | 69.1 ms                                                                | 68.5 ms: 1.01x faster                                                    |
| mako                     | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                    |
| connected_components     | 493 ms                                                                 | 489 ms: 1.01x faster                                                     |
| bench_thread_pool        | 3.33 ms                                                                | 3.31 ms: 1.01x faster                                                    |
| coverage                 | 97.4 ms                                                                | 96.7 ms: 1.01x faster                                                    |
| dulwich_log              | 82.7 ms                                                                | 82.1 ms: 1.01x faster                                                    |
| pprint_pformat           | 1.71 sec                                                               | 1.70 sec: 1.01x faster                                                   |
| go                       | 136 ms                                                                 | 135 ms: 1.01x faster                                                     |
| scimark_sor              | 131 ms                                                                 | 130 ms: 1.01x faster                                                     |
| unpickle_pure_python     | 246 us                                                                 | 245 us: 1.01x faster                                                     |
| async_tree_io            | 610 ms                                                                 | 606 ms: 1.01x faster                                                     |
| pycparser                | 1.18 sec                                                               | 1.18 sec: 1.01x faster                                                   |
| scimark_fft              | 380 ms                                                                 | 378 ms: 1.00x faster                                                     |
| float                    | 75.9 ms                                                                | 75.6 ms: 1.00x faster                                                    |
| nqueens                  | 96.7 ms                                                                | 96.3 ms: 1.00x faster                                                    |
| chaos                    | 68.9 ms                                                                | 68.6 ms: 1.00x faster                                                    |
| json_dumps               | 12.8 ms                                                                | 12.8 ms: 1.00x faster                                                    |
| pprint_safe_repr         | 829 ms                                                                 | 826 ms: 1.00x faster                                                     |
| sympy_integrate          | 24.1 ms                                                                | 24.0 ms: 1.00x faster                                                    |
| async_generators         | 376 ms                                                                 | 376 ms: 1.00x faster                                                     |
| crypto_pyaes             | 87.4 ms                                                                | 87.8 ms: 1.00x slower                                                    |
| sympy_sum                | 186 ms                                                                 | 187 ms: 1.00x slower                                                     |
| deepcopy_memo            | 38.1 us                                                                | 38.2 us: 1.00x slower                                                    |
| async_tree_cpu_io_mixed  | 529 ms                                                                 | 532 ms: 1.00x slower                                                     |
| json_loads               | 31.2 us                                                                | 31.4 us: 1.01x slower                                                    |
| pickle_pure_python       | 376 us                                                                 | 379 us: 1.01x slower                                                     |
| json                     | 5.38 ms                                                                | 5.42 ms: 1.01x slower                                                    |
| telco                    | 8.60 ms                                                                | 8.66 ms: 1.01x slower                                                    |
| fannkuch                 | 486 ms                                                                 | 490 ms: 1.01x slower                                                     |
| 2to3                     | 302 ms                                                                 | 305 ms: 1.01x slower                                                     |
| sqlite_synth             | 2.02 us                                                                | 2.04 us: 1.01x slower                                                    |
| subparsers               | 25.5 ms                                                                | 25.9 ms: 1.02x slower                                                    |
| python_startup           | 15.3 ms                                                                | 15.6 ms: 1.02x slower                                                    |
| python_startup_no_site   | 9.62 ms                                                                | 9.82 ms: 1.02x slower                                                    |
| pyflate                  | 491 ms                                                                 | 502 ms: 1.02x slower                                                     |
| scimark_lu               | 134 ms                                                                 | 137 ms: 1.02x slower                                                     |
| create_gc_cycles         | 1.35 ms                                                                | 1.73 ms: 1.28x slower                                                    |
| gc_traversal             | 1.72 ms                                                                | 3.19 ms: 1.85x slower                                                    |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (36): sqlalchemy_imperative, async_tree_none_tg, django_template, logging_format, sqlglot_parse, sphinx, sqlglot_optimize, xml_etree_generate, deepcopy, sqlglot_normalize, pylint, shortest_path, async_tree_memoization_tg, raytrace, async_tree_none, sqlglot_transpile, regex_effbot, xml_etree_parse, docutils, many_optionals, regex_compile, asyncio_websockets, k_core, sympy_str, xml_etree_iterparse, html5lib, regex_v8, richards_super, logging_silent, async_tree_cpu_io_mixed_tg, sqlalchemy_declarative, async_tree_memoization, sympy_expand, logging_simple, scimark_monte_carlo, bench_mp_pool

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 99.66% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x