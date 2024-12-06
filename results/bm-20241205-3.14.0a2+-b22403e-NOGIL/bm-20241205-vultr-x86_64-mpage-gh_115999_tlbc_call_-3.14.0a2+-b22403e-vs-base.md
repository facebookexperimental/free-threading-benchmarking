# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.001x faster
- HPT reliability: 98.62%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 367 ms                                                                 | 366 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 864 ms                                                                 | 842 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 360 ms                                                                 | 352 ms: 1.02x faster                                                  |
| async_tree_memoization     | 478 ms                                                                 | 468 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 623 ms                                                                 | 611 ms: 1.02x faster                                                  |
| async_tree_io_tg           | 832 ms                                                                 | 817 ms: 1.02x faster                                                  |
| async_tree_none            | 390 ms                                                                 | 383 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 450 ms                                                                 | 444 ms: 1.01x faster                                                  |
| async_generators           | 456 ms                                                                 | 451 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 632 ms: 1.01x faster                                                  |
| asyncio_websockets         | 519 ms                                                                 | 522 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                 | 181 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 183 ms                                                                 | 181 ms: 1.02x faster                                                  |
| regex_compile  | 179 ms                                                                 | 181 ms: 1.01x slower                                                  |
| regex_v8       | 24.6 ms                                                                | 25.0 ms: 1.01x slower                                                 |
| regex_effbot   | 2.79 ms                                                                | 2.84 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 332 us                                                                 | 331 us: 1.00x faster                                                  |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.00x slower                                                  |
| json_loads           | 28.4 us                                                                | 28.5 us: 1.00x slower                                                 |
| xml_etree_generate   | 97.3 ms                                                                | 97.9 ms: 1.01x slower                                                 |
| xml_etree_process    | 77.2 ms                                                                | 78.0 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (4): pickle_pure_python, json_dumps, tomli_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.5 ms: 1.00x slower                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 50.9 ms                                                                | 50.3 ms: 1.01x faster                                                 |
| genshi_text     | 31.6 ms                                                                | 31.5 ms: 1.00x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| logging_simple             | 10.9 us                                                                | 10.5 us: 1.03x faster                                                 |
| async_tree_io              | 864 ms                                                                 | 842 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 360 ms                                                                 | 352 ms: 1.02x faster                                                  |
| logging_format             | 12.0 us                                                                | 11.7 us: 1.02x faster                                                 |
| deepcopy_reduce            | 3.62 us                                                                | 3.54 us: 1.02x faster                                                 |
| telco                      | 8.83 ms                                                                | 8.64 ms: 1.02x faster                                                 |
| async_tree_memoization     | 478 ms                                                                 | 468 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 623 ms                                                                 | 611 ms: 1.02x faster                                                  |
| pidigits                   | 184 ms                                                                 | 181 ms: 1.02x faster                                                  |
| async_tree_io_tg           | 832 ms                                                                 | 817 ms: 1.02x faster                                                  |
| logging_silent             | 184 ns                                                                 | 181 ns: 1.02x faster                                                  |
| async_tree_none            | 390 ms                                                                 | 383 ms: 1.02x faster                                                  |
| regex_dna                  | 183 ms                                                                 | 181 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 450 ms                                                                 | 444 ms: 1.01x faster                                                  |
| pprint_pformat             | 2.03 sec                                                               | 2.01 sec: 1.01x faster                                                |
| django_template            | 50.9 ms                                                                | 50.3 ms: 1.01x faster                                                 |
| sqlglot_parse              | 2.61 ms                                                                | 2.58 ms: 1.01x faster                                                 |
| async_generators           | 456 ms                                                                 | 451 ms: 1.01x faster                                                  |
| generators                 | 38.3 ms                                                                | 37.9 ms: 1.01x faster                                                 |
| deltablue                  | 7.94 ms                                                                | 7.86 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 632 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 981 ms                                                                 | 971 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.85 ms                                                                | 1.84 ms: 1.01x faster                                                 |
| scimark_lu                 | 185 ms                                                                 | 184 ms: 1.01x faster                                                  |
| dulwich_log                | 96.1 ms                                                                | 95.4 ms: 1.01x faster                                                 |
| crypto_pyaes               | 91.3 ms                                                                | 90.7 ms: 1.01x faster                                                 |
| sqlalchemy_declarative     | 205 ms                                                                 | 203 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 69.2 ms                                                                | 68.8 ms: 1.01x faster                                                 |
| gc_traversal               | 3.53 ms                                                                | 3.51 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 332 us                                                                 | 331 us: 1.00x faster                                                  |
| genshi_text                | 31.6 ms                                                                | 31.5 ms: 1.00x faster                                                 |
| sympy_expand               | 953 ms                                                                 | 949 ms: 1.00x faster                                                  |
| sympy_str                  | 477 ms                                                                 | 475 ms: 1.00x faster                                                  |
| pycparser                  | 1.53 sec                                                               | 1.53 sec: 1.00x faster                                                |
| go                         | 265 ms                                                                 | 264 ms: 1.00x faster                                                  |
| 2to3                       | 367 ms                                                                 | 366 ms: 1.00x faster                                                  |
| sympy_sum                  | 349 ms                                                                 | 348 ms: 1.00x faster                                                  |
| python_startup             | 17.5 ms                                                                | 17.5 ms: 1.00x slower                                                 |
| comprehensions             | 26.8 us                                                                | 26.9 us: 1.00x slower                                                 |
| xml_etree_parse            | 130 ms                                                                 | 131 ms: 1.00x slower                                                  |
| bpe_tokeniser              | 4.95 sec                                                               | 4.97 sec: 1.00x slower                                                |
| json_loads                 | 28.4 us                                                                | 28.5 us: 1.00x slower                                                 |
| hexiom                     | 9.80 ms                                                                | 9.83 ms: 1.00x slower                                                 |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.00x slower                                                 |
| bench_thread_pool          | 3.34 ms                                                                | 3.36 ms: 1.00x slower                                                 |
| xml_etree_generate         | 97.3 ms                                                                | 97.9 ms: 1.01x slower                                                 |
| asyncio_websockets         | 519 ms                                                                 | 522 ms: 1.01x slower                                                  |
| chaos                      | 103 ms                                                                 | 104 ms: 1.01x slower                                                  |
| pathlib                    | 20.4 ms                                                                | 20.5 ms: 1.01x slower                                                 |
| nqueens                    | 95.8 ms                                                                | 96.7 ms: 1.01x slower                                                 |
| fannkuch                   | 493 ms                                                                 | 497 ms: 1.01x slower                                                  |
| deepcopy_memo              | 40.1 us                                                                | 40.5 us: 1.01x slower                                                 |
| regex_compile              | 179 ms                                                                 | 181 ms: 1.01x slower                                                  |
| xml_etree_process          | 77.2 ms                                                                | 78.0 ms: 1.01x slower                                                 |
| raytrace                   | 543 ms                                                                 | 549 ms: 1.01x slower                                                  |
| json                       | 5.06 ms                                                                | 5.12 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.26 us                                                                | 2.29 us: 1.01x slower                                                 |
| scimark_monte_carlo        | 117 ms                                                                 | 119 ms: 1.01x slower                                                  |
| regex_v8                   | 24.6 ms                                                                | 25.0 ms: 1.01x slower                                                 |
| richards                   | 75.5 ms                                                                | 76.6 ms: 1.01x slower                                                 |
| regex_effbot               | 2.79 ms                                                                | 2.84 ms: 1.02x slower                                                 |
| pyflate                    | 676 ms                                                                 | 695 ms: 1.03x slower                                                  |
| scimark_fft                | 389 ms                                                                 | 405 ms: 1.04x slower                                                  |
| scimark_sparse_mat_mult    | 5.58 ms                                                                | 5.96 ms: 1.07x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (32): sqlalchemy_imperative, typing_runtime_protocols, scimark_sor, pylint, richards_super, sqlglot_normalize, pickle_pure_python, thrift, mdp, json_dumps, html5lib, connected_components, many_optionals, k_core, sympy_integrate, docutils, sphinx, bench_mp_pool, coroutines, meteor_contest, genshi_xml, spectral_norm, deepcopy, coverage, mako, shortest_path, tomli_loads, nbody, float, subparsers, xml_etree_iterparse, sqlglot_transpile

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 98.62% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x