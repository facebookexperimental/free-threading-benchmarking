# Results vs. base

- fork: colesbury
- ref: gh_129236_gc_stackpo
- machine: linux-x86_64
- commit hash: 1ec055b
- commit date: 2025-01-23
- overall geometric mean: 1.010x faster
- HPT reliability: 87.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4+-c05a851 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 304 ms                                                                 | 303 ms: 1.00x faster                                                      |
| html5lib       | 70.9 ms                                                                | 68.4 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4+-c05a851 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|---------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines                | 24.3 ms                                                                | 23.5 ms: 1.04x faster                                                     |
| async_tree_io_tg          | 587 ms                                                                 | 578 ms: 1.02x faster                                                      |
| async_tree_none_tg        | 255 ms                                                                 | 252 ms: 1.01x faster                                                      |
| async_tree_io             | 617 ms                                                                 | 611 ms: 1.01x faster                                                      |
| async_tree_none           | 291 ms                                                                 | 288 ms: 1.01x faster                                                      |
| async_tree_memoization_tg | 323 ms                                                                 | 321 ms: 1.01x faster                                                      |
| async_tree_cpu_io_mixed   | 542 ms                                                                 | 538 ms: 1.01x faster                                                      |
| asyncio_websockets        | 509 ms                                                                 | 512 ms: 1.00x slower                                                      |
| async_generators          | 370 ms                                                                 | 375 ms: 1.01x slower                                                      |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (2): async_tree_memoization, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4+-c05a851 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                                 | 190 ms: 1.05x faster                                                      |
| float          | 76.6 ms                                                                | 75.8 ms: 1.01x faster                                                     |
| nbody          | 134 ms                                                                 | 132 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4+-c05a851 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 2.93 ms                                                                | 2.80 ms: 1.05x faster                                                     |
| regex_v8       | 24.7 ms                                                                | 24.0 ms: 1.03x faster                                                     |
| regex_dna      | 182 ms                                                                 | 180 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4+-c05a851 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle_pure_python | 247 us                                                                 | 246 us: 1.00x faster                                                      |
| xml_etree_generate   | 96.3 ms                                                                | 96.7 ms: 1.00x slower                                                     |
| json_loads           | 30.4 us                                                                | 30.6 us: 1.01x slower                                                     |
| xml_etree_iterparse  | 86.4 ms                                                                | 87.2 ms: 1.01x slower                                                     |
| pickle_pure_python   | 371 us                                                                 | 375 us: 1.01x slower                                                      |
| xml_etree_parse      | 127 ms                                                                 | 129 ms: 1.01x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (3): tomli_loads, xml_etree_process, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4+-c05a851 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                                | 15.3 ms: 1.00x slower                                                     |
| python_startup_no_site | 9.55 ms                                                                | 9.60 ms: 1.01x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4+-c05a851 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako           | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (3): genshi_xml, django_template, genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4+-c05a851 | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|---------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal              | 3.29 ms                                                                | 1.66 ms: 1.97x faster                                                     |
| regex_effbot              | 2.93 ms                                                                | 2.80 ms: 1.05x faster                                                     |
| pidigits                  | 199 ms                                                                 | 190 ms: 1.05x faster                                                      |
| html5lib                  | 70.9 ms                                                                | 68.4 ms: 1.04x faster                                                     |
| coroutines                | 24.3 ms                                                                | 23.5 ms: 1.04x faster                                                     |
| mdp                       | 2.67 sec                                                               | 2.59 sec: 1.03x faster                                                    |
| pyflate                   | 509 ms                                                                 | 495 ms: 1.03x faster                                                      |
| regex_v8                  | 24.7 ms                                                                | 24.0 ms: 1.03x faster                                                     |
| deepcopy_reduce           | 3.28 us                                                                | 3.19 us: 1.03x faster                                                     |
| richards                  | 56.6 ms                                                                | 55.2 ms: 1.02x faster                                                     |
| generators                | 32.1 ms                                                                | 31.4 ms: 1.02x faster                                                     |
| scimark_monte_carlo       | 82.6 ms                                                                | 81.0 ms: 1.02x faster                                                     |
| logging_silent            | 116 ns                                                                 | 113 ns: 1.02x faster                                                      |
| richards_super            | 65.0 ms                                                                | 63.8 ms: 1.02x faster                                                     |
| typing_runtime_protocols  | 206 us                                                                 | 202 us: 1.02x faster                                                      |
| async_tree_io_tg          | 587 ms                                                                 | 578 ms: 1.02x faster                                                      |
| regex_dna                 | 182 ms                                                                 | 180 ms: 1.01x faster                                                      |
| deltablue                 | 4.69 ms                                                                | 4.63 ms: 1.01x faster                                                     |
| go                        | 139 ms                                                                 | 137 ms: 1.01x faster                                                      |
| async_tree_none_tg        | 255 ms                                                                 | 252 ms: 1.01x faster                                                      |
| float                     | 76.6 ms                                                                | 75.8 ms: 1.01x faster                                                     |
| nbody                     | 134 ms                                                                 | 132 ms: 1.01x faster                                                      |
| async_tree_io             | 617 ms                                                                 | 611 ms: 1.01x faster                                                      |
| async_tree_none           | 291 ms                                                                 | 288 ms: 1.01x faster                                                      |
| comprehensions            | 20.8 us                                                                | 20.6 us: 1.01x faster                                                     |
| hexiom                    | 7.36 ms                                                                | 7.30 ms: 1.01x faster                                                     |
| async_tree_memoization_tg | 323 ms                                                                 | 321 ms: 1.01x faster                                                      |
| scimark_sparse_mat_mult   | 5.53 ms                                                                | 5.49 ms: 1.01x faster                                                     |
| coverage                  | 98.4 ms                                                                | 97.7 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed   | 542 ms                                                                 | 538 ms: 1.01x faster                                                      |
| sympy_expand              | 550 ms                                                                 | 548 ms: 1.00x faster                                                      |
| unpickle_pure_python      | 247 us                                                                 | 246 us: 1.00x faster                                                      |
| 2to3                      | 304 ms                                                                 | 303 ms: 1.00x faster                                                      |
| mako                      | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                                     |
| scimark_fft               | 384 ms                                                                 | 383 ms: 1.00x faster                                                      |
| bpe_tokeniser             | 4.71 sec                                                               | 4.72 sec: 1.00x slower                                                    |
| chaos                     | 69.5 ms                                                                | 69.7 ms: 1.00x slower                                                     |
| nqueens                   | 96.0 ms                                                                | 96.3 ms: 1.00x slower                                                     |
| xml_etree_generate        | 96.3 ms                                                                | 96.7 ms: 1.00x slower                                                     |
| dulwich_log               | 82.2 ms                                                                | 82.5 ms: 1.00x slower                                                     |
| sqlglot_normalize         | 120 ms                                                                 | 121 ms: 1.00x slower                                                      |
| asyncio_websockets        | 509 ms                                                                 | 512 ms: 1.00x slower                                                      |
| python_startup            | 15.2 ms                                                                | 15.3 ms: 1.00x slower                                                     |
| bench_mp_pool             | 94.5 ms                                                                | 95.0 ms: 1.00x slower                                                     |
| python_startup_no_site    | 9.55 ms                                                                | 9.60 ms: 1.01x slower                                                     |
| sympy_sum                 | 186 ms                                                                 | 187 ms: 1.01x slower                                                      |
| sympy_integrate           | 24.1 ms                                                                | 24.3 ms: 1.01x slower                                                     |
| json_loads                | 30.4 us                                                                | 30.6 us: 1.01x slower                                                     |
| deepcopy                  | 314 us                                                                 | 316 us: 1.01x slower                                                      |
| json                      | 5.34 ms                                                                | 5.39 ms: 1.01x slower                                                     |
| xml_etree_iterparse       | 86.4 ms                                                                | 87.2 ms: 1.01x slower                                                     |
| deepcopy_memo             | 38.0 us                                                                | 38.4 us: 1.01x slower                                                     |
| crypto_pyaes              | 86.3 ms                                                                | 87.1 ms: 1.01x slower                                                     |
| subparsers                | 25.6 ms                                                                | 25.9 ms: 1.01x slower                                                     |
| pickle_pure_python        | 371 us                                                                 | 375 us: 1.01x slower                                                      |
| xml_etree_parse           | 127 ms                                                                 | 129 ms: 1.01x slower                                                      |
| many_optionals            | 1.17 ms                                                                | 1.19 ms: 1.01x slower                                                     |
| pprint_pformat            | 1.68 sec                                                               | 1.70 sec: 1.01x slower                                                    |
| pathlib                   | 18.7 ms                                                                | 18.9 ms: 1.01x slower                                                     |
| async_generators          | 370 ms                                                                 | 375 ms: 1.01x slower                                                      |
| pprint_safe_repr          | 815 ms                                                                 | 826 ms: 1.01x slower                                                      |
| scimark_sor               | 134 ms                                                                 | 136 ms: 1.01x slower                                                      |
| scimark_lu                | 137 ms                                                                 | 139 ms: 1.02x slower                                                      |
| spectral_norm             | 111 ms                                                                 | 113 ms: 1.02x slower                                                      |
| logging_format            | 8.17 us                                                                | 8.41 us: 1.03x slower                                                     |
| create_gc_cycles          | 1.33 ms                                                                | 1.40 ms: 1.05x slower                                                     |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (30): async_tree_memoization, sqlalchemy_imperative, telco, async_tree_cpu_io_mixed_tg, genshi_xml, sqlite_synth, sympy_str, tomli_loads, logging_simple, shortest_path, sphinx, docutils, connected_components, sqlalchemy_declarative, fannkuch, django_template, regex_compile, k_core, raytrace, sqlglot_parse, bench_thread_pool, sqlglot_transpile, pylint, pycparser, genshi_text, thrift, xml_etree_process, sqlglot_optimize, meteor_contest, json_dumps

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 87.63% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x