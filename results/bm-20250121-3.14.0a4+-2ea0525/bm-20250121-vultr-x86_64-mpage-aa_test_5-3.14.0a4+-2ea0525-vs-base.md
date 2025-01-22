# Results vs. base

- fork: mpage
- ref: aa_test_5
- machine: linux-x86_64
- commit hash: 2ea0525
- commit date: 2025-01-21
- overall geometric mean: 1.001x faster
- HPT reliability: 97.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4+-767cf70 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 255 ms: 1.00x faster                                       |
| Geometric mean | (ref)                                                                  | 1.00x faster                                               |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4+-767cf70 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 497 ms                                                                 | 486 ms: 1.02x faster                                       |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 476 ms: 1.02x faster                                       |
| async_tree_io_tg           | 622 ms                                                                 | 613 ms: 1.02x faster                                       |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                               |

Benchmark hidden because not significant (8): async_tree_io, async_tree_none, async_tree_memoization, async_generators, coroutines, async_tree_memoization_tg, asyncio_websockets, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4+-767cf70 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 231 ms                                                                 | 192 ms: 1.20x faster                                       |
| nbody          | 90.5 ms                                                                | 93.1 ms: 1.03x slower                                      |
| Geometric mean | (ref)                                                                  | 1.05x faster                                               |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4+-767cf70 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_dna      | 169 ms                                                                 | 174 ms: 1.03x slower                                       |
| regex_effbot   | 2.57 ms                                                                | 2.73 ms: 1.06x slower                                      |
| Geometric mean | (ref)                                                                  | 1.02x slower                                               |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4+-767cf70 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_process    | 61.2 ms                                                                | 60.6 ms: 1.01x faster                                      |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.01x faster                                       |
| xml_etree_iterparse  | 91.0 ms                                                                | 90.6 ms: 1.00x faster                                      |
| xml_etree_generate   | 83.1 ms                                                                | 83.5 ms: 1.00x slower                                      |
| json_loads           | 27.7 us                                                                | 27.9 us: 1.01x slower                                      |
| unpickle_pure_python | 221 us                                                                 | 225 us: 1.02x slower                                       |
| json_dumps           | 11.3 ms                                                                | 11.5 ms: 1.02x slower                                      |
| pickle_pure_python   | 314 us                                                                 | 322 us: 1.03x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4+-767cf70 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup | 14.7 ms                                                                | 14.6 ms: 1.00x faster                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                               |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): mako, genshi_xml, genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20250122-vultr-x86_64-python-767cf708449fbf13826d-3.14.0a4+-767cf70 | bm-20250121-vultr-x86_64-mpage-aa_test_5-3.14.0a4+-2ea0525 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits                   | 231 ms                                                                 | 192 ms: 1.20x faster                                       |
| async_tree_cpu_io_mixed    | 497 ms                                                                 | 486 ms: 1.02x faster                                       |
| scimark_fft                | 311 ms                                                                 | 305 ms: 1.02x faster                                       |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 476 ms: 1.02x faster                                       |
| spectral_norm              | 92.9 ms                                                                | 91.5 ms: 1.02x faster                                      |
| async_tree_io_tg           | 622 ms                                                                 | 613 ms: 1.02x faster                                       |
| telco                      | 7.40 ms                                                                | 7.29 ms: 1.01x faster                                      |
| gc_traversal               | 4.29 ms                                                                | 4.23 ms: 1.01x faster                                      |
| pyflate                    | 424 ms                                                                 | 419 ms: 1.01x faster                                       |
| xml_etree_process          | 61.2 ms                                                                | 60.6 ms: 1.01x faster                                      |
| dulwich_log                | 76.6 ms                                                                | 75.9 ms: 1.01x faster                                      |
| logging_simple             | 6.50 us                                                                | 6.44 us: 1.01x faster                                      |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.01x faster                                       |
| logging_format             | 7.21 us                                                                | 7.15 us: 1.01x faster                                      |
| sqlglot_transpile          | 1.57 ms                                                                | 1.56 ms: 1.01x faster                                      |
| sympy_integrate            | 20.0 ms                                                                | 19.8 ms: 1.01x faster                                      |
| bench_thread_pool          | 1.04 ms                                                                | 1.03 ms: 1.01x faster                                      |
| sympy_sum                  | 154 ms                                                                 | 153 ms: 1.00x faster                                       |
| sqlglot_parse              | 1.26 ms                                                                | 1.26 ms: 1.00x faster                                      |
| shortest_path              | 431 ms                                                                 | 429 ms: 1.00x faster                                       |
| coverage                   | 79.8 ms                                                                | 79.5 ms: 1.00x faster                                      |
| xml_etree_iterparse        | 91.0 ms                                                                | 90.6 ms: 1.00x faster                                      |
| sqlalchemy_declarative     | 131 ms                                                                 | 130 ms: 1.00x faster                                       |
| chaos                      | 56.1 ms                                                                | 55.8 ms: 1.00x faster                                      |
| nqueens                    | 77.9 ms                                                                | 77.7 ms: 1.00x faster                                      |
| python_startup             | 14.7 ms                                                                | 14.6 ms: 1.00x faster                                      |
| sqlglot_optimize           | 52.7 ms                                                                | 52.6 ms: 1.00x faster                                      |
| raytrace                   | 267 ms                                                                 | 266 ms: 1.00x faster                                       |
| 2to3                       | 256 ms                                                                 | 255 ms: 1.00x faster                                       |
| mdp                        | 2.29 sec                                                               | 2.30 sec: 1.00x slower                                     |
| go                         | 115 ms                                                                 | 115 ms: 1.00x slower                                       |
| deepcopy_reduce            | 2.58 us                                                                | 2.59 us: 1.00x slower                                      |
| xml_etree_generate         | 83.1 ms                                                                | 83.5 ms: 1.00x slower                                      |
| many_optionals             | 1.04 ms                                                                | 1.04 ms: 1.00x slower                                      |
| logging_silent             | 104 ns                                                                 | 104 ns: 1.01x slower                                       |
| scimark_sor                | 113 ms                                                                 | 114 ms: 1.01x slower                                       |
| thrift                     | 746 us                                                                 | 753 us: 1.01x slower                                       |
| pprint_pformat             | 1.42 sec                                                               | 1.43 sec: 1.01x slower                                     |
| json_loads                 | 27.7 us                                                                | 27.9 us: 1.01x slower                                      |
| meteor_contest             | 97.4 ms                                                                | 98.4 ms: 1.01x slower                                      |
| fannkuch                   | 368 ms                                                                 | 372 ms: 1.01x slower                                       |
| pprint_safe_repr           | 695 ms                                                                 | 703 ms: 1.01x slower                                       |
| generators                 | 27.4 ms                                                                | 27.8 ms: 1.01x slower                                      |
| crypto_pyaes               | 68.3 ms                                                                | 69.1 ms: 1.01x slower                                      |
| deltablue                  | 3.09 ms                                                                | 3.13 ms: 1.01x slower                                      |
| unpickle_pure_python       | 221 us                                                                 | 225 us: 1.02x slower                                       |
| json_dumps                 | 11.3 ms                                                                | 11.5 ms: 1.02x slower                                      |
| typing_runtime_protocols   | 156 us                                                                 | 160 us: 1.02x slower                                       |
| pickle_pure_python         | 314 us                                                                 | 322 us: 1.03x slower                                       |
| nbody                      | 90.5 ms                                                                | 93.1 ms: 1.03x slower                                      |
| regex_dna                  | 169 ms                                                                 | 174 ms: 1.03x slower                                       |
| regex_effbot               | 2.57 ms                                                                | 2.73 ms: 1.06x slower                                      |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                               |

Benchmark hidden because not significant (43): async_tree_io, sympy_expand, async_tree_none, regex_compile, connected_components, async_tree_memoization, docutils, pylint, mako, scimark_monte_carlo, sphinx, async_generators, coroutines, k_core, scimark_lu, hexiom, json, bpe_tokeniser, async_tree_memoization_tg, python_startup_no_site, genshi_xml, asyncio_websockets, sqlite_synth, float, deepcopy, richards, pycparser, sqlglot_normalize, comprehensions, subparsers, create_gc_cycles, bench_mp_pool, tomli_loads, sympy_str, async_tree_none_tg, deepcopy_memo, sqlalchemy_imperative, scimark_sparse_mat_mult, genshi_text, richards_super, regex_v8, django_template, pathlib

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 97.86% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x