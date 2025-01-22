# Results vs. base

- fork: mpage
- ref: ft_aa_test_0
- machine: linux-x86_64
- commit hash: fcbf62d
- commit date: 2025-01-22
- overall geometric mean: 1.001x slower
- HPT reliability: 93.21%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 312 ms                                                                 | 314 ms: 1.01x slower                                          |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                  |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_generators           | 381 ms                                                                 | 376 ms: 1.01x faster                                          |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                 | 502 ms: 1.01x faster                                          |
| asyncio_websockets         | 516 ms                                                                 | 513 ms: 1.01x faster                                          |
| async_tree_cpu_io_mixed    | 540 ms                                                                 | 537 ms: 1.01x faster                                          |
| coroutines                 | 24.9 ms                                                                | 25.4 ms: 1.02x slower                                         |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_none_tg, async_tree_io, async_tree_io_tg, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 220 ms                                                                 | 196 ms: 1.13x faster                                          |
| nbody          | 136 ms                                                                 | 141 ms: 1.04x slower                                          |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                  |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_v8       | 24.3 ms                                                                | 23.8 ms: 1.02x faster                                         |
| regex_effbot   | 2.89 ms                                                                | 2.88 ms: 1.00x faster                                         |
| regex_compile  | 159 ms                                                                 | 160 ms: 1.00x slower                                          |
| regex_dna      | 180 ms                                                                 | 183 ms: 1.01x slower                                          |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 89.0 ms                                                                | 87.9 ms: 1.01x faster                                         |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                          |
| json_loads           | 30.8 us                                                                | 30.6 us: 1.01x faster                                         |
| unpickle_pure_python | 275 us                                                                 | 275 us: 1.00x slower                                          |
| json_dumps           | 12.9 ms                                                                | 13.0 ms: 1.00x slower                                         |
| pickle_pure_python   | 397 us                                                                 | 399 us: 1.00x slower                                          |
| tomli_loads          | 2.43 sec                                                               | 2.49 sec: 1.03x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                  |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 9.55 ms                                                                | 9.53 ms: 1.00x faster                                         |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| mako           | 16.2 ms                                                                | 16.3 ms: 1.00x slower                                         |
| genshi_text    | 29.6 ms                                                                | 29.9 ms: 1.01x slower                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                  |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                  | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits                   | 220 ms                                                                 | 196 ms: 1.13x faster                                          |
| gc_traversal               | 3.35 ms                                                                | 3.25 ms: 1.03x faster                                         |
| create_gc_cycles           | 1.36 ms                                                                | 1.32 ms: 1.03x faster                                         |
| regex_v8                   | 24.3 ms                                                                | 23.8 ms: 1.02x faster                                         |
| sqlite_synth               | 2.08 us                                                                | 2.05 us: 1.02x faster                                         |
| async_generators           | 381 ms                                                                 | 376 ms: 1.01x faster                                          |
| xml_etree_iterparse        | 89.0 ms                                                                | 87.9 ms: 1.01x faster                                         |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                          |
| sympy_expand               | 567 ms                                                                 | 561 ms: 1.01x faster                                          |
| dulwich_log                | 84.6 ms                                                                | 83.8 ms: 1.01x faster                                         |
| json_loads                 | 30.8 us                                                                | 30.6 us: 1.01x faster                                         |
| richards                   | 57.0 ms                                                                | 56.6 ms: 1.01x faster                                         |
| deltablue                  | 4.80 ms                                                                | 4.77 ms: 1.01x faster                                         |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                 | 502 ms: 1.01x faster                                          |
| asyncio_websockets         | 516 ms                                                                 | 513 ms: 1.01x faster                                          |
| async_tree_cpu_io_mixed    | 540 ms                                                                 | 537 ms: 1.01x faster                                          |
| sympy_sum                  | 192 ms                                                                 | 191 ms: 1.01x faster                                          |
| regex_effbot               | 2.89 ms                                                                | 2.88 ms: 1.00x faster                                         |
| python_startup_no_site     | 9.55 ms                                                                | 9.53 ms: 1.00x faster                                         |
| unpickle_pure_python       | 275 us                                                                 | 275 us: 1.00x slower                                          |
| scimark_sparse_mat_mult    | 5.65 ms                                                                | 5.67 ms: 1.00x slower                                         |
| regex_compile              | 159 ms                                                                 | 160 ms: 1.00x slower                                          |
| json_dumps                 | 12.9 ms                                                                | 13.0 ms: 1.00x slower                                         |
| mako                       | 16.2 ms                                                                | 16.3 ms: 1.00x slower                                         |
| pickle_pure_python         | 397 us                                                                 | 399 us: 1.00x slower                                          |
| 2to3                       | 312 ms                                                                 | 314 ms: 1.01x slower                                          |
| generators                 | 33.1 ms                                                                | 33.3 ms: 1.01x slower                                         |
| deepcopy                   | 326 us                                                                 | 328 us: 1.01x slower                                          |
| shortest_path              | 547 ms                                                                 | 551 ms: 1.01x slower                                          |
| pprint_pformat             | 1.76 sec                                                               | 1.78 sec: 1.01x slower                                        |
| scimark_monte_carlo        | 83.6 ms                                                                | 84.3 ms: 1.01x slower                                         |
| hexiom                     | 7.69 ms                                                                | 7.77 ms: 1.01x slower                                         |
| pprint_safe_repr           | 850 ms                                                                 | 859 ms: 1.01x slower                                          |
| go                         | 143 ms                                                                 | 145 ms: 1.01x slower                                          |
| genshi_text                | 29.6 ms                                                                | 29.9 ms: 1.01x slower                                         |
| scimark_lu                 | 141 ms                                                                 | 142 ms: 1.01x slower                                          |
| logging_silent             | 119 ns                                                                 | 121 ns: 1.01x slower                                          |
| coverage                   | 97.6 ms                                                                | 98.8 ms: 1.01x slower                                         |
| pathlib                    | 18.7 ms                                                                | 18.9 ms: 1.01x slower                                         |
| regex_dna                  | 180 ms                                                                 | 183 ms: 1.01x slower                                          |
| nqueens                    | 99.1 ms                                                                | 101 ms: 1.02x slower                                          |
| meteor_contest             | 130 ms                                                                 | 133 ms: 1.02x slower                                          |
| chaos                      | 70.9 ms                                                                | 72.1 ms: 1.02x slower                                         |
| mdp                        | 2.69 sec                                                               | 2.74 sec: 1.02x slower                                        |
| coroutines                 | 24.9 ms                                                                | 25.4 ms: 1.02x slower                                         |
| crypto_pyaes               | 87.0 ms                                                                | 88.9 ms: 1.02x slower                                         |
| fannkuch                   | 489 ms                                                                 | 502 ms: 1.03x slower                                          |
| tomli_loads                | 2.43 sec                                                               | 2.49 sec: 1.03x slower                                        |
| pyflate                    | 509 ms                                                                 | 525 ms: 1.03x slower                                          |
| scimark_fft                | 386 ms                                                                 | 398 ms: 1.03x slower                                          |
| nbody                      | 136 ms                                                                 | 141 ms: 1.04x slower                                          |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                  |

Benchmark hidden because not significant (45): pylint, logging_format, richards_super, many_optionals, sqlglot_parse, bench_mp_pool, subparsers, docutils, xml_etree_process, async_tree_memoization_tg, float, sqlalchemy_declarative, python_startup, async_tree_none_tg, json, comprehensions, deepcopy_memo, sphinx, k_core, sqlglot_transpile, deepcopy_reduce, scimark_sor, raytrace, bpe_tokeniser, async_tree_io, sqlalchemy_imperative, bench_thread_pool, pycparser, async_tree_io_tg, xml_etree_generate, spectral_norm, sqlglot_normalize, html5lib, sympy_integrate, telco, sympy_str, thrift, genshi_xml, sqlglot_optimize, django_template, typing_runtime_protocols, async_tree_none, async_tree_memoization, logging_simple, connected_components

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 93.21% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x