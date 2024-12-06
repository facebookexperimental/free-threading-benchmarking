# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.004x faster
- HPT reliability: 86.70%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 258 ms: 1.00x slower                                                  |
| sphinx         | 994 ms                                                                 | 1.00 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 498 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 483 ms: 1.22x faster                                                  |
| async_generators           | 370 ms                                                                 | 368 ms: 1.01x faster                                                  |
| coroutines                 | 21.9 ms                                                                | 22.3 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_io, async_tree_memoization, asyncio_websockets, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 185 ms: 1.20x faster                                                  |
| nbody          | 95.2 ms                                                                | 94.5 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 169 ms                                                                 | 168 ms: 1.01x faster                                                  |
| regex_v8       | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                 |
| regex_effbot   | 2.74 ms                                                                | 2.81 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps          | 11.5 ms                                                                | 11.3 ms: 1.02x faster                                                 |
| pickle_pure_python  | 316 us                                                                 | 313 us: 1.01x faster                                                  |
| xml_etree_parse     | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| xml_etree_iterparse | 92.1 ms                                                                | 91.9 ms: 1.00x faster                                                 |
| xml_etree_process   | 59.6 ms                                                                | 60.0 ms: 1.01x slower                                                 |
| xml_etree_generate  | 85.1 ms                                                                | 86.9 ms: 1.02x slower                                                 |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): unpickle_pure_python, json_loads, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                 |
| python_startup_no_site | 7.43 ms                                                                | 7.47 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml     | 51.2 ms                                                                | 50.5 ms: 1.01x faster                                                 |
| genshi_text    | 22.3 ms                                                                | 22.0 ms: 1.01x faster                                                 |
| mako           | 11.5 ms                                                                | 11.7 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 498 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 483 ms: 1.22x faster                                                  |
| pidigits                   | 222 ms                                                                 | 185 ms: 1.20x faster                                                  |
| gc_traversal               | 4.58 ms                                                                | 4.29 ms: 1.07x faster                                                 |
| crypto_pyaes               | 68.1 ms                                                                | 66.3 ms: 1.03x faster                                                 |
| chaos                      | 60.1 ms                                                                | 58.7 ms: 1.02x faster                                                 |
| logging_simple             | 6.27 us                                                                | 6.15 us: 1.02x faster                                                 |
| sqlalchemy_imperative      | 19.4 ms                                                                | 19.0 ms: 1.02x faster                                                 |
| json_dumps                 | 11.5 ms                                                                | 11.3 ms: 1.02x faster                                                 |
| genshi_xml                 | 51.2 ms                                                                | 50.5 ms: 1.01x faster                                                 |
| genshi_text                | 22.3 ms                                                                | 22.0 ms: 1.01x faster                                                 |
| sqlite_synth               | 2.28 us                                                                | 2.25 us: 1.01x faster                                                 |
| pickle_pure_python         | 316 us                                                                 | 313 us: 1.01x faster                                                  |
| logging_format             | 7.04 us                                                                | 6.99 us: 1.01x faster                                                 |
| nbody                      | 95.2 ms                                                                | 94.5 ms: 1.01x faster                                                 |
| scimark_fft                | 340 ms                                                                 | 337 ms: 1.01x faster                                                  |
| sqlglot_parse              | 1.30 ms                                                                | 1.29 ms: 1.01x faster                                                 |
| regex_dna                  | 169 ms                                                                 | 168 ms: 1.01x faster                                                  |
| go                         | 120 ms                                                                 | 119 ms: 1.01x faster                                                  |
| async_generators           | 370 ms                                                                 | 368 ms: 1.01x faster                                                  |
| xml_etree_parse            | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| coverage                   | 79.8 ms                                                                | 79.5 ms: 1.00x faster                                                 |
| hexiom                     | 5.99 ms                                                                | 5.98 ms: 1.00x faster                                                 |
| xml_etree_iterparse        | 92.1 ms                                                                | 91.9 ms: 1.00x faster                                                 |
| sympy_integrate            | 20.1 ms                                                                | 20.1 ms: 1.00x slower                                                 |
| raytrace                   | 265 ms                                                                 | 266 ms: 1.00x slower                                                  |
| sqlalchemy_declarative     | 127 ms                                                                 | 127 ms: 1.00x slower                                                  |
| 2to3                       | 257 ms                                                                 | 258 ms: 1.00x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 155 ms: 1.00x slower                                                  |
| sqlglot_normalize          | 107 ms                                                                 | 108 ms: 1.00x slower                                                  |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                 |
| python_startup_no_site     | 7.43 ms                                                                | 7.47 ms: 1.00x slower                                                 |
| deltablue                  | 3.25 ms                                                                | 3.27 ms: 1.01x slower                                                 |
| sqlglot_optimize           | 53.6 ms                                                                | 53.9 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.45 sec                                                               | 1.46 sec: 1.01x slower                                                |
| bench_thread_pool          | 1.02 ms                                                                | 1.02 ms: 1.01x slower                                                 |
| deepcopy_memo              | 30.7 us                                                                | 30.9 us: 1.01x slower                                                 |
| sphinx                     | 994 ms                                                                 | 1.00 sec: 1.01x slower                                                |
| bpe_tokeniser              | 4.32 sec                                                               | 4.35 sec: 1.01x slower                                                |
| xml_etree_process          | 59.6 ms                                                                | 60.0 ms: 1.01x slower                                                 |
| scimark_sor                | 133 ms                                                                 | 134 ms: 1.01x slower                                                  |
| subparsers                 | 22.1 ms                                                                | 22.3 ms: 1.01x slower                                                 |
| sympy_expand               | 460 ms                                                                 | 465 ms: 1.01x slower                                                  |
| json                       | 4.53 ms                                                                | 4.58 ms: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 4.57 ms                                                                | 4.62 ms: 1.01x slower                                                 |
| connected_components       | 400 ms                                                                 | 405 ms: 1.01x slower                                                  |
| logging_silent             | 105 ns                                                                 | 107 ns: 1.01x slower                                                  |
| comprehensions             | 17.3 us                                                                | 17.6 us: 1.01x slower                                                 |
| create_gc_cycles           | 1.83 ms                                                                | 1.85 ms: 1.01x slower                                                 |
| mako                       | 11.5 ms                                                                | 11.7 ms: 1.02x slower                                                 |
| coroutines                 | 21.9 ms                                                                | 22.3 ms: 1.02x slower                                                 |
| regex_v8                   | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                 |
| nqueens                    | 79.5 ms                                                                | 81.0 ms: 1.02x slower                                                 |
| deepcopy_reduce            | 2.60 us                                                                | 2.65 us: 1.02x slower                                                 |
| xml_etree_generate         | 85.1 ms                                                                | 86.9 ms: 1.02x slower                                                 |
| telco                      | 7.19 ms                                                                | 7.34 ms: 1.02x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 385 ms: 1.02x slower                                                  |
| regex_effbot               | 2.74 ms                                                                | 2.81 ms: 1.02x slower                                                 |
| spectral_norm              | 107 ms                                                                 | 110 ms: 1.03x slower                                                  |
| scimark_lu                 | 109 ms                                                                 | 112 ms: 1.03x slower                                                  |
| meteor_contest             | 99.1 ms                                                                | 102 ms: 1.03x slower                                                  |
| mdp                        | 2.35 sec                                                               | 2.54 sec: 1.08x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (33): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, richards, django_template, scimark_monte_carlo, many_optionals, async_tree_io, sympy_str, async_tree_memoization, pycparser, dulwich_log, docutils, asyncio_websockets, typing_runtime_protocols, pylint, generators, k_core, unpickle_pure_python, float, async_tree_none, sqlglot_transpile, regex_compile, pyflate, pathlib, json_loads, deepcopy, tomli_loads, bench_mp_pool, thrift, pprint_safe_repr, shortest_path, richards_super

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 86.70% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x