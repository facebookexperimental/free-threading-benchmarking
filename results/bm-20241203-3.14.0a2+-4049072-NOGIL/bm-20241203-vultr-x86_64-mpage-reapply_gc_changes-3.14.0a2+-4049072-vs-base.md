# Results vs. base

- fork: mpage
- ref: reapply_gc_changes
- machine: linux-x86_64
- commit hash: 4049072
- commit date: 2024-12-03
- overall geometric mean: 1.004x faster
- HPT reliability: 99.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 376 ms                                                                 | 375 ms: 1.00x faster                                                |
| sphinx         | 1.24 sec                                                               | 1.23 sec: 1.01x faster                                              |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| coroutines              | 28.2 ms                                                                | 27.3 ms: 1.03x faster                                               |
| async_tree_io_tg        | 862 ms                                                                 | 855 ms: 1.01x faster                                                |
| async_tree_memoization  | 491 ms                                                                 | 488 ms: 1.01x faster                                                |
| async_generators        | 472 ms                                                                 | 469 ms: 1.01x faster                                                |
| asyncio_websockets      | 520 ms                                                                 | 517 ms: 1.01x faster                                                |
| async_tree_io           | 887 ms                                                                 | 892 ms: 1.01x slower                                                |
| async_tree_cpu_io_mixed | 652 ms                                                                 | 659 ms: 1.01x slower                                                |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (4): async_tree_none, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 132 ms                                                                 | 128 ms: 1.03x faster                                                |
| pidigits       | 184 ms                                                                 | 182 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_v8       | 25.5 ms                                                                | 24.0 ms: 1.06x faster                                               |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.04x faster                                                |
| regex_effbot   | 2.91 ms                                                                | 2.89 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                        |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 382 us                                                                 | 373 us: 1.02x faster                                                |
| pickle_pure_python   | 570 us                                                                 | 560 us: 1.02x faster                                                |
| tomli_loads          | 2.78 sec                                                               | 2.75 sec: 1.01x faster                                              |
| json_loads           | 27.9 us                                                                | 28.0 us: 1.00x slower                                               |
| xml_etree_process    | 82.1 ms                                                                | 82.6 ms: 1.01x slower                                               |
| xml_etree_generate   | 102 ms                                                                 | 104 ms: 1.02x slower                                                |
| json_dumps           | 14.2 ms                                                                | 14.6 ms: 1.02x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 17.4 ms                                                                | 17.5 ms: 1.00x slower                                               |
| python_startup_no_site | 10.2 ms                                                                | 10.3 ms: 1.00x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako           | 19.9 ms                                                                | 19.6 ms: 1.02x faster                                               |
| genshi_xml     | 67.0 ms                                                                | 66.2 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2+-4049072 |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_v8                | 25.5 ms                                                                | 24.0 ms: 1.06x faster                                               |
| regex_dna               | 189 ms                                                                 | 182 ms: 1.04x faster                                                |
| nbody                   | 132 ms                                                                 | 128 ms: 1.03x faster                                                |
| coroutines              | 28.2 ms                                                                | 27.3 ms: 1.03x faster                                               |
| logging_silent          | 202 ns                                                                 | 196 ns: 1.03x faster                                                |
| hexiom                  | 10.9 ms                                                                | 10.6 ms: 1.03x faster                                               |
| deltablue               | 8.82 ms                                                                | 8.60 ms: 1.03x faster                                               |
| mdp                     | 3.03 sec                                                               | 2.96 sec: 1.03x faster                                              |
| unpickle_pure_python    | 382 us                                                                 | 373 us: 1.02x faster                                                |
| go                      | 282 ms                                                                 | 276 ms: 1.02x faster                                                |
| richards                | 83.7 ms                                                                | 82.1 ms: 1.02x faster                                               |
| pickle_pure_python      | 570 us                                                                 | 560 us: 1.02x faster                                                |
| scimark_sor             | 244 ms                                                                 | 239 ms: 1.02x faster                                                |
| mako                    | 19.9 ms                                                                | 19.6 ms: 1.02x faster                                               |
| crypto_pyaes            | 94.3 ms                                                                | 92.7 ms: 1.02x faster                                               |
| raytrace                | 603 ms                                                                 | 593 ms: 1.02x faster                                                |
| scimark_monte_carlo     | 123 ms                                                                 | 121 ms: 1.02x faster                                                |
| shortest_path           | 567 ms                                                                 | 559 ms: 1.02x faster                                                |
| scimark_fft             | 409 ms                                                                 | 403 ms: 1.02x faster                                                |
| pidigits                | 184 ms                                                                 | 182 ms: 1.01x faster                                                |
| coverage                | 102 ms                                                                 | 101 ms: 1.01x faster                                                |
| chaos                   | 111 ms                                                                 | 110 ms: 1.01x faster                                                |
| pathlib                 | 20.9 ms                                                                | 20.6 ms: 1.01x faster                                               |
| genshi_xml              | 67.0 ms                                                                | 66.2 ms: 1.01x faster                                               |
| bpe_tokeniser           | 5.49 sec                                                               | 5.43 sec: 1.01x faster                                              |
| richards_super          | 101 ms                                                                 | 99.7 ms: 1.01x faster                                               |
| tomli_loads             | 2.78 sec                                                               | 2.75 sec: 1.01x faster                                              |
| regex_effbot            | 2.91 ms                                                                | 2.89 ms: 1.01x faster                                               |
| async_tree_io_tg        | 862 ms                                                                 | 855 ms: 1.01x faster                                                |
| fannkuch                | 515 ms                                                                 | 511 ms: 1.01x faster                                                |
| pyflate                 | 734 ms                                                                 | 728 ms: 1.01x faster                                                |
| comprehensions          | 29.2 us                                                                | 29.0 us: 1.01x faster                                               |
| async_tree_memoization  | 491 ms                                                                 | 488 ms: 1.01x faster                                                |
| async_generators        | 472 ms                                                                 | 469 ms: 1.01x faster                                                |
| spectral_norm           | 131 ms                                                                 | 130 ms: 1.01x faster                                                |
| dulwich_log             | 99.1 ms                                                                | 98.5 ms: 1.01x faster                                               |
| asyncio_websockets      | 520 ms                                                                 | 517 ms: 1.01x faster                                                |
| sphinx                  | 1.24 sec                                                               | 1.23 sec: 1.01x faster                                              |
| sympy_integrate         | 30.7 ms                                                                | 30.6 ms: 1.00x faster                                               |
| 2to3                    | 376 ms                                                                 | 375 ms: 1.00x faster                                                |
| deepcopy_reduce         | 3.75 us                                                                | 3.73 us: 1.00x faster                                               |
| deepcopy_memo           | 45.1 us                                                                | 45.2 us: 1.00x slower                                               |
| python_startup          | 17.4 ms                                                                | 17.5 ms: 1.00x slower                                               |
| json_loads              | 27.9 us                                                                | 28.0 us: 1.00x slower                                               |
| scimark_lu              | 194 ms                                                                 | 195 ms: 1.00x slower                                                |
| python_startup_no_site  | 10.2 ms                                                                | 10.3 ms: 1.00x slower                                               |
| async_tree_io           | 887 ms                                                                 | 892 ms: 1.01x slower                                                |
| sqlglot_normalize       | 150 ms                                                                 | 151 ms: 1.01x slower                                                |
| xml_etree_process       | 82.1 ms                                                                | 82.6 ms: 1.01x slower                                               |
| scimark_sparse_mat_mult | 5.90 ms                                                                | 5.94 ms: 1.01x slower                                               |
| pprint_pformat          | 2.21 sec                                                               | 2.22 sec: 1.01x slower                                              |
| sqlglot_optimize        | 74.9 ms                                                                | 75.4 ms: 1.01x slower                                               |
| thrift                  | 1.19 ms                                                                | 1.20 ms: 1.01x slower                                               |
| generators              | 38.1 ms                                                                | 38.5 ms: 1.01x slower                                               |
| async_tree_cpu_io_mixed | 652 ms                                                                 | 659 ms: 1.01x slower                                                |
| pprint_safe_repr        | 1.06 sec                                                               | 1.08 sec: 1.01x slower                                              |
| nqueens                 | 103 ms                                                                 | 104 ms: 1.01x slower                                                |
| xml_etree_generate      | 102 ms                                                                 | 104 ms: 1.02x slower                                                |
| pycparser               | 1.60 sec                                                               | 1.63 sec: 1.02x slower                                              |
| telco                   | 8.80 ms                                                                | 8.98 ms: 1.02x slower                                               |
| json_dumps              | 14.2 ms                                                                | 14.6 ms: 1.02x slower                                               |
| create_gc_cycles        | 1.82 ms                                                                | 1.86 ms: 1.02x slower                                               |
| gc_traversal            | 3.30 ms                                                                | 3.52 ms: 1.07x slower                                               |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (33): logging_simple, xml_etree_iterparse, django_template, async_tree_none, pylint, connected_components, k_core, json, async_tree_none_tg, sqlglot_parse, sympy_expand, html5lib, sqlglot_transpile, docutils, sqlalchemy_declarative, sympy_str, meteor_contest, genshi_text, bench_mp_pool, many_optionals, bench_thread_pool, float, xml_etree_parse, typing_runtime_protocols, sqlite_synth, sympy_sum, subparsers, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, regex_compile, sqlalchemy_imperative, deepcopy, logging_format

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 99.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x