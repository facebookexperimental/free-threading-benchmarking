# Results vs. base

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 73aa5a2
- commit date: 2025-01-15
- overall geometric mean: 1.004x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 304 ms                                                                 | 305 ms: 1.00x slower                                                  |
| html5lib       | 70.8 ms                                                                | 68.8 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg | 306 ms                                                                 | 309 ms: 1.01x slower                                                  |
| async_generators          | 369 ms                                                                 | 373 ms: 1.01x slower                                                  |
| async_tree_memoization    | 346 ms                                                                 | 350 ms: 1.01x slower                                                  |
| async_tree_io             | 596 ms                                                                 | 604 ms: 1.01x slower                                                  |
| coroutines                | 23.3 ms                                                                | 23.9 ms: 1.03x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (6): asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 133 ms                                                                 | 130 ms: 1.03x faster                                                  |
| float          | 77.3 ms                                                                | 76.9 ms: 1.00x faster                                                 |
| pidigits       | 190 ms                                                                 | 193 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 182 ms: 1.00x slower                                                  |
| regex_compile  | 149 ms                                                                 | 150 ms: 1.00x slower                                                  |
| regex_effbot   | 2.82 ms                                                                | 2.84 ms: 1.01x slower                                                 |
| regex_v8       | 23.6 ms                                                                | 24.6 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 373 us                                                                 | 371 us: 1.01x faster                                                  |
| json_dumps           | 12.7 ms                                                                | 12.8 ms: 1.01x slower                                                 |
| xml_etree_process    | 69.1 ms                                                                | 69.6 ms: 1.01x slower                                                 |
| tomli_loads          | 2.29 sec                                                               | 2.32 sec: 1.01x slower                                                |
| json_loads           | 30.2 us                                                                | 30.7 us: 1.02x slower                                                 |
| unpickle_pure_python | 244 us                                                                 | 250 us: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.58 ms                                                                | 9.52 ms: 1.01x faster                                                 |
| python_startup         | 15.3 ms                                                                | 15.2 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                 |
| django_template | 43.4 ms                                                                | 43.6 ms: 1.01x slower                                                 |
| genshi_text     | 27.9 ms                                                                | 28.3 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| scimark_sparse_mat_mult   | 5.89 ms                                                                | 5.71 ms: 1.03x faster                                                 |
| html5lib                  | 70.8 ms                                                                | 68.8 ms: 1.03x faster                                                 |
| nbody                     | 133 ms                                                                 | 130 ms: 1.03x faster                                                  |
| logging_format            | 8.50 us                                                                | 8.28 us: 1.03x faster                                                 |
| scimark_fft               | 396 ms                                                                 | 387 ms: 1.02x faster                                                  |
| create_gc_cycles          | 1.35 ms                                                                | 1.32 ms: 1.02x faster                                                 |
| pyflate                   | 496 ms                                                                 | 486 ms: 1.02x faster                                                  |
| fannkuch                  | 486 ms                                                                 | 479 ms: 1.01x faster                                                  |
| telco                     | 8.52 ms                                                                | 8.42 ms: 1.01x faster                                                 |
| deepcopy_memo             | 39.1 us                                                                | 38.7 us: 1.01x faster                                                 |
| shortest_path             | 545 ms                                                                 | 540 ms: 1.01x faster                                                  |
| logging_simple            | 7.34 us                                                                | 7.28 us: 1.01x faster                                                 |
| sympy_expand              | 552 ms                                                                 | 548 ms: 1.01x faster                                                  |
| python_startup_no_site    | 9.58 ms                                                                | 9.52 ms: 1.01x faster                                                 |
| scimark_monte_carlo       | 82.7 ms                                                                | 82.3 ms: 1.01x faster                                                 |
| raytrace                  | 327 ms                                                                 | 325 ms: 1.01x faster                                                  |
| python_startup            | 15.3 ms                                                                | 15.2 ms: 1.01x faster                                                 |
| coverage                  | 98.1 ms                                                                | 97.6 ms: 1.01x faster                                                 |
| mako                      | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                 |
| pickle_pure_python        | 373 us                                                                 | 371 us: 1.01x faster                                                  |
| float                     | 77.3 ms                                                                | 76.9 ms: 1.00x faster                                                 |
| regex_dna                 | 182 ms                                                                 | 182 ms: 1.00x slower                                                  |
| 2to3                      | 304 ms                                                                 | 305 ms: 1.00x slower                                                  |
| bpe_tokeniser             | 4.72 sec                                                               | 4.73 sec: 1.00x slower                                                |
| regex_compile             | 149 ms                                                                 | 150 ms: 1.00x slower                                                  |
| deepcopy                  | 313 us                                                                 | 314 us: 1.00x slower                                                  |
| django_template           | 43.4 ms                                                                | 43.6 ms: 1.01x slower                                                 |
| scimark_lu                | 139 ms                                                                 | 140 ms: 1.01x slower                                                  |
| json                      | 5.29 ms                                                                | 5.32 ms: 1.01x slower                                                 |
| go                        | 137 ms                                                                 | 138 ms: 1.01x slower                                                  |
| json_dumps                | 12.7 ms                                                                | 12.8 ms: 1.01x slower                                                 |
| sympy_sum                 | 187 ms                                                                 | 188 ms: 1.01x slower                                                  |
| many_optionals            | 1.18 ms                                                                | 1.19 ms: 1.01x slower                                                 |
| regex_effbot              | 2.82 ms                                                                | 2.84 ms: 1.01x slower                                                 |
| richards                  | 55.2 ms                                                                | 55.6 ms: 1.01x slower                                                 |
| sqlglot_normalize         | 121 ms                                                                 | 122 ms: 1.01x slower                                                  |
| xml_etree_process         | 69.1 ms                                                                | 69.6 ms: 1.01x slower                                                 |
| pathlib                   | 18.7 ms                                                                | 18.8 ms: 1.01x slower                                                 |
| async_tree_memoization_tg | 306 ms                                                                 | 309 ms: 1.01x slower                                                  |
| sqlglot_parse             | 1.57 ms                                                                | 1.58 ms: 1.01x slower                                                 |
| sympy_integrate           | 24.2 ms                                                                | 24.4 ms: 1.01x slower                                                 |
| sympy_str                 | 335 ms                                                                 | 338 ms: 1.01x slower                                                  |
| deltablue                 | 4.61 ms                                                                | 4.66 ms: 1.01x slower                                                 |
| tomli_loads               | 2.29 sec                                                               | 2.32 sec: 1.01x slower                                                |
| async_generators          | 369 ms                                                                 | 373 ms: 1.01x slower                                                  |
| pprint_pformat            | 1.68 sec                                                               | 1.70 sec: 1.01x slower                                                |
| pycparser                 | 1.19 sec                                                               | 1.20 sec: 1.01x slower                                                |
| async_tree_memoization    | 346 ms                                                                 | 350 ms: 1.01x slower                                                  |
| sqlglot_transpile         | 1.90 ms                                                                | 1.92 ms: 1.01x slower                                                 |
| subparsers                | 25.6 ms                                                                | 25.9 ms: 1.01x slower                                                 |
| logging_silent            | 114 ns                                                                 | 116 ns: 1.01x slower                                                  |
| spectral_norm             | 115 ms                                                                 | 117 ms: 1.01x slower                                                  |
| pidigits                  | 190 ms                                                                 | 193 ms: 1.01x slower                                                  |
| async_tree_io             | 596 ms                                                                 | 604 ms: 1.01x slower                                                  |
| genshi_text               | 27.9 ms                                                                | 28.3 ms: 1.01x slower                                                 |
| nqueens                   | 95.9 ms                                                                | 97.3 ms: 1.02x slower                                                 |
| json_loads                | 30.2 us                                                                | 30.7 us: 1.02x slower                                                 |
| scimark_sor               | 131 ms                                                                 | 133 ms: 1.02x slower                                                  |
| comprehensions            | 20.7 us                                                                | 21.2 us: 1.02x slower                                                 |
| meteor_contest            | 130 ms                                                                 | 133 ms: 1.02x slower                                                  |
| unpickle_pure_python      | 244 us                                                                 | 250 us: 1.02x slower                                                  |
| hexiom                    | 7.37 ms                                                                | 7.55 ms: 1.02x slower                                                 |
| coroutines                | 23.3 ms                                                                | 23.9 ms: 1.03x slower                                                 |
| mdp                       | 2.60 sec                                                               | 2.70 sec: 1.04x slower                                                |
| richards_super            | 63.7 ms                                                                | 66.3 ms: 1.04x slower                                                 |
| regex_v8                  | 23.6 ms                                                                | 24.6 ms: 1.04x slower                                                 |
| gc_traversal              | 3.36 ms                                                                | 3.68 ms: 1.10x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (29): typing_runtime_protocols, docutils, genshi_xml, bench_mp_pool, sqlite_synth, deepcopy_reduce, thrift, generators, sphinx, crypto_pyaes, dulwich_log, asyncio_websockets, k_core, xml_etree_generate, xml_etree_iterparse, pylint, chaos, async_tree_cpu_io_mixed_tg, pprint_safe_repr, sqlalchemy_imperative, sqlalchemy_declarative, connected_components, bench_thread_pool, async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed, xml_etree_parse, sqlglot_optimize, async_tree_io_tg

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x