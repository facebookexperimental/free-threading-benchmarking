# Results vs. base

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.010x slower
- HPT reliability: 99.10%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 469 ms                                                                 | 511 ms: 1.09x slower                                                  |
| docutils       | 3.97 sec                                                               | 4.09 sec: 1.03x slower                                                |
| sphinx         | 1.52 sec                                                               | 1.62 sec: 1.06x slower                                                |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 717 ms                                                                 | 650 ms: 1.10x faster                                                  |
| async_tree_memoization  | 465 ms                                                                 | 495 ms: 1.06x slower                                                  |
| coroutines              | 31.4 ms                                                                | 36.6 ms: 1.17x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_none_tg, asyncio_websockets, async_generators, async_tree_memoization_tg, async_tree_none, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 161 ms                                                                 | 150 ms: 1.07x faster                                                  |
| pidigits       | 242 ms                                                                 | 231 ms: 1.05x faster                                                  |
| float          | 92.0 ms                                                                | 100 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 280 ms                                                                 | 289 ms: 1.03x slower                                                  |
| regex_v8       | 29.9 ms                                                                | 31.8 ms: 1.06x slower                                                 |
| regex_effbot   | 3.96 ms                                                                | 4.24 ms: 1.07x slower                                                 |
| regex_compile  | 178 ms                                                                 | 192 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_process  | 103 ms                                                                 | 91.5 ms: 1.12x faster                                                 |
| xml_etree_generate | 133 ms                                                                 | 129 ms: 1.03x faster                                                  |
| tomli_loads        | 2.72 sec                                                               | 2.88 sec: 1.06x slower                                                |
| json_dumps         | 15.8 ms                                                                | 17.0 ms: 1.08x slower                                                 |
| pickle_pure_python | 454 us                                                                 | 497 us: 1.09x slower                                                  |
| Geometric mean     | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (4): xml_etree_parse, unpickle_pure_python, json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 32.2 ms                                                                | 29.8 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 35.3 ms                                                                | 37.0 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (3): genshi_xml, mako, django_template

All benchmarks:
===============

| Benchmark               | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| sqlalchemy_imperative   | 34.7 ms                                                                | 29.3 ms: 1.18x faster                                                 |
| xml_etree_process       | 103 ms                                                                 | 91.5 ms: 1.12x faster                                                 |
| async_tree_cpu_io_mixed | 717 ms                                                                 | 650 ms: 1.10x faster                                                  |
| sqlglot_v2_normalize    | 159 ms                                                                 | 146 ms: 1.09x faster                                                  |
| json                    | 7.79 ms                                                                | 7.18 ms: 1.08x faster                                                 |
| deepcopy_reduce         | 4.17 us                                                                | 3.86 us: 1.08x faster                                                 |
| python_startup          | 32.2 ms                                                                | 29.8 ms: 1.08x faster                                                 |
| nbody                   | 161 ms                                                                 | 150 ms: 1.07x faster                                                  |
| pidigits                | 242 ms                                                                 | 231 ms: 1.05x faster                                                  |
| sqlglot_v2_parse        | 2.03 ms                                                                | 1.96 ms: 1.03x faster                                                 |
| sqlalchemy_declarative  | 219 ms                                                                 | 211 ms: 1.03x faster                                                  |
| xml_etree_generate      | 133 ms                                                                 | 129 ms: 1.03x faster                                                  |
| regex_dna               | 280 ms                                                                 | 289 ms: 1.03x slower                                                  |
| docutils                | 3.97 sec                                                               | 4.09 sec: 1.03x slower                                                |
| k_core                  | 4.22 sec                                                               | 4.35 sec: 1.03x slower                                                |
| scimark_sor             | 162 ms                                                                 | 168 ms: 1.04x slower                                                  |
| comprehensions          | 24.3 us                                                                | 25.3 us: 1.04x slower                                                 |
| pprint_pformat          | 2.06 sec                                                               | 2.15 sec: 1.04x slower                                                |
| genshi_text             | 35.3 ms                                                                | 37.0 ms: 1.05x slower                                                 |
| many_optionals          | 1.49 ms                                                                | 1.56 ms: 1.05x slower                                                 |
| meteor_contest          | 172 ms                                                                 | 181 ms: 1.05x slower                                                  |
| connected_components    | 886 ms                                                                 | 935 ms: 1.06x slower                                                  |
| tomli_loads             | 2.72 sec                                                               | 2.88 sec: 1.06x slower                                                |
| deepcopy                | 383 us                                                                 | 405 us: 1.06x slower                                                  |
| sqlglot_v2_transpile    | 2.61 ms                                                                | 2.76 ms: 1.06x slower                                                 |
| generators              | 44.0 ms                                                                | 46.6 ms: 1.06x slower                                                 |
| mdp                     | 2.22 sec                                                               | 2.35 sec: 1.06x slower                                                |
| regex_v8                | 29.9 ms                                                                | 31.8 ms: 1.06x slower                                                 |
| async_tree_memoization  | 465 ms                                                                 | 495 ms: 1.06x slower                                                  |
| sphinx                  | 1.52 sec                                                               | 1.62 sec: 1.06x slower                                                |
| scimark_sparse_mat_mult | 6.82 ms                                                                | 7.27 ms: 1.07x slower                                                 |
| logging_silent          | 129 ns                                                                 | 138 ns: 1.07x slower                                                  |
| regex_effbot            | 3.96 ms                                                                | 4.24 ms: 1.07x slower                                                 |
| logging_format          | 9.98 us                                                                | 10.7 us: 1.07x slower                                                 |
| json_dumps              | 15.8 ms                                                                | 17.0 ms: 1.08x slower                                                 |
| regex_compile           | 178 ms                                                                 | 192 ms: 1.08x slower                                                  |
| spectral_norm           | 136 ms                                                                 | 147 ms: 1.08x slower                                                  |
| scimark_monte_carlo     | 98.7 ms                                                                | 106 ms: 1.08x slower                                                  |
| chaos                   | 80.5 ms                                                                | 87.0 ms: 1.08x slower                                                 |
| 2to3                    | 469 ms                                                                 | 511 ms: 1.09x slower                                                  |
| float                   | 92.0 ms                                                                | 100 ms: 1.09x slower                                                  |
| richards                | 64.3 ms                                                                | 70.2 ms: 1.09x slower                                                 |
| pickle_pure_python      | 454 us                                                                 | 497 us: 1.09x slower                                                  |
| telco                   | 11.0 ms                                                                | 12.1 ms: 1.10x slower                                                 |
| gc_traversal            | 3.73 ms                                                                | 4.14 ms: 1.11x slower                                                 |
| hexiom                  | 9.44 ms                                                                | 10.6 ms: 1.12x slower                                                 |
| coroutines              | 31.4 ms                                                                | 36.6 ms: 1.17x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (48): create_gc_cycles, genshi_xml, deltablue, mako, xml_etree_parse, go, sympy_integrate, logging_simple, pycparser, deepcopy_memo, sqlglot_v2_optimize, raytrace, typing_runtime_protocols, pprint_safe_repr, richards_super, nqueens, fannkuch, async_tree_cpu_io_mixed_tg, python_startup_no_site, async_tree_io_tg, async_tree_none_tg, subparsers, sympy_str, unpickle_pure_python, dulwich_log, pylint, scimark_fft, sympy_expand, shortest_path, pathlib, asyncio_websockets, bpe_tokeniser, pyflate, html5lib, async_generators, json_loads, coverage, async_tree_memoization_tg, async_tree_none, sympy_sum, crypto_pyaes, scimark_lu, async_tree_io, django_template, sqlite_synth, bench_mp_pool, xml_etree_iterparse, bench_thread_pool

- Geometric mean (including insignificant results): 1.010x slower

# HPT report

- Reliability score: 99.10% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x