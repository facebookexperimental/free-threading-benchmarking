# Results vs. base

- fork: mpage
- ref: revert_gc_changes
- machine: linux-x86_64
- commit hash: 2923163
- commit date: 2024-12-03
- overall geometric mean: 1.003x faster
- HPT reliability: 56.65%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 376 ms                                                                 | 377 ms: 1.00x slower                                               |
| docutils       | 3.21 sec                                                               | 3.18 sec: 1.01x faster                                             |
| html5lib       | 100 ms                                                                 | 99.7 ms: 1.01x faster                                              |
| sphinx         | 1.24 sec                                                               | 1.23 sec: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| coroutines                | 28.2 ms                                                                | 27.6 ms: 1.02x faster                                              |
| async_generators          | 472 ms                                                                 | 468 ms: 1.01x faster                                               |
| async_tree_none           | 398 ms                                                                 | 401 ms: 1.01x slower                                               |
| async_tree_io             | 887 ms                                                                 | 893 ms: 1.01x slower                                               |
| async_tree_memoization_tg | 459 ms                                                                 | 463 ms: 1.01x slower                                               |
| async_tree_io_tg          | 862 ms                                                                 | 870 ms: 1.01x slower                                               |
| async_tree_none_tg        | 363 ms                                                                 | 367 ms: 1.01x slower                                               |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                       |

Benchmark hidden because not significant (4): asyncio_websockets, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                 | 182 ms: 1.01x faster                                               |
| nbody          | 132 ms                                                                 | 133 ms: 1.01x slower                                               |
| float          | 143 ms                                                                 | 144 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_v8       | 25.5 ms                                                                | 23.3 ms: 1.09x faster                                              |
| regex_effbot   | 2.91 ms                                                                | 2.67 ms: 1.09x faster                                              |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                               |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                       |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|---------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse | 95.4 ms                                                                | 94.6 ms: 1.01x faster                                              |
| tomli_loads         | 2.78 sec                                                               | 2.76 sec: 1.00x faster                                             |
| xml_etree_process   | 82.1 ms                                                                | 82.3 ms: 1.00x slower                                              |
| xml_etree_generate  | 102 ms                                                                 | 102 ms: 1.01x slower                                               |
| json_loads          | 27.9 us                                                                | 28.2 us: 1.01x slower                                              |
| json_dumps          | 14.2 ms                                                                | 14.6 ms: 1.03x slower                                              |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                       |

Benchmark hidden because not significant (3): pickle_pure_python, unpickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 10.2 ms                                                                | 10.3 ms: 1.00x slower                                              |
| python_startup         | 17.4 ms                                                                | 17.5 ms: 1.00x slower                                              |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| mako           | 19.9 ms                                                                | 20.1 ms: 1.01x slower                                              |
| genshi_text    | 33.3 ms                                                                | 33.9 ms: 1.02x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                       |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                 | bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2+-8ba9f5b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_v8                  | 25.5 ms                                                                | 23.3 ms: 1.09x faster                                              |
| regex_effbot              | 2.91 ms                                                                | 2.67 ms: 1.09x faster                                              |
| regex_dna                 | 189 ms                                                                 | 175 ms: 1.08x faster                                               |
| gc_traversal              | 3.30 ms                                                                | 3.18 ms: 1.04x faster                                              |
| richards_super            | 101 ms                                                                 | 98.5 ms: 1.02x faster                                              |
| logging_simple            | 11.2 us                                                                | 11.0 us: 1.02x faster                                              |
| coroutines                | 28.2 ms                                                                | 27.6 ms: 1.02x faster                                              |
| mdp                       | 3.03 sec                                                               | 2.98 sec: 1.02x faster                                             |
| fannkuch                  | 515 ms                                                                 | 506 ms: 1.02x faster                                               |
| richards                  | 83.7 ms                                                                | 82.2 ms: 1.02x faster                                              |
| pidigits                  | 184 ms                                                                 | 182 ms: 1.01x faster                                               |
| coverage                  | 102 ms                                                                 | 101 ms: 1.01x faster                                               |
| logging_format            | 12.3 us                                                                | 12.2 us: 1.01x faster                                              |
| hexiom                    | 10.9 ms                                                                | 10.8 ms: 1.01x faster                                              |
| logging_silent            | 202 ns                                                                 | 200 ns: 1.01x faster                                               |
| crypto_pyaes              | 94.3 ms                                                                | 93.4 ms: 1.01x faster                                              |
| async_generators          | 472 ms                                                                 | 468 ms: 1.01x faster                                               |
| xml_etree_iterparse       | 95.4 ms                                                                | 94.6 ms: 1.01x faster                                              |
| pyflate                   | 734 ms                                                                 | 728 ms: 1.01x faster                                               |
| html5lib                  | 100 ms                                                                 | 99.7 ms: 1.01x faster                                              |
| go                        | 282 ms                                                                 | 280 ms: 1.01x faster                                               |
| docutils                  | 3.21 sec                                                               | 3.18 sec: 1.01x faster                                             |
| bpe_tokeniser             | 5.49 sec                                                               | 5.46 sec: 1.01x faster                                             |
| sphinx                    | 1.24 sec                                                               | 1.23 sec: 1.01x faster                                             |
| scimark_fft               | 409 ms                                                                 | 406 ms: 1.01x faster                                               |
| raytrace                  | 603 ms                                                                 | 599 ms: 1.01x faster                                               |
| comprehensions            | 29.2 us                                                                | 29.0 us: 1.01x faster                                              |
| scimark_sparse_mat_mult   | 5.90 ms                                                                | 5.87 ms: 1.01x faster                                              |
| sympy_expand              | 986 ms                                                                 | 982 ms: 1.00x faster                                               |
| tomli_loads               | 2.78 sec                                                               | 2.76 sec: 1.00x faster                                             |
| pprint_pformat            | 2.21 sec                                                               | 2.20 sec: 1.00x faster                                             |
| pprint_safe_repr          | 1.06 sec                                                               | 1.06 sec: 1.00x faster                                             |
| 2to3                      | 376 ms                                                                 | 377 ms: 1.00x slower                                               |
| xml_etree_process         | 82.1 ms                                                                | 82.3 ms: 1.00x slower                                              |
| sympy_str                 | 492 ms                                                                 | 494 ms: 1.00x slower                                               |
| sympy_integrate           | 30.7 ms                                                                | 30.8 ms: 1.00x slower                                              |
| python_startup_no_site    | 10.2 ms                                                                | 10.3 ms: 1.00x slower                                              |
| python_startup            | 17.4 ms                                                                | 17.5 ms: 1.00x slower                                              |
| deepcopy_reduce           | 3.75 us                                                                | 3.76 us: 1.00x slower                                              |
| scimark_sor               | 244 ms                                                                 | 245 ms: 1.00x slower                                               |
| xml_etree_generate        | 102 ms                                                                 | 102 ms: 1.01x slower                                               |
| create_gc_cycles          | 1.82 ms                                                                | 1.83 ms: 1.01x slower                                              |
| connected_components      | 513 ms                                                                 | 516 ms: 1.01x slower                                               |
| async_tree_none           | 398 ms                                                                 | 401 ms: 1.01x slower                                               |
| nqueens                   | 103 ms                                                                 | 103 ms: 1.01x slower                                               |
| spectral_norm             | 131 ms                                                                 | 132 ms: 1.01x slower                                               |
| async_tree_io             | 887 ms                                                                 | 893 ms: 1.01x slower                                               |
| nbody                     | 132 ms                                                                 | 133 ms: 1.01x slower                                               |
| sqlglot_optimize          | 74.9 ms                                                                | 75.4 ms: 1.01x slower                                              |
| float                     | 143 ms                                                                 | 144 ms: 1.01x slower                                               |
| mako                      | 19.9 ms                                                                | 20.1 ms: 1.01x slower                                              |
| telco                     | 8.80 ms                                                                | 8.87 ms: 1.01x slower                                              |
| async_tree_memoization_tg | 459 ms                                                                 | 463 ms: 1.01x slower                                               |
| async_tree_io_tg          | 862 ms                                                                 | 870 ms: 1.01x slower                                               |
| async_tree_none_tg        | 363 ms                                                                 | 367 ms: 1.01x slower                                               |
| pycparser                 | 1.60 sec                                                               | 1.62 sec: 1.01x slower                                             |
| thrift                    | 1.19 ms                                                                | 1.21 ms: 1.01x slower                                              |
| sqlglot_normalize         | 150 ms                                                                 | 152 ms: 1.01x slower                                               |
| json_loads                | 27.9 us                                                                | 28.2 us: 1.01x slower                                              |
| pathlib                   | 20.9 ms                                                                | 21.1 ms: 1.01x slower                                              |
| generators                | 38.1 ms                                                                | 38.6 ms: 1.01x slower                                              |
| deepcopy_memo             | 45.1 us                                                                | 45.7 us: 1.01x slower                                              |
| many_optionals            | 1.36 ms                                                                | 1.38 ms: 1.02x slower                                              |
| genshi_text               | 33.3 ms                                                                | 33.9 ms: 1.02x slower                                              |
| subparsers                | 33.0 ms                                                                | 33.8 ms: 1.02x slower                                              |
| json_dumps                | 14.2 ms                                                                | 14.6 ms: 1.03x slower                                              |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                       |

Benchmark hidden because not significant (30): sqlite_synth, pickle_pure_python, sqlalchemy_imperative, scimark_monte_carlo, dulwich_log, genshi_xml, unpickle_pure_python, typing_runtime_protocols, chaos, asyncio_websockets, bench_thread_pool, bench_mp_pool, sqlalchemy_declarative, shortest_path, async_tree_memoization, deltablue, async_tree_cpu_io_mixed, deepcopy, k_core, sympy_sum, xml_etree_parse, pylint, sqlglot_transpile, django_template, regex_compile, scimark_lu, async_tree_cpu_io_mixed_tg, meteor_contest, json, sqlglot_parse

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 56.65% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x