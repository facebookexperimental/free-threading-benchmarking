# Results vs. base

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.004x faster
- HPT reliability: 57.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| html5lib       | 89.3 ms                                                                | 84.4 ms: 1.06x faster                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg | 363 ms                                                                 | 375 ms: 1.03x slower                                                 |
| async_tree_io_tg   | 849 ms                                                                 | 888 ms: 1.05x slower                                                 |
| Geometric mean     | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (9): async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none, asyncio_websockets, async_generators, async_tree_cpu_io_mixed, coroutines, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 113 ms                                                                 | 107 ms: 1.05x faster                                                 |
| nbody          | 120 ms                                                                 | 129 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.12 ms                                                                | 4.24 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (3): regex_compile, regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|---------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse | 143 ms                                                                 | 136 ms: 1.05x faster                                                 |
| json_dumps          | 15.6 ms                                                                | 14.9 ms: 1.05x faster                                                |
| json_loads          | 32.7 us                                                                | 33.7 us: 1.03x slower                                                |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (6): xml_etree_generate, xml_etree_process, tomli_loads, xml_etree_parse, unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml     | 69.5 ms                                                                | 65.3 ms: 1.06x faster                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (3): mako, genshi_text, django_template

All benchmarks:
===============

| Benchmark             | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal          | 7.70 ms                                                                | 7.01 ms: 1.10x faster                                                |
| crypto_pyaes          | 97.2 ms                                                                | 89.1 ms: 1.09x faster                                                |
| sympy_integrate       | 28.4 ms                                                                | 26.5 ms: 1.07x faster                                                |
| nqueens               | 105 ms                                                                 | 98.1 ms: 1.07x faster                                                |
| genshi_xml            | 69.5 ms                                                                | 65.3 ms: 1.06x faster                                                |
| html5lib              | 89.3 ms                                                                | 84.4 ms: 1.06x faster                                                |
| pprint_pformat        | 1.99 sec                                                               | 1.88 sec: 1.06x faster                                               |
| meteor_contest        | 144 ms                                                                 | 137 ms: 1.06x faster                                                 |
| scimark_sor           | 157 ms                                                                 | 149 ms: 1.05x faster                                                 |
| xml_etree_iterparse   | 143 ms                                                                 | 136 ms: 1.05x faster                                                 |
| create_gc_cycles      | 3.53 ms                                                                | 3.36 ms: 1.05x faster                                                |
| float                 | 113 ms                                                                 | 107 ms: 1.05x faster                                                 |
| json_dumps            | 15.6 ms                                                                | 14.9 ms: 1.05x faster                                                |
| pycparser             | 1.61 sec                                                               | 1.54 sec: 1.04x faster                                               |
| scimark_lu            | 154 ms                                                                 | 148 ms: 1.04x faster                                                 |
| deepcopy              | 348 us                                                                 | 338 us: 1.03x faster                                                 |
| richards_super        | 69.8 ms                                                                | 67.8 ms: 1.03x faster                                                |
| sympy_expand          | 575 ms                                                                 | 591 ms: 1.03x slower                                                 |
| json_loads            | 32.7 us                                                                | 33.7 us: 1.03x slower                                                |
| deltablue             | 4.17 ms                                                                | 4.29 ms: 1.03x slower                                                |
| regex_effbot          | 4.12 ms                                                                | 4.24 ms: 1.03x slower                                                |
| comprehensions        | 21.2 us                                                                | 21.9 us: 1.03x slower                                                |
| sqlglot_normalize     | 135 ms                                                                 | 139 ms: 1.03x slower                                                 |
| async_tree_none_tg    | 363 ms                                                                 | 375 ms: 1.03x slower                                                 |
| sqlglot_parse         | 1.62 ms                                                                | 1.68 ms: 1.04x slower                                                |
| scimark_fft           | 436 ms                                                                 | 453 ms: 1.04x slower                                                 |
| async_tree_io_tg      | 849 ms                                                                 | 888 ms: 1.05x slower                                                 |
| pyflate               | 633 ms                                                                 | 662 ms: 1.05x slower                                                 |
| json                  | 6.03 ms                                                                | 6.32 ms: 1.05x slower                                                |
| sqlalchemy_imperative | 21.7 ms                                                                | 22.9 ms: 1.05x slower                                                |
| logging_simple        | 8.00 us                                                                | 8.47 us: 1.06x slower                                                |
| spectral_norm         | 134 ms                                                                 | 142 ms: 1.06x slower                                                 |
| bench_mp_pool         | 85.7 ms                                                                | 90.9 ms: 1.06x slower                                                |
| sympy_str             | 345 ms                                                                 | 369 ms: 1.07x slower                                                 |
| nbody                 | 120 ms                                                                 | 129 ms: 1.07x slower                                                 |
| Geometric mean        | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (61): sqlite_synth, mako, genshi_text, regex_compile, async_tree_memoization, telco, 2to3, hexiom, deepcopy_memo, regex_v8, chaos, sqlglot_optimize, scimark_monte_carlo, pprint_safe_repr, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, docutils, python_startup, regex_dna, xml_etree_generate, k_core, subparsers, connected_components, sphinx, logging_silent, bpe_tokeniser, django_template, generators, pylint, fannkuch, async_tree_none, asyncio_websockets, logging_format, dulwich_log, mdp, sqlalchemy_declarative, many_optionals, thrift, xml_etree_process, tomli_loads, raytrace, async_generators, typing_runtime_protocols, sqlglot_transpile, pidigits, python_startup_no_site, async_tree_cpu_io_mixed, shortest_path, richards, xml_etree_parse, deepcopy_reduce, coverage, scimark_sparse_mat_mult, unpickle_pure_python, coroutines, async_tree_io, pickle_pure_python, go, sympy_sum, pathlib, bench_thread_pool

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 57.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x