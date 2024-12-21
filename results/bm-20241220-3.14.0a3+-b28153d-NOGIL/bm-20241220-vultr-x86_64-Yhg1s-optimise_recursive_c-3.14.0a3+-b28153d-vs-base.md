# Results vs. base

- fork: Yhg1s
- ref: optimise_recursive_c
- machine: linux-x86_64
- commit hash: b28153d
- commit date: 2024-12-20
- overall geometric mean: 1.020x faster
- HPT reliability: 85.61%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 360 ms                                                                 | 352 ms: 1.02x faster                                                  |
| docutils       | 3.05 sec                                                               | 3.00 sec: 1.02x faster                                                |
| html5lib       | 91.4 ms                                                                | 90.8 ms: 1.01x faster                                                 |
| sphinx         | 1.16 sec                                                               | 1.15 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io             | 757 ms                                                                 | 760 ms: 1.00x slower                                                  |
| async_tree_memoization_tg | 402 ms                                                                 | 405 ms: 1.01x slower                                                  |
| async_tree_memoization    | 430 ms                                                                 | 433 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed   | 598 ms                                                                 | 603 ms: 1.01x slower                                                  |
| coroutines                | 24.0 ms                                                                | 24.2 ms: 1.01x slower                                                 |
| async_tree_io_tg          | 735 ms                                                                 | 742 ms: 1.01x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_none, asyncio_websockets, async_generators, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 113 ms                                                                 | 113 ms: 1.00x slower                                                  |
| pidigits       | 181 ms                                                                 | 184 ms: 1.02x slower                                                  |
| nbody          | 127 ms                                                                 | 137 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.8 ms                                                                | 24.7 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): regex_compile, regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps         | 14.3 ms                                                                | 14.0 ms: 1.02x faster                                                 |
| xml_etree_generate | 97.2 ms                                                                | 97.0 ms: 1.00x faster                                                 |
| json_loads         | 28.2 us                                                                | 28.4 us: 1.01x slower                                                 |
| tomli_loads        | 2.53 sec                                                               | 2.60 sec: 1.03x slower                                                |
| Geometric mean     | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (5): xml_etree_process, xml_etree_parse, pickle_pure_python, xml_etree_iterparse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.2 ms                                                                | 15.7 ms: 1.09x faster                                                 |
| python_startup_no_site | 10.2 ms                                                                | 9.82 ms: 1.04x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml     | 63.7 ms                                                                | 62.9 ms: 1.01x faster                                                 |
| genshi_text    | 30.7 ms                                                                | 30.5 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                 | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| sympy_sum                 | 349 ms                                                                 | 195 ms: 1.79x faster                                                  |
| sympy_expand              | 951 ms                                                                 | 582 ms: 1.63x faster                                                  |
| sympy_str                 | 478 ms                                                                 | 357 ms: 1.34x faster                                                  |
| sympy_integrate           | 29.6 ms                                                                | 25.3 ms: 1.17x faster                                                 |
| python_startup            | 17.2 ms                                                                | 15.7 ms: 1.09x faster                                                 |
| sqlalchemy_declarative    | 197 ms                                                                 | 183 ms: 1.08x faster                                                  |
| bench_mp_pool             | 108 ms                                                                 | 101 ms: 1.07x faster                                                  |
| pylint                    | 365 ms                                                                 | 348 ms: 1.05x faster                                                  |
| python_startup_no_site    | 10.2 ms                                                                | 9.82 ms: 1.04x faster                                                 |
| logging_silent            | 184 ns                                                                 | 177 ns: 1.04x faster                                                  |
| deltablue                 | 7.67 ms                                                                | 7.39 ms: 1.04x faster                                                 |
| coverage                  | 102 ms                                                                 | 99.0 ms: 1.03x faster                                                 |
| richards                  | 69.1 ms                                                                | 67.2 ms: 1.03x faster                                                 |
| pyflate                   | 655 ms                                                                 | 639 ms: 1.03x faster                                                  |
| go                        | 244 ms                                                                 | 238 ms: 1.02x faster                                                  |
| 2to3                      | 360 ms                                                                 | 352 ms: 1.02x faster                                                  |
| scimark_sor               | 219 ms                                                                 | 215 ms: 1.02x faster                                                  |
| thrift                    | 1.00 ms                                                                | 984 us: 1.02x faster                                                  |
| json_dumps                | 14.3 ms                                                                | 14.0 ms: 1.02x faster                                                 |
| pathlib                   | 19.8 ms                                                                | 19.4 ms: 1.02x faster                                                 |
| scimark_fft               | 388 ms                                                                 | 382 ms: 1.02x faster                                                  |
| raytrace                  | 497 ms                                                                 | 489 ms: 1.02x faster                                                  |
| logging_simple            | 9.21 us                                                                | 9.06 us: 1.02x faster                                                 |
| docutils                  | 3.05 sec                                                               | 3.00 sec: 1.02x faster                                                |
| telco                     | 8.81 ms                                                                | 8.68 ms: 1.02x faster                                                 |
| genshi_xml                | 63.7 ms                                                                | 62.9 ms: 1.01x faster                                                 |
| comprehensions            | 27.9 us                                                                | 27.5 us: 1.01x faster                                                 |
| scimark_monte_carlo       | 107 ms                                                                 | 106 ms: 1.01x faster                                                  |
| sqlite_synth              | 2.14 us                                                                | 2.12 us: 1.01x faster                                                 |
| generators                | 38.4 ms                                                                | 38.0 ms: 1.01x faster                                                 |
| hexiom                    | 9.66 ms                                                                | 9.57 ms: 1.01x faster                                                 |
| sphinx                    | 1.16 sec                                                               | 1.15 sec: 1.01x faster                                                |
| spectral_norm             | 111 ms                                                                 | 110 ms: 1.01x faster                                                  |
| typing_runtime_protocols  | 206 us                                                                 | 204 us: 1.01x faster                                                  |
| html5lib                  | 91.4 ms                                                                | 90.8 ms: 1.01x faster                                                 |
| genshi_text               | 30.7 ms                                                                | 30.5 ms: 1.01x faster                                                 |
| many_optionals            | 1.25 ms                                                                | 1.24 ms: 1.01x faster                                                 |
| regex_v8                  | 24.8 ms                                                                | 24.7 ms: 1.00x faster                                                 |
| xml_etree_generate        | 97.2 ms                                                                | 97.0 ms: 1.00x faster                                                 |
| float                     | 113 ms                                                                 | 113 ms: 1.00x slower                                                  |
| sqlglot_normalize         | 133 ms                                                                 | 133 ms: 1.00x slower                                                  |
| bench_thread_pool         | 3.38 ms                                                                | 3.39 ms: 1.00x slower                                                 |
| async_tree_io             | 757 ms                                                                 | 760 ms: 1.00x slower                                                  |
| nqueens                   | 98.0 ms                                                                | 98.5 ms: 1.00x slower                                                 |
| async_tree_memoization_tg | 402 ms                                                                 | 405 ms: 1.01x slower                                                  |
| async_tree_memoization    | 430 ms                                                                 | 433 ms: 1.01x slower                                                  |
| dulwich_log               | 90.1 ms                                                                | 90.8 ms: 1.01x slower                                                 |
| deepcopy_memo             | 39.9 us                                                                | 40.2 us: 1.01x slower                                                 |
| pprint_pformat            | 1.99 sec                                                               | 2.01 sec: 1.01x slower                                                |
| json_loads                | 28.2 us                                                                | 28.4 us: 1.01x slower                                                 |
| pprint_safe_repr          | 956 ms                                                                 | 964 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed   | 598 ms                                                                 | 603 ms: 1.01x slower                                                  |
| scimark_lu                | 158 ms                                                                 | 160 ms: 1.01x slower                                                  |
| bpe_tokeniser             | 4.99 sec                                                               | 5.04 sec: 1.01x slower                                                |
| coroutines                | 24.0 ms                                                                | 24.2 ms: 1.01x slower                                                 |
| async_tree_io_tg          | 735 ms                                                                 | 742 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult   | 5.47 ms                                                                | 5.54 ms: 1.01x slower                                                 |
| pidigits                  | 181 ms                                                                 | 184 ms: 1.02x slower                                                  |
| fannkuch                  | 490 ms                                                                 | 500 ms: 1.02x slower                                                  |
| mdp                       | 2.81 sec                                                               | 2.87 sec: 1.02x slower                                                |
| tomli_loads               | 2.53 sec                                                               | 2.60 sec: 1.03x slower                                                |
| create_gc_cycles          | 1.79 ms                                                                | 1.84 ms: 1.03x slower                                                 |
| gc_traversal              | 3.26 ms                                                                | 3.51 ms: 1.08x slower                                                 |
| nbody                     | 127 ms                                                                 | 137 ms: 1.08x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (32): chaos, subparsers, sqlalchemy_imperative, async_tree_none_tg, sqlglot_transpile, django_template, sqlglot_parse, deepcopy_reduce, regex_compile, logging_format, async_tree_none, mako, regex_dna, asyncio_websockets, xml_etree_process, k_core, xml_etree_parse, meteor_contest, deepcopy, async_generators, pickle_pure_python, async_tree_cpu_io_mixed_tg, regex_effbot, crypto_pyaes, pycparser, xml_etree_iterparse, connected_components, shortest_path, unpickle_pure_python, json, sqlglot_optimize, richards_super

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 85.61% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x