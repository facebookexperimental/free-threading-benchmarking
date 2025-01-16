# Results vs. base

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 65a6ad3
- commit date: 2025-01-16
- overall geometric mean: 1.013x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 302 ms                                                                 | 306 ms: 1.01x slower                                                  |
| docutils       | 2.81 sec                                                               | 2.83 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators           | 368 ms                                                                 | 367 ms: 1.00x faster                                                  |
| coroutines                 | 23.6 ms                                                                | 23.7 ms: 1.01x slower                                                 |
| async_tree_none_tg         | 238 ms                                                                 | 240 ms: 1.01x slower                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 310 ms: 1.01x slower                                                  |
| async_tree_io              | 603 ms                                                                 | 610 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 532 ms                                                                 | 540 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 499 ms: 1.02x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (4): asyncio_websockets, async_tree_none, async_tree_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 130 ms                                                                 | 135 ms: 1.03x slower                                                  |
| float          | 75.1 ms                                                                | 78.5 ms: 1.05x slower                                                 |
| pidigits       | 199 ms                                                                 | 209 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 185 ms                                                                 | 183 ms: 1.01x faster                                                  |
| regex_compile  | 151 ms                                                                 | 152 ms: 1.01x slower                                                  |
| regex_effbot   | 2.78 ms                                                                | 2.82 ms: 1.01x slower                                                 |
| regex_v8       | 22.9 ms                                                                | 23.4 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_generate   | 96.0 ms                                                                | 96.4 ms: 1.00x slower                                                 |
| xml_etree_process    | 68.7 ms                                                                | 69.0 ms: 1.00x slower                                                 |
| json_loads           | 30.3 us                                                                | 30.7 us: 1.01x slower                                                 |
| pickle_pure_python   | 370 us                                                                 | 377 us: 1.02x slower                                                  |
| tomli_loads          | 2.30 sec                                                               | 2.35 sec: 1.02x slower                                                |
| json_dumps           | 12.7 ms                                                                | 13.0 ms: 1.03x slower                                                 |
| unpickle_pure_python | 242 us                                                                 | 252 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 15.2 ms                                                                | 15.2 ms: 1.00x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 43.5 ms                                                                | 43.0 ms: 1.01x faster                                                 |
| genshi_text     | 27.7 ms                                                                | 28.2 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna                  | 185 ms                                                                 | 183 ms: 1.01x faster                                                  |
| django_template            | 43.5 ms                                                                | 43.0 ms: 1.01x faster                                                 |
| spectral_norm              | 109 ms                                                                 | 108 ms: 1.01x faster                                                  |
| shortest_path              | 541 ms                                                                 | 536 ms: 1.01x faster                                                  |
| coverage                   | 98.4 ms                                                                | 97.9 ms: 1.00x faster                                                 |
| async_generators           | 368 ms                                                                 | 367 ms: 1.00x faster                                                  |
| python_startup             | 15.2 ms                                                                | 15.2 ms: 1.00x slower                                                 |
| xml_etree_generate         | 96.0 ms                                                                | 96.4 ms: 1.00x slower                                                 |
| xml_etree_process          | 68.7 ms                                                                | 69.0 ms: 1.00x slower                                                 |
| coroutines                 | 23.6 ms                                                                | 23.7 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.69 sec                                                               | 1.70 sec: 1.01x slower                                                |
| sqlalchemy_declarative     | 163 ms                                                                 | 164 ms: 1.01x slower                                                  |
| many_optionals             | 1.17 ms                                                                | 1.18 ms: 1.01x slower                                                 |
| docutils                   | 2.81 sec                                                               | 2.83 sec: 1.01x slower                                                |
| async_tree_none_tg         | 238 ms                                                                 | 240 ms: 1.01x slower                                                  |
| fannkuch                   | 476 ms                                                                 | 480 ms: 1.01x slower                                                  |
| deepcopy                   | 313 us                                                                 | 316 us: 1.01x slower                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 310 ms: 1.01x slower                                                  |
| scimark_fft                | 383 ms                                                                 | 387 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 5.57 ms                                                                | 5.63 ms: 1.01x slower                                                 |
| async_tree_io              | 603 ms                                                                 | 610 ms: 1.01x slower                                                  |
| regex_compile              | 151 ms                                                                 | 152 ms: 1.01x slower                                                  |
| pprint_safe_repr           | 819 ms                                                                 | 828 ms: 1.01x slower                                                  |
| sympy_integrate            | 24.0 ms                                                                | 24.3 ms: 1.01x slower                                                 |
| sympy_sum                  | 185 ms                                                                 | 188 ms: 1.01x slower                                                  |
| sympy_expand               | 545 ms                                                                 | 552 ms: 1.01x slower                                                  |
| json_loads                 | 30.3 us                                                                | 30.7 us: 1.01x slower                                                 |
| sympy_str                  | 332 ms                                                                 | 336 ms: 1.01x slower                                                  |
| pycparser                  | 1.18 sec                                                               | 1.19 sec: 1.01x slower                                                |
| logging_format             | 8.33 us                                                                | 8.43 us: 1.01x slower                                                 |
| 2to3                       | 302 ms                                                                 | 306 ms: 1.01x slower                                                  |
| regex_effbot               | 2.78 ms                                                                | 2.82 ms: 1.01x slower                                                 |
| generators                 | 31.1 ms                                                                | 31.5 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.02 us                                                                | 2.05 us: 1.01x slower                                                 |
| logging_simple             | 7.27 us                                                                | 7.37 us: 1.01x slower                                                 |
| deltablue                  | 4.59 ms                                                                | 4.66 ms: 1.01x slower                                                 |
| typing_runtime_protocols   | 201 us                                                                 | 204 us: 1.01x slower                                                  |
| create_gc_cycles           | 1.30 ms                                                                | 1.32 ms: 1.01x slower                                                 |
| telco                      | 8.40 ms                                                                | 8.52 ms: 1.01x slower                                                 |
| async_tree_cpu_io_mixed    | 532 ms                                                                 | 540 ms: 1.01x slower                                                  |
| crypto_pyaes               | 87.0 ms                                                                | 88.3 ms: 1.01x slower                                                 |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 499 ms: 1.02x slower                                                  |
| nqueens                    | 95.3 ms                                                                | 96.9 ms: 1.02x slower                                                 |
| pickle_pure_python         | 370 us                                                                 | 377 us: 1.02x slower                                                  |
| sqlglot_optimize           | 60.9 ms                                                                | 62.1 ms: 1.02x slower                                                 |
| sqlglot_normalize          | 120 ms                                                                 | 122 ms: 1.02x slower                                                  |
| genshi_text                | 27.7 ms                                                                | 28.2 ms: 1.02x slower                                                 |
| deepcopy_reduce            | 3.26 us                                                                | 3.33 us: 1.02x slower                                                 |
| comprehensions             | 20.5 us                                                                | 20.9 us: 1.02x slower                                                 |
| tomli_loads                | 2.30 sec                                                               | 2.35 sec: 1.02x slower                                                |
| meteor_contest             | 128 ms                                                                 | 131 ms: 1.02x slower                                                  |
| scimark_lu                 | 135 ms                                                                 | 138 ms: 1.02x slower                                                  |
| regex_v8                   | 22.9 ms                                                                | 23.4 ms: 1.02x slower                                                 |
| pyflate                    | 490 ms                                                                 | 502 ms: 1.02x slower                                                  |
| json_dumps                 | 12.7 ms                                                                | 13.0 ms: 1.03x slower                                                 |
| raytrace                   | 322 ms                                                                 | 330 ms: 1.03x slower                                                  |
| richards                   | 55.8 ms                                                                | 57.3 ms: 1.03x slower                                                 |
| bpe_tokeniser              | 4.62 sec                                                               | 4.74 sec: 1.03x slower                                                |
| chaos                      | 67.0 ms                                                                | 68.7 ms: 1.03x slower                                                 |
| scimark_monte_carlo        | 80.0 ms                                                                | 82.2 ms: 1.03x slower                                                 |
| hexiom                     | 7.22 ms                                                                | 7.44 ms: 1.03x slower                                                 |
| nbody                      | 130 ms                                                                 | 135 ms: 1.03x slower                                                  |
| richards_super             | 64.7 ms                                                                | 66.9 ms: 1.03x slower                                                 |
| sqlglot_parse              | 1.57 ms                                                                | 1.63 ms: 1.04x slower                                                 |
| go                         | 134 ms                                                                 | 139 ms: 1.04x slower                                                  |
| sqlglot_transpile          | 1.89 ms                                                                | 1.96 ms: 1.04x slower                                                 |
| scimark_sor                | 128 ms                                                                 | 133 ms: 1.04x slower                                                  |
| unpickle_pure_python       | 242 us                                                                 | 252 us: 1.04x slower                                                  |
| float                      | 75.1 ms                                                                | 78.5 ms: 1.05x slower                                                 |
| pidigits                   | 199 ms                                                                 | 209 ms: 1.05x slower                                                  |
| logging_silent             | 112 ns                                                                 | 118 ns: 1.05x slower                                                  |
| deepcopy_memo              | 37.3 us                                                                | 39.3 us: 1.05x slower                                                 |
| mdp                        | 2.59 sec                                                               | 2.77 sec: 1.07x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (23): xml_etree_parse, connected_components, sqlalchemy_imperative, mako, thrift, asyncio_websockets, json, python_startup_no_site, subparsers, async_tree_none, gc_traversal, xml_etree_iterparse, k_core, html5lib, async_tree_memoization, bench_thread_pool, genshi_xml, dulwich_log, bench_mp_pool, pathlib, sphinx, async_tree_io_tg, pylint

- Geometric mean (including insignificant results): 1.013x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x