# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: 26bfc21
- commit date: 2024-11-22
- overall geometric mean: 1.00x slower
- HPT reliability: 96.66%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 378 ms                                                                 | 381 ms: 1.01x slower                                                  |
| html5lib       | 102 ms                                                                 | 99.7 ms: 1.02x faster                                                 |
| sphinx         | 1.24 sec                                                               | 1.24 sec: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 27.6 ms                                                                | 27.5 ms: 1.00x faster                                                 |
| async_tree_io_tg           | 880 ms                                                                 | 887 ms: 1.01x slower                                                  |
| async_tree_memoization_tg  | 468 ms                                                                 | 472 ms: 1.01x slower                                                  |
| async_tree_none            | 407 ms                                                                 | 412 ms: 1.01x slower                                                  |
| async_tree_io              | 901 ms                                                                 | 912 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 642 ms: 1.01x slower                                                  |
| async_tree_none_tg         | 373 ms                                                                 | 377 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (4): async_generators, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 163 ms                                                                 | 158 ms: 1.03x faster                                                  |
| pidigits       | 184 ms                                                                 | 184 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 183 ms                                                                 | 181 ms: 1.01x faster                                                  |
| regex_effbot   | 2.70 ms                                                                | 2.80 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 375 us                                                                 | 371 us: 1.01x faster                                                  |
| xml_etree_parse      | 132 ms                                                                 | 131 ms: 1.01x faster                                                  |
| pickle_pure_python   | 549 us                                                                 | 545 us: 1.01x faster                                                  |
| json_loads           | 27.9 us                                                                | 27.9 us: 1.00x faster                                                 |
| xml_etree_generate   | 103 ms                                                                 | 103 ms: 1.00x faster                                                  |
| json_dumps           | 14.4 ms                                                                | 14.5 ms: 1.00x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): xml_etree_process, xml_etree_iterparse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.5 ms: 1.00x faster                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 33.8 ms                                                                | 34.2 ms: 1.01x slower                                                 |
| genshi_xml     | 66.3 ms                                                                | 68.1 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody                      | 163 ms                                                                 | 158 ms: 1.03x faster                                                  |
| coverage                   | 103 ms                                                                 | 101 ms: 1.02x faster                                                  |
| html5lib                   | 102 ms                                                                 | 99.7 ms: 1.02x faster                                                 |
| meteor_contest             | 139 ms                                                                 | 136 ms: 1.02x faster                                                  |
| shortest_path              | 568 ms                                                                 | 558 ms: 1.02x faster                                                  |
| connected_components       | 516 ms                                                                 | 509 ms: 1.01x faster                                                  |
| logging_simple             | 11.2 us                                                                | 11.1 us: 1.01x faster                                                 |
| deltablue                  | 8.76 ms                                                                | 8.65 ms: 1.01x faster                                                 |
| regex_dna                  | 183 ms                                                                 | 181 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 375 us                                                                 | 371 us: 1.01x faster                                                  |
| logging_silent             | 197 ns                                                                 | 195 ns: 1.01x faster                                                  |
| xml_etree_parse            | 132 ms                                                                 | 131 ms: 1.01x faster                                                  |
| pyflate                    | 744 ms                                                                 | 738 ms: 1.01x faster                                                  |
| pickle_pure_python         | 549 us                                                                 | 545 us: 1.01x faster                                                  |
| create_gc_cycles           | 1.86 ms                                                                | 1.85 ms: 1.01x faster                                                 |
| gc_traversal               | 3.53 ms                                                                | 3.51 ms: 1.01x faster                                                 |
| scimark_sor                | 245 ms                                                                 | 243 ms: 1.01x faster                                                  |
| sphinx                     | 1.24 sec                                                               | 1.24 sec: 1.00x faster                                                |
| spectral_norm              | 127 ms                                                                 | 127 ms: 1.00x faster                                                  |
| coroutines                 | 27.6 ms                                                                | 27.5 ms: 1.00x faster                                                 |
| pathlib                    | 20.8 ms                                                                | 20.7 ms: 1.00x faster                                                 |
| python_startup             | 17.5 ms                                                                | 17.5 ms: 1.00x faster                                                 |
| json_loads                 | 27.9 us                                                                | 27.9 us: 1.00x faster                                                 |
| bpe_tokeniser              | 5.65 sec                                                               | 5.64 sec: 1.00x faster                                                |
| xml_etree_generate         | 103 ms                                                                 | 103 ms: 1.00x faster                                                  |
| fannkuch                   | 551 ms                                                                 | 550 ms: 1.00x faster                                                  |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                 |
| pidigits                   | 184 ms                                                                 | 184 ms: 1.00x faster                                                  |
| comprehensions             | 28.8 us                                                                | 28.9 us: 1.00x slower                                                 |
| crypto_pyaes               | 103 ms                                                                 | 103 ms: 1.00x slower                                                  |
| sympy_expand               | 987 ms                                                                 | 991 ms: 1.00x slower                                                  |
| hexiom                     | 11.3 ms                                                                | 11.4 ms: 1.00x slower                                                 |
| sqlglot_normalize          | 149 ms                                                                 | 149 ms: 1.00x slower                                                  |
| json_dumps                 | 14.4 ms                                                                | 14.5 ms: 1.00x slower                                                 |
| sympy_str                  | 494 ms                                                                 | 497 ms: 1.00x slower                                                  |
| 2to3                       | 378 ms                                                                 | 381 ms: 1.01x slower                                                  |
| richards_super             | 98.9 ms                                                                | 99.7 ms: 1.01x slower                                                 |
| async_tree_io_tg           | 880 ms                                                                 | 887 ms: 1.01x slower                                                  |
| scimark_monte_carlo        | 120 ms                                                                 | 121 ms: 1.01x slower                                                  |
| async_tree_memoization_tg  | 468 ms                                                                 | 472 ms: 1.01x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                                | 75.5 ms: 1.01x slower                                                 |
| raytrace                   | 594 ms                                                                 | 601 ms: 1.01x slower                                                  |
| genshi_text                | 33.8 ms                                                                | 34.2 ms: 1.01x slower                                                 |
| async_tree_none            | 407 ms                                                                 | 412 ms: 1.01x slower                                                  |
| scimark_fft                | 396 ms                                                                 | 401 ms: 1.01x slower                                                  |
| async_tree_io              | 901 ms                                                                 | 912 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 642 ms: 1.01x slower                                                  |
| async_tree_none_tg         | 373 ms                                                                 | 377 ms: 1.01x slower                                                  |
| richards                   | 82.5 ms                                                                | 83.6 ms: 1.01x slower                                                 |
| deepcopy_reduce            | 3.73 us                                                                | 3.79 us: 1.01x slower                                                 |
| telco                      | 8.97 ms                                                                | 9.12 ms: 1.02x slower                                                 |
| subparsers                 | 32.9 ms                                                                | 33.5 ms: 1.02x slower                                                 |
| mdp                        | 2.96 sec                                                               | 3.02 sec: 1.02x slower                                                |
| genshi_xml                 | 66.3 ms                                                                | 68.1 ms: 1.03x slower                                                 |
| regex_effbot               | 2.70 ms                                                                | 2.80 ms: 1.03x slower                                                 |
| scimark_sparse_mat_mult    | 5.55 ms                                                                | 5.80 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (38): logging_format, sqlite_synth, async_generators, typing_runtime_protocols, go, asyncio_websockets, json, sqlglot_parse, pprint_safe_repr, django_template, mako, xml_etree_process, sympy_integrate, docutils, sqlglot_transpile, pprint_pformat, dulwich_log, regex_compile, deepcopy, nqueens, chaos, deepcopy_memo, k_core, xml_etree_iterparse, bench_mp_pool, pylint, thrift, async_tree_cpu_io_mixed, bench_thread_pool, generators, many_optionals, sympy_sum, pycparser, tomli_loads, async_tree_memoization, regex_v8, scimark_lu, float

# HPT report

- Reliability score: 96.66% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x