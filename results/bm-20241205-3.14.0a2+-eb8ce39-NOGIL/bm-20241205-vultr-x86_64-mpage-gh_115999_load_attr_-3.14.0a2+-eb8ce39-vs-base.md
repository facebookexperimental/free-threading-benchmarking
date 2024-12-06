# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: eb8ce39
- commit date: 2024-12-05
- overall geometric mean: 1.013x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 367 ms                                                                 | 361 ms: 1.02x faster                                                  |
| html5lib       | 97.1 ms                                                                | 98.7 ms: 1.02x slower                                                 |
| sphinx         | 1.18 sec                                                               | 1.17 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 864 ms                                                                 | 811 ms: 1.07x faster                                                  |
| async_tree_io_tg           | 832 ms                                                                 | 786 ms: 1.06x faster                                                  |
| async_tree_memoization     | 478 ms                                                                 | 453 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 360 ms                                                                 | 345 ms: 1.04x faster                                                  |
| async_tree_none            | 390 ms                                                                 | 374 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 450 ms                                                                 | 432 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 623 ms                                                                 | 610 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 626 ms: 1.02x faster                                                  |
| async_generators           | 456 ms                                                                 | 453 ms: 1.01x faster                                                  |
| coroutines                 | 24.3 ms                                                                | 25.1 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 131 ms                                                                 | 125 ms: 1.05x faster                                                  |
| float          | 138 ms                                                                 | 137 ms: 1.01x faster                                                  |
| pidigits       | 184 ms                                                                 | 184 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.6 ms                                                                | 24.2 ms: 1.02x faster                                                 |
| regex_dna      | 183 ms                                                                 | 184 ms: 1.00x slower                                                  |
| regex_effbot   | 2.79 ms                                                                | 2.81 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 14.4 ms                                                                | 14.3 ms: 1.01x faster                                                 |
| tomli_loads          | 2.66 sec                                                               | 2.64 sec: 1.01x faster                                                |
| unpickle_pure_python | 332 us                                                                 | 331 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 90.9 ms                                                                | 91.5 ms: 1.01x slower                                                 |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                  |
| json_loads           | 28.4 us                                                                | 28.8 us: 1.01x slower                                                 |
| xml_etree_process    | 77.2 ms                                                                | 78.5 ms: 1.02x slower                                                 |
| pickle_pure_python   | 505 us                                                                 | 518 us: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.1 ms: 1.02x faster                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 17.6 ms                                                                | 16.8 ms: 1.05x faster                                                 |
| genshi_text     | 31.6 ms                                                                | 30.4 ms: 1.04x faster                                                 |
| django_template | 50.9 ms                                                                | 50.2 ms: 1.01x faster                                                 |
| genshi_xml      | 63.3 ms                                                                | 62.7 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| logging_simple             | 10.9 us                                                                | 9.82 us: 1.11x faster                                                 |
| logging_format             | 12.0 us                                                                | 10.9 us: 1.10x faster                                                 |
| gc_traversal               | 3.53 ms                                                                | 3.29 ms: 1.07x faster                                                 |
| async_tree_io              | 864 ms                                                                 | 811 ms: 1.07x faster                                                  |
| async_tree_io_tg           | 832 ms                                                                 | 786 ms: 1.06x faster                                                  |
| async_tree_memoization     | 478 ms                                                                 | 453 ms: 1.05x faster                                                  |
| thrift                     | 1.17 ms                                                                | 1.11 ms: 1.05x faster                                                 |
| deepcopy_reduce            | 3.62 us                                                                | 3.44 us: 1.05x faster                                                 |
| nbody                      | 131 ms                                                                 | 125 ms: 1.05x faster                                                  |
| mako                       | 17.6 ms                                                                | 16.8 ms: 1.05x faster                                                 |
| async_tree_none_tg         | 360 ms                                                                 | 345 ms: 1.04x faster                                                  |
| async_tree_none            | 390 ms                                                                 | 374 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 450 ms                                                                 | 432 ms: 1.04x faster                                                  |
| genshi_text                | 31.6 ms                                                                | 30.4 ms: 1.04x faster                                                 |
| sqlglot_optimize           | 69.2 ms                                                                | 66.8 ms: 1.04x faster                                                 |
| pylint                     | 382 ms                                                                 | 370 ms: 1.03x faster                                                  |
| many_optionals             | 1.30 ms                                                                | 1.26 ms: 1.03x faster                                                 |
| sqlalchemy_imperative      | 29.7 ms                                                                | 28.8 ms: 1.03x faster                                                 |
| telco                      | 8.83 ms                                                                | 8.59 ms: 1.03x faster                                                 |
| sqlglot_parse              | 2.61 ms                                                                | 2.54 ms: 1.03x faster                                                 |
| subparsers                 | 31.7 ms                                                                | 30.9 ms: 1.02x faster                                                 |
| create_gc_cycles           | 1.85 ms                                                                | 1.81 ms: 1.02x faster                                                 |
| pprint_safe_repr           | 981 ms                                                                 | 959 ms: 1.02x faster                                                  |
| spectral_norm              | 122 ms                                                                 | 119 ms: 1.02x faster                                                  |
| pprint_pformat             | 2.03 sec                                                               | 1.99 sec: 1.02x faster                                                |
| async_tree_cpu_io_mixed_tg | 623 ms                                                                 | 610 ms: 1.02x faster                                                  |
| deepcopy                   | 327 us                                                                 | 320 us: 1.02x faster                                                  |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 626 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.26 us                                                                | 2.22 us: 1.02x faster                                                 |
| python_startup             | 17.5 ms                                                                | 17.1 ms: 1.02x faster                                                 |
| sqlalchemy_declarative     | 205 ms                                                                 | 201 ms: 1.02x faster                                                  |
| regex_v8                   | 24.6 ms                                                                | 24.2 ms: 1.02x faster                                                 |
| scimark_lu                 | 185 ms                                                                 | 182 ms: 1.02x faster                                                  |
| 2to3                       | 367 ms                                                                 | 361 ms: 1.02x faster                                                  |
| deepcopy_memo              | 40.1 us                                                                | 39.5 us: 1.01x faster                                                 |
| django_template            | 50.9 ms                                                                | 50.2 ms: 1.01x faster                                                 |
| sqlglot_transpile          | 2.97 ms                                                                | 2.93 ms: 1.01x faster                                                 |
| sphinx                     | 1.18 sec                                                               | 1.17 sec: 1.01x faster                                                |
| pathlib                    | 20.4 ms                                                                | 20.1 ms: 1.01x faster                                                 |
| mdp                        | 2.77 sec                                                               | 2.74 sec: 1.01x faster                                                |
| dulwich_log                | 96.1 ms                                                                | 95.0 ms: 1.01x faster                                                 |
| scimark_sor                | 235 ms                                                                 | 233 ms: 1.01x faster                                                  |
| sqlglot_normalize          | 137 ms                                                                 | 136 ms: 1.01x faster                                                  |
| bench_mp_pool              | 109 ms                                                                 | 108 ms: 1.01x faster                                                  |
| genshi_xml                 | 63.3 ms                                                                | 62.7 ms: 1.01x faster                                                 |
| meteor_contest             | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| json_dumps                 | 14.4 ms                                                                | 14.3 ms: 1.01x faster                                                 |
| async_generators           | 456 ms                                                                 | 453 ms: 1.01x faster                                                  |
| bench_thread_pool          | 3.34 ms                                                                | 3.32 ms: 1.01x faster                                                 |
| float                      | 138 ms                                                                 | 137 ms: 1.01x faster                                                  |
| chaos                      | 103 ms                                                                 | 103 ms: 1.01x faster                                                  |
| tomli_loads                | 2.66 sec                                                               | 2.64 sec: 1.01x faster                                                |
| sympy_str                  | 477 ms                                                                 | 474 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 332 us                                                                 | 331 us: 1.01x faster                                                  |
| sympy_integrate            | 29.4 ms                                                                | 29.3 ms: 1.00x faster                                                 |
| fannkuch                   | 493 ms                                                                 | 491 ms: 1.00x faster                                                  |
| sympy_sum                  | 349 ms                                                                 | 348 ms: 1.00x faster                                                  |
| python_startup_no_site     | 10.3 ms                                                                | 10.2 ms: 1.00x faster                                                 |
| hexiom                     | 9.80 ms                                                                | 9.78 ms: 1.00x faster                                                 |
| pidigits                   | 184 ms                                                                 | 184 ms: 1.00x faster                                                  |
| regex_dna                  | 183 ms                                                                 | 184 ms: 1.00x slower                                                  |
| crypto_pyaes               | 91.3 ms                                                                | 91.6 ms: 1.00x slower                                                 |
| go                         | 265 ms                                                                 | 266 ms: 1.00x slower                                                  |
| regex_effbot               | 2.79 ms                                                                | 2.81 ms: 1.01x slower                                                 |
| xml_etree_iterparse        | 90.9 ms                                                                | 91.5 ms: 1.01x slower                                                 |
| xml_etree_parse            | 130 ms                                                                 | 131 ms: 1.01x slower                                                  |
| nqueens                    | 95.8 ms                                                                | 96.5 ms: 1.01x slower                                                 |
| richards                   | 75.5 ms                                                                | 76.1 ms: 1.01x slower                                                 |
| bpe_tokeniser              | 4.95 sec                                                               | 5.00 sec: 1.01x slower                                                |
| raytrace                   | 543 ms                                                                 | 551 ms: 1.01x slower                                                  |
| json_loads                 | 28.4 us                                                                | 28.8 us: 1.01x slower                                                 |
| scimark_monte_carlo        | 117 ms                                                                 | 119 ms: 1.01x slower                                                  |
| html5lib                   | 97.1 ms                                                                | 98.7 ms: 1.02x slower                                                 |
| xml_etree_process          | 77.2 ms                                                                | 78.5 ms: 1.02x slower                                                 |
| deltablue                  | 7.94 ms                                                                | 8.08 ms: 1.02x slower                                                 |
| pyflate                    | 676 ms                                                                 | 690 ms: 1.02x slower                                                  |
| pickle_pure_python         | 505 us                                                                 | 518 us: 1.03x slower                                                  |
| comprehensions             | 26.8 us                                                                | 27.5 us: 1.03x slower                                                 |
| coroutines                 | 24.3 ms                                                                | 25.1 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (17): richards_super, generators, pycparser, asyncio_websockets, connected_components, shortest_path, logging_silent, sympy_expand, docutils, k_core, scimark_sparse_mat_mult, regex_compile, json, xml_etree_generate, scimark_fft, coverage, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x