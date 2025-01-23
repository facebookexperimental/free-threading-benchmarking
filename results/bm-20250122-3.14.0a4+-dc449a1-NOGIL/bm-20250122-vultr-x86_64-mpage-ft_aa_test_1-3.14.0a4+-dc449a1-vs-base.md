# Results vs. base

- fork: mpage
- ref: ft_aa_test_1
- machine: linux-x86_64
- commit hash: dc449a1
- commit date: 2025-01-22
- overall geometric mean: 1.002x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4+-24c84d8 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 312 ms                                                                 | 314 ms: 1.01x slower                                          |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                  |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4+-24c84d8 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 509 ms                                                                 | 502 ms: 1.02x faster                                          |
| async_tree_cpu_io_mixed    | 546 ms                                                                 | 538 ms: 1.01x faster                                          |
| async_generators           | 381 ms                                                                 | 378 ms: 1.01x faster                                          |
| coroutines                 | 24.9 ms                                                                | 25.0 ms: 1.00x slower                                         |
| async_tree_io              | 615 ms                                                                 | 620 ms: 1.01x slower                                          |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (6): async_tree_none, async_tree_none_tg, asyncio_websockets, async_tree_memoization, async_tree_memoization_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4+-24c84d8 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 197 ms                                                                 | 190 ms: 1.04x faster                                          |
| nbody          | 140 ms                                                                 | 136 ms: 1.03x faster                                          |
| float          | 78.3 ms                                                                | 77.5 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4+-24c84d8 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 2.96 ms                                                                | 2.89 ms: 1.02x faster                                         |
| regex_dna      | 183 ms                                                                 | 181 ms: 1.01x faster                                          |
| regex_v8       | 24.4 ms                                                                | 24.6 ms: 1.01x slower                                         |
| regex_compile  | 157 ms                                                                 | 159 ms: 1.01x slower                                          |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4+-24c84d8 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| json_dumps           | 12.9 ms                                                                | 13.0 ms: 1.00x slower                                         |
| json_loads           | 30.3 us                                                                | 30.4 us: 1.00x slower                                         |
| pickle_pure_python   | 393 us                                                                 | 395 us: 1.01x slower                                          |
| xml_etree_iterparse  | 88.1 ms                                                                | 88.7 ms: 1.01x slower                                         |
| xml_etree_generate   | 98.5 ms                                                                | 99.3 ms: 1.01x slower                                         |
| tomli_loads          | 2.41 sec                                                               | 2.43 sec: 1.01x slower                                        |
| unpickle_pure_python | 272 us                                                                 | 275 us: 1.01x slower                                          |
| xml_etree_process    | 74.7 ms                                                                | 77.1 ms: 1.03x slower                                         |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                  |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4+-24c84d8 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| mako            | 16.2 ms                                                                | 16.3 ms: 1.01x slower                                         |
| genshi_xml      | 63.6 ms                                                                | 64.0 ms: 1.01x slower                                         |
| django_template | 44.5 ms                                                                | 45.0 ms: 1.01x slower                                         |
| genshi_text     | 29.9 ms                                                                | 30.3 ms: 1.01x slower                                         |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20250122-vultr-x86_64-python-24c84d816f2f2ecb76b8-3.14.0a4+-24c84d8 | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------:|
| gc_traversal               | 3.34 ms                                                                | 3.13 ms: 1.07x faster                                         |
| scimark_sparse_mat_mult    | 5.68 ms                                                                | 5.43 ms: 1.05x faster                                         |
| pidigits                   | 197 ms                                                                 | 190 ms: 1.04x faster                                          |
| sqlite_synth               | 2.12 us                                                                | 2.05 us: 1.03x faster                                         |
| scimark_fft                | 393 ms                                                                 | 382 ms: 1.03x faster                                          |
| nbody                      | 140 ms                                                                 | 136 ms: 1.03x faster                                          |
| regex_effbot               | 2.96 ms                                                                | 2.89 ms: 1.02x faster                                         |
| telco                      | 8.71 ms                                                                | 8.50 ms: 1.02x faster                                         |
| scimark_sor                | 142 ms                                                                 | 139 ms: 1.02x faster                                          |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                 | 502 ms: 1.02x faster                                          |
| crypto_pyaes               | 88.2 ms                                                                | 86.9 ms: 1.01x faster                                         |
| async_tree_cpu_io_mixed    | 546 ms                                                                 | 538 ms: 1.01x faster                                          |
| float                      | 78.3 ms                                                                | 77.5 ms: 1.01x faster                                         |
| async_generators           | 381 ms                                                                 | 378 ms: 1.01x faster                                          |
| regex_dna                  | 183 ms                                                                 | 181 ms: 1.01x faster                                          |
| create_gc_cycles           | 1.32 ms                                                                | 1.31 ms: 1.01x faster                                         |
| coroutines                 | 24.9 ms                                                                | 25.0 ms: 1.00x slower                                         |
| deepcopy_reduce            | 3.38 us                                                                | 3.39 us: 1.00x slower                                         |
| mdp                        | 2.67 sec                                                               | 2.68 sec: 1.00x slower                                        |
| json_dumps                 | 12.9 ms                                                                | 13.0 ms: 1.00x slower                                         |
| sqlglot_optimize           | 62.4 ms                                                                | 62.7 ms: 1.00x slower                                         |
| json_loads                 | 30.3 us                                                                | 30.4 us: 1.00x slower                                         |
| mako                       | 16.2 ms                                                                | 16.3 ms: 1.01x slower                                         |
| go                         | 144 ms                                                                 | 145 ms: 1.01x slower                                          |
| regex_v8                   | 24.4 ms                                                                | 24.6 ms: 1.01x slower                                         |
| pickle_pure_python         | 393 us                                                                 | 395 us: 1.01x slower                                          |
| 2to3                       | 312 ms                                                                 | 314 ms: 1.01x slower                                          |
| chaos                      | 71.1 ms                                                                | 71.6 ms: 1.01x slower                                         |
| xml_etree_iterparse        | 88.1 ms                                                                | 88.7 ms: 1.01x slower                                         |
| genshi_xml                 | 63.6 ms                                                                | 64.0 ms: 1.01x slower                                         |
| fannkuch                   | 493 ms                                                                 | 497 ms: 1.01x slower                                          |
| xml_etree_generate         | 98.5 ms                                                                | 99.3 ms: 1.01x slower                                         |
| async_tree_io              | 615 ms                                                                 | 620 ms: 1.01x slower                                          |
| thrift                     | 918 us                                                                 | 925 us: 1.01x slower                                          |
| tomli_loads                | 2.41 sec                                                               | 2.43 sec: 1.01x slower                                        |
| sympy_expand               | 562 ms                                                                 | 567 ms: 1.01x slower                                          |
| pycparser                  | 1.23 sec                                                               | 1.24 sec: 1.01x slower                                        |
| sqlglot_normalize          | 123 ms                                                                 | 125 ms: 1.01x slower                                          |
| scimark_lu                 | 139 ms                                                                 | 141 ms: 1.01x slower                                          |
| pprint_pformat             | 1.75 sec                                                               | 1.77 sec: 1.01x slower                                        |
| scimark_monte_carlo        | 82.8 ms                                                                | 83.7 ms: 1.01x slower                                         |
| pyflate                    | 509 ms                                                                 | 515 ms: 1.01x slower                                          |
| unpickle_pure_python       | 272 us                                                                 | 275 us: 1.01x slower                                          |
| bpe_tokeniser              | 4.77 sec                                                               | 4.82 sec: 1.01x slower                                        |
| raytrace                   | 334 ms                                                                 | 338 ms: 1.01x slower                                          |
| django_template            | 44.5 ms                                                                | 45.0 ms: 1.01x slower                                         |
| genshi_text                | 29.9 ms                                                                | 30.3 ms: 1.01x slower                                         |
| sympy_integrate            | 24.7 ms                                                                | 25.0 ms: 1.01x slower                                         |
| spectral_norm              | 111 ms                                                                 | 112 ms: 1.01x slower                                          |
| regex_compile              | 157 ms                                                                 | 159 ms: 1.01x slower                                          |
| sympy_str                  | 342 ms                                                                 | 347 ms: 1.01x slower                                          |
| pprint_safe_repr           | 846 ms                                                                 | 858 ms: 1.02x slower                                          |
| logging_silent             | 119 ns                                                                 | 121 ns: 1.02x slower                                          |
| hexiom                     | 7.55 ms                                                                | 7.67 ms: 1.02x slower                                         |
| deepcopy_memo              | 40.3 us                                                                | 41.0 us: 1.02x slower                                         |
| richards                   | 56.3 ms                                                                | 57.3 ms: 1.02x slower                                         |
| logging_simple             | 7.68 us                                                                | 7.82 us: 1.02x slower                                         |
| sympy_sum                  | 190 ms                                                                 | 193 ms: 1.02x slower                                          |
| deltablue                  | 4.69 ms                                                                | 4.78 ms: 1.02x slower                                         |
| generators                 | 33.2 ms                                                                | 33.9 ms: 1.02x slower                                         |
| logging_format             | 8.71 us                                                                | 8.90 us: 1.02x slower                                         |
| deepcopy                   | 323 us                                                                 | 330 us: 1.02x slower                                          |
| richards_super             | 65.9 ms                                                                | 67.7 ms: 1.03x slower                                         |
| nqueens                    | 98.4 ms                                                                | 101 ms: 1.03x slower                                          |
| typing_runtime_protocols   | 208 us                                                                 | 214 us: 1.03x slower                                          |
| xml_etree_process          | 74.7 ms                                                                | 77.1 ms: 1.03x slower                                         |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                  |

Benchmark hidden because not significant (30): json, subparsers, sqlalchemy_declarative, shortest_path, async_tree_none, coverage, pathlib, async_tree_none_tg, connected_components, bench_thread_pool, comprehensions, python_startup, sqlglot_parse, xml_etree_parse, bench_mp_pool, python_startup_no_site, asyncio_websockets, many_optionals, k_core, html5lib, dulwich_log, async_tree_memoization, sqlalchemy_imperative, pylint, sphinx, sqlglot_transpile, async_tree_memoization_tg, docutils, meteor_contest, async_tree_io_tg

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x