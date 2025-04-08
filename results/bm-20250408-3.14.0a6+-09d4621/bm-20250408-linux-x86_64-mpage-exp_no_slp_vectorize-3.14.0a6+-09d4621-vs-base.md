# Results vs. base

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.012x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 3.66 sec                                                               | 3.55 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg | 360 ms                                                                 | 375 ms: 1.04x slower                                                  |
| async_tree_io_tg   | 883 ms                                                                 | 934 ms: 1.06x slower                                                  |
| Geometric mean     | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (9): coroutines, async_generators, async_tree_memoization_tg, asyncio_websockets, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 115 ms                                                                 | 125 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.53 ms                                                                | 4.29 ms: 1.06x faster                                                 |
| regex_compile  | 157 ms                                                                 | 165 ms: 1.05x slower                                                  |
| regex_v8       | 30.1 ms                                                                | 34.3 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps     | 16.1 ms                                                                | 14.9 ms: 1.08x faster                                                 |
| tomli_loads    | 2.41 sec                                                               | 2.50 sec: 1.04x slower                                                |
| json_loads     | 38.2 us                                                                | 42.1 us: 1.10x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (6): xml_etree_iterparse, xml_etree_parse, unpickle_pure_python, xml_etree_generate, xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 27.6 ms                                                                | 29.3 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): django_template, genshi_xml, genshi_text, mako

All benchmarks:
===============

| Benchmark                | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|--------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| bench_thread_pool        | 3.22 ms                                                                | 2.53 ms: 1.27x faster                                                 |
| typing_runtime_protocols | 248 us                                                                 | 220 us: 1.13x faster                                                  |
| richards_super           | 70.5 ms                                                                | 63.6 ms: 1.11x faster                                                 |
| comprehensions           | 22.8 us                                                                | 20.8 us: 1.10x faster                                                 |
| json_dumps               | 16.1 ms                                                                | 14.9 ms: 1.08x faster                                                 |
| sympy_str                | 366 ms                                                                 | 338 ms: 1.08x faster                                                  |
| hexiom                   | 8.62 ms                                                                | 8.07 ms: 1.07x faster                                                 |
| regex_effbot             | 4.53 ms                                                                | 4.29 ms: 1.06x faster                                                 |
| docutils                 | 3.66 sec                                                               | 3.55 sec: 1.03x faster                                                |
| telco                    | 9.79 ms                                                                | 9.53 ms: 1.03x faster                                                 |
| tomli_loads              | 2.41 sec                                                               | 2.50 sec: 1.04x slower                                                |
| generators               | 42.9 ms                                                                | 44.6 ms: 1.04x slower                                                 |
| spectral_norm            | 128 ms                                                                 | 134 ms: 1.04x slower                                                  |
| async_tree_none_tg       | 360 ms                                                                 | 375 ms: 1.04x slower                                                  |
| connected_components     | 796 ms                                                                 | 829 ms: 1.04x slower                                                  |
| bpe_tokeniser            | 5.81 sec                                                               | 6.05 sec: 1.04x slower                                                |
| pprint_pformat           | 1.78 sec                                                               | 1.85 sec: 1.04x slower                                                |
| nqueens                  | 102 ms                                                                 | 107 ms: 1.05x slower                                                  |
| richards                 | 54.4 ms                                                                | 57.2 ms: 1.05x slower                                                 |
| regex_compile            | 157 ms                                                                 | 165 ms: 1.05x slower                                                  |
| sqlglot_v2_transpile     | 2.06 ms                                                                | 2.17 ms: 1.05x slower                                                 |
| async_tree_io_tg         | 883 ms                                                                 | 934 ms: 1.06x slower                                                  |
| deepcopy                 | 308 us                                                                 | 327 us: 1.06x slower                                                  |
| python_startup           | 27.6 ms                                                                | 29.3 ms: 1.06x slower                                                 |
| pyflate                  | 597 ms                                                                 | 636 ms: 1.07x slower                                                  |
| raytrace                 | 322 ms                                                                 | 345 ms: 1.07x slower                                                  |
| scimark_sor              | 147 ms                                                                 | 158 ms: 1.08x slower                                                  |
| chaos                    | 69.6 ms                                                                | 75.0 ms: 1.08x slower                                                 |
| nbody                    | 115 ms                                                                 | 125 ms: 1.08x slower                                                  |
| sqlalchemy_imperative    | 21.2 ms                                                                | 23.2 ms: 1.10x slower                                                 |
| json_loads               | 38.2 us                                                                | 42.1 us: 1.10x slower                                                 |
| logging_format           | 8.78 us                                                                | 9.82 us: 1.12x slower                                                 |
| regex_v8                 | 30.1 ms                                                                | 34.3 ms: 1.14x slower                                                 |
| gc_traversal             | 7.09 ms                                                                | 8.36 ms: 1.18x slower                                                 |
| sqlglot_v2_normalize     | 129 ms                                                                 | 155 ms: 1.20x slower                                                  |
| logging_simple           | 7.45 us                                                                | 9.03 us: 1.21x slower                                                 |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (58): xml_etree_iterparse, deltablue, crypto_pyaes, xml_etree_parse, coroutines, pathlib, sympy_expand, bench_mp_pool, scimark_fft, sqlite_synth, django_template, unpickle_pure_python, xml_etree_generate, async_generators, genshi_xml, genshi_text, go, async_tree_memoization_tg, deepcopy_memo, create_gc_cycles, asyncio_websockets, meteor_contest, xml_etree_process, scimark_monte_carlo, coverage, dulwich_log, python_startup_no_site, json, deepcopy_reduce, scimark_lu, scimark_sparse_mat_mult, pprint_safe_repr, regex_dna, mako, 2to3, sympy_integrate, k_core, pycparser, pidigits, pickle_pure_python, async_tree_none, sqlglot_v2_optimize, fannkuch, async_tree_memoization, mdp, shortest_path, logging_silent, float, sphinx, async_tree_cpu_io_mixed, sqlalchemy_declarative, async_tree_io, async_tree_cpu_io_mixed_tg, many_optionals, subparsers, sympy_sum, pylint, sqlglot_v2_parse

- Geometric mean (including insignificant results): 1.012x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x