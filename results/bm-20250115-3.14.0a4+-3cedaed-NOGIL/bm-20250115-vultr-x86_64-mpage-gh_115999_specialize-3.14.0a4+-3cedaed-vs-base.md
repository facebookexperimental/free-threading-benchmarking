# Results vs. base

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 3cedaed
- commit date: 2025-01-15
- overall geometric mean: 1.000x faster
- HPT reliability: 60.44%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| html5lib       | 70.8 ms                                                                | 70.0 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 346 ms                                                                 | 348 ms: 1.01x slower                                                  |
| async_tree_memoization_tg  | 306 ms                                                                 | 309 ms: 1.01x slower                                                  |
| async_tree_none_tg         | 237 ms                                                                 | 239 ms: 1.01x slower                                                  |
| async_tree_io              | 596 ms                                                                 | 602 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 500 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed    | 528 ms                                                                 | 539 ms: 1.02x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (4): async_tree_io_tg, async_tree_none, asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 133 ms                                                                 | 132 ms: 1.01x faster                                                  |
| pidigits       | 190 ms                                                                 | 193 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 185 ms: 1.02x slower                                                  |
| regex_effbot   | 2.82 ms                                                                | 2.92 ms: 1.04x slower                                                 |
| regex_v8       | 23.6 ms                                                                | 24.4 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 373 us                                                                 | 370 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 86.6 ms                                                                | 86.1 ms: 1.01x faster                                                 |
| unpickle_pure_python | 244 us                                                                 | 243 us: 1.01x faster                                                  |
| xml_etree_process    | 69.1 ms                                                                | 68.8 ms: 1.01x faster                                                 |
| xml_etree_generate   | 97.1 ms                                                                | 96.7 ms: 1.00x faster                                                 |
| tomli_loads          | 2.29 sec                                                               | 2.31 sec: 1.01x slower                                                |
| json_loads           | 30.2 us                                                                | 30.8 us: 1.02x slower                                                 |
| json_dumps           | 12.7 ms                                                                | 13.0 ms: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.2 ms: 1.00x faster                                                 |
| python_startup_no_site | 9.58 ms                                                                | 9.55 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 15.8 ms                                                                | 15.5 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): genshi_xml, genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| scimark_fft                | 396 ms                                                                 | 381 ms: 1.04x faster                                                  |
| logging_silent             | 114 ns                                                                 | 110 ns: 1.03x faster                                                  |
| pyflate                    | 496 ms                                                                 | 483 ms: 1.03x faster                                                  |
| scimark_lu                 | 139 ms                                                                 | 136 ms: 1.02x faster                                                  |
| fannkuch                   | 486 ms                                                                 | 475 ms: 1.02x faster                                                  |
| deepcopy_memo              | 39.1 us                                                                | 38.4 us: 1.02x faster                                                 |
| mako                       | 15.8 ms                                                                | 15.5 ms: 1.02x faster                                                 |
| gc_traversal               | 3.36 ms                                                                | 3.30 ms: 1.02x faster                                                 |
| create_gc_cycles           | 1.35 ms                                                                | 1.33 ms: 1.01x faster                                                 |
| hexiom                     | 7.37 ms                                                                | 7.26 ms: 1.01x faster                                                 |
| deepcopy_reduce            | 3.31 us                                                                | 3.27 us: 1.01x faster                                                 |
| raytrace                   | 327 ms                                                                 | 323 ms: 1.01x faster                                                  |
| html5lib                   | 70.8 ms                                                                | 70.0 ms: 1.01x faster                                                 |
| coverage                   | 98.1 ms                                                                | 96.9 ms: 1.01x faster                                                 |
| shortest_path              | 545 ms                                                                 | 538 ms: 1.01x faster                                                  |
| typing_runtime_protocols   | 204 us                                                                 | 202 us: 1.01x faster                                                  |
| deltablue                  | 4.61 ms                                                                | 4.57 ms: 1.01x faster                                                 |
| go                         | 137 ms                                                                 | 136 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.72 sec                                                               | 4.68 sec: 1.01x faster                                                |
| crypto_pyaes               | 87.7 ms                                                                | 86.9 ms: 1.01x faster                                                 |
| spectral_norm              | 115 ms                                                                 | 114 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 5.89 ms                                                                | 5.84 ms: 1.01x faster                                                 |
| pickle_pure_python         | 373 us                                                                 | 370 us: 1.01x faster                                                  |
| logging_format             | 8.50 us                                                                | 8.43 us: 1.01x faster                                                 |
| sympy_expand               | 552 ms                                                                 | 548 ms: 1.01x faster                                                  |
| nbody                      | 133 ms                                                                 | 132 ms: 1.01x faster                                                  |
| connected_components       | 488 ms                                                                 | 484 ms: 1.01x faster                                                  |
| bench_thread_pool          | 3.33 ms                                                                | 3.31 ms: 1.01x faster                                                 |
| scimark_monte_carlo        | 82.7 ms                                                                | 82.2 ms: 1.01x faster                                                 |
| xml_etree_iterparse        | 86.6 ms                                                                | 86.1 ms: 1.01x faster                                                 |
| chaos                      | 71.0 ms                                                                | 70.6 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 244 us                                                                 | 243 us: 1.01x faster                                                  |
| xml_etree_process          | 69.1 ms                                                                | 68.8 ms: 1.01x faster                                                 |
| xml_etree_generate         | 97.1 ms                                                                | 96.7 ms: 1.00x faster                                                 |
| python_startup             | 15.3 ms                                                                | 15.2 ms: 1.00x faster                                                 |
| python_startup_no_site     | 9.58 ms                                                                | 9.55 ms: 1.00x faster                                                 |
| sqlglot_normalize          | 121 ms                                                                 | 121 ms: 1.00x faster                                                  |
| sqlalchemy_declarative     | 163 ms                                                                 | 163 ms: 1.00x faster                                                  |
| deepcopy                   | 313 us                                                                 | 314 us: 1.01x slower                                                  |
| scimark_sor                | 131 ms                                                                 | 131 ms: 1.01x slower                                                  |
| async_tree_memoization     | 346 ms                                                                 | 348 ms: 1.01x slower                                                  |
| richards_super             | 63.7 ms                                                                | 64.2 ms: 1.01x slower                                                 |
| logging_simple             | 7.34 us                                                                | 7.40 us: 1.01x slower                                                 |
| tomli_loads                | 2.29 sec                                                               | 2.31 sec: 1.01x slower                                                |
| comprehensions             | 20.7 us                                                                | 20.9 us: 1.01x slower                                                 |
| nqueens                    | 95.9 ms                                                                | 96.8 ms: 1.01x slower                                                 |
| pprint_safe_repr           | 821 ms                                                                 | 829 ms: 1.01x slower                                                  |
| async_tree_memoization_tg  | 306 ms                                                                 | 309 ms: 1.01x slower                                                  |
| json                       | 5.29 ms                                                                | 5.35 ms: 1.01x slower                                                 |
| async_tree_none_tg         | 237 ms                                                                 | 239 ms: 1.01x slower                                                  |
| async_tree_io              | 596 ms                                                                 | 602 ms: 1.01x slower                                                  |
| pprint_pformat             | 1.68 sec                                                               | 1.70 sec: 1.01x slower                                                |
| thrift                     | 907 us                                                                 | 920 us: 1.01x slower                                                  |
| pidigits                   | 190 ms                                                                 | 193 ms: 1.01x slower                                                  |
| regex_dna                  | 182 ms                                                                 | 185 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 500 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed    | 528 ms                                                                 | 539 ms: 1.02x slower                                                  |
| json_loads                 | 30.2 us                                                                | 30.8 us: 1.02x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| json_dumps                 | 12.7 ms                                                                | 13.0 ms: 1.02x slower                                                 |
| regex_effbot               | 2.82 ms                                                                | 2.92 ms: 1.04x slower                                                 |
| regex_v8                   | 23.6 ms                                                                | 24.4 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (34): xml_etree_parse, meteor_contest, bench_mp_pool, docutils, genshi_xml, pylint, async_tree_io_tg, sympy_integrate, sqlglot_optimize, float, dulwich_log, subparsers, 2to3, sphinx, richards, async_tree_none, asyncio_websockets, mdp, genshi_text, async_generators, sqlite_synth, k_core, pycparser, telco, sympy_str, regex_compile, sqlglot_parse, generators, sympy_sum, sqlglot_transpile, many_optionals, sqlalchemy_imperative, pathlib, django_template

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 60.44% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x