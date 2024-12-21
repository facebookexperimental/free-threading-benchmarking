# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: d6d4c73
- commit date: 2024-12-20
- overall geometric mean: 1.010x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 255 ms: 1.00x faster                                                  |
| sphinx         | 989 ms                                                                 | 984 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 475 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 493 ms: 1.15x faster                                                  |
| coroutines                 | 22.2 ms                                                                | 21.8 ms: 1.02x faster                                                 |
| async_tree_io              | 624 ms                                                                 | 614 ms: 1.02x faster                                                  |
| async_generators           | 357 ms                                                                 | 355 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, asyncio_websockets, async_tree_io_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 185 ms: 1.17x faster                                                  |
| nbody          | 91.1 ms                                                                | 88.2 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.81 ms                                                                | 2.72 ms: 1.03x faster                                                 |
| regex_dna      | 181 ms                                                                 | 176 ms: 1.03x faster                                                  |
| regex_v8       | 25.0 ms                                                                | 24.4 ms: 1.02x faster                                                 |
| regex_compile  | 127 ms                                                                 | 126 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 316 us                                                                 | 312 us: 1.01x faster                                                  |
| unpickle_pure_python | 213 us                                                                 | 210 us: 1.01x faster                                                  |
| xml_etree_process    | 57.9 ms                                                                | 57.5 ms: 1.01x faster                                                 |
| xml_etree_generate   | 82.9 ms                                                                | 83.3 ms: 1.01x slower                                                 |
| tomli_loads          | 1.90 sec                                                               | 1.93 sec: 1.02x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (4): json_loads, xml_etree_parse, json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                 |
| python_startup_no_site | 7.48 ms                                                                | 7.52 ms: 1.01x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.4 ms                                                                | 21.1 ms: 1.01x faster                                                 |
| genshi_xml     | 48.9 ms                                                                | 48.4 ms: 1.01x faster                                                 |
| mako           | 11.5 ms                                                                | 11.8 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                                 | 185 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 475 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 493 ms: 1.15x faster                                                  |
| scimark_sor                | 117 ms                                                                 | 112 ms: 1.04x faster                                                  |
| regex_effbot               | 2.81 ms                                                                | 2.72 ms: 1.03x faster                                                 |
| nbody                      | 91.1 ms                                                                | 88.2 ms: 1.03x faster                                                 |
| deltablue                  | 3.17 ms                                                                | 3.08 ms: 1.03x faster                                                 |
| regex_dna                  | 181 ms                                                                 | 176 ms: 1.03x faster                                                  |
| go                         | 116 ms                                                                 | 114 ms: 1.02x faster                                                  |
| regex_v8                   | 25.0 ms                                                                | 24.4 ms: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 4.26 ms                                                                | 4.18 ms: 1.02x faster                                                 |
| coroutines                 | 22.2 ms                                                                | 21.8 ms: 1.02x faster                                                 |
| scimark_monte_carlo        | 63.4 ms                                                                | 62.3 ms: 1.02x faster                                                 |
| gc_traversal               | 4.37 ms                                                                | 4.30 ms: 1.02x faster                                                 |
| sqlglot_parse              | 1.26 ms                                                                | 1.24 ms: 1.02x faster                                                 |
| deepcopy_memo              | 30.1 us                                                                | 29.7 us: 1.02x faster                                                 |
| spectral_norm              | 97.3 ms                                                                | 95.8 ms: 1.02x faster                                                 |
| chaos                      | 58.9 ms                                                                | 58.0 ms: 1.02x faster                                                 |
| async_tree_io              | 624 ms                                                                 | 614 ms: 1.02x faster                                                  |
| raytrace                   | 260 ms                                                                 | 256 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 157 us                                                                 | 155 us: 1.02x faster                                                  |
| connected_components       | 394 ms                                                                 | 388 ms: 1.02x faster                                                  |
| telco                      | 7.25 ms                                                                | 7.15 ms: 1.02x faster                                                 |
| logging_simple             | 5.95 us                                                                | 5.87 us: 1.01x faster                                                 |
| pickle_pure_python         | 316 us                                                                 | 312 us: 1.01x faster                                                  |
| genshi_text                | 21.4 ms                                                                | 21.1 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 213 us                                                                 | 210 us: 1.01x faster                                                  |
| scimark_lu                 | 111 ms                                                                 | 110 ms: 1.01x faster                                                  |
| pyflate                    | 419 ms                                                                 | 414 ms: 1.01x faster                                                  |
| logging_silent             | 106 ns                                                                 | 105 ns: 1.01x faster                                                  |
| bpe_tokeniser              | 4.28 sec                                                               | 4.23 sec: 1.01x faster                                                |
| genshi_xml                 | 48.9 ms                                                                | 48.4 ms: 1.01x faster                                                 |
| comprehensions             | 17.0 us                                                                | 16.8 us: 1.01x faster                                                 |
| sqlglot_transpile          | 1.56 ms                                                                | 1.55 ms: 1.01x faster                                                 |
| thrift                     | 739 us                                                                 | 734 us: 1.01x faster                                                  |
| sqlalchemy_declarative     | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| sqlalchemy_imperative      | 19.4 ms                                                                | 19.2 ms: 1.01x faster                                                 |
| scimark_fft                | 313 ms                                                                 | 311 ms: 1.01x faster                                                  |
| xml_etree_process          | 57.9 ms                                                                | 57.5 ms: 1.01x faster                                                 |
| richards                   | 42.3 ms                                                                | 42.0 ms: 1.01x faster                                                 |
| mdp                        | 2.34 sec                                                               | 2.33 sec: 1.01x faster                                                |
| sphinx                     | 989 ms                                                                 | 984 ms: 1.01x faster                                                  |
| regex_compile              | 127 ms                                                                 | 126 ms: 1.00x faster                                                  |
| 2to3                       | 256 ms                                                                 | 255 ms: 1.00x faster                                                  |
| hexiom                     | 5.88 ms                                                                | 5.85 ms: 1.00x faster                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 1.03 ms: 1.00x faster                                                 |
| async_generators           | 357 ms                                                                 | 355 ms: 1.00x faster                                                  |
| many_optionals             | 1.03 ms                                                                | 1.03 ms: 1.00x faster                                                 |
| crypto_pyaes               | 67.5 ms                                                                | 67.3 ms: 1.00x faster                                                 |
| sympy_integrate            | 19.8 ms                                                                | 19.8 ms: 1.00x faster                                                 |
| python_startup             | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                 |
| xml_etree_generate         | 82.9 ms                                                                | 83.3 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.48 ms                                                                | 7.52 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.44 sec                                                               | 1.45 sec: 1.01x slower                                                |
| nqueens                    | 77.7 ms                                                                | 78.1 ms: 1.01x slower                                                 |
| pycparser                  | 1.11 sec                                                               | 1.12 sec: 1.01x slower                                                |
| dulwich_log                | 74.3 ms                                                                | 75.0 ms: 1.01x slower                                                 |
| meteor_contest             | 98.9 ms                                                                | 99.8 ms: 1.01x slower                                                 |
| pathlib                    | 17.9 ms                                                                | 18.1 ms: 1.01x slower                                                 |
| fannkuch                   | 365 ms                                                                 | 370 ms: 1.01x slower                                                  |
| subparsers                 | 21.6 ms                                                                | 21.9 ms: 1.02x slower                                                 |
| tomli_loads                | 1.90 sec                                                               | 1.93 sec: 1.02x slower                                                |
| mako                       | 11.5 ms                                                                | 11.8 ms: 1.03x slower                                                 |
| generators                 | 27.1 ms                                                                | 27.9 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (31): pylint, json, json_loads, k_core, float, async_tree_memoization_tg, async_tree_none_tg, deepcopy, docutils, richards_super, sympy_expand, async_tree_memoization, shortest_path, sqlglot_optimize, sqlite_synth, coverage, asyncio_websockets, logging_format, sympy_sum, sympy_str, async_tree_io_tg, sqlglot_normalize, django_template, xml_etree_parse, pprint_safe_repr, async_tree_none, deepcopy_reduce, json_dumps, xml_etree_iterparse, bench_mp_pool, create_gc_cycles

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x