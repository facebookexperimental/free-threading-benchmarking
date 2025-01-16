# Results vs. base

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 65a6ad3
- commit date: 2025-01-16
- overall geometric mean: 1.001x slower
- HPT reliability: 97.72%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 254 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg | 302 ms                                                                 | 304 ms: 1.01x slower                                                  |
| async_tree_none_tg        | 252 ms                                                                 | 255 ms: 1.01x slower                                                  |
| async_tree_none           | 267 ms                                                                 | 272 ms: 1.02x slower                                                  |
| async_tree_io_tg          | 605 ms                                                                 | 615 ms: 1.02x slower                                                  |
| coroutines                | 21.8 ms                                                                | 22.5 ms: 1.03x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (6): async_tree_io, async_tree_cpu_io_mixed_tg, asyncio_websockets, async_generators, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 206 ms                                                                 | 191 ms: 1.08x faster                                                  |
| nbody          | 85.8 ms                                                                | 87.3 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                | 2.71 ms: 1.05x faster                                                 |
| regex_v8       | 23.8 ms                                                                | 23.4 ms: 1.02x faster                                                 |
| regex_dna      | 171 ms                                                                 | 177 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_generate  | 85.1 ms                                                                | 83.8 ms: 1.02x faster                                                 |
| xml_etree_parse     | 130 ms                                                                 | 128 ms: 1.01x faster                                                  |
| xml_etree_process   | 59.9 ms                                                                | 59.2 ms: 1.01x faster                                                 |
| json_loads          | 27.8 us                                                                | 27.6 us: 1.01x faster                                                 |
| xml_etree_iterparse | 90.9 ms                                                                | 90.4 ms: 1.01x faster                                                 |
| json_dumps          | 11.4 ms                                                                | 11.5 ms: 1.01x slower                                                 |
| pickle_pure_python  | 308 us                                                                 | 313 us: 1.02x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): unpickle_pure_python, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.45 ms                                                                | 7.48 ms: 1.00x slower                                                 |
| python_startup         | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.6 ms                                                                | 21.3 ms: 1.01x faster                                                 |
| genshi_xml      | 49.4 ms                                                                | 48.8 ms: 1.01x faster                                                 |
| django_template | 35.7 ms                                                                | 36.0 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                 | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| scimark_sparse_mat_mult   | 4.59 ms                                                                | 4.20 ms: 1.09x faster                                                 |
| pidigits                  | 206 ms                                                                 | 191 ms: 1.08x faster                                                  |
| regex_effbot              | 2.84 ms                                                                | 2.71 ms: 1.05x faster                                                 |
| scimark_fft               | 328 ms                                                                 | 314 ms: 1.04x faster                                                  |
| scimark_lu                | 115 ms                                                                 | 112 ms: 1.02x faster                                                  |
| regex_v8                  | 23.8 ms                                                                | 23.4 ms: 1.02x faster                                                 |
| telco                     | 7.33 ms                                                                | 7.21 ms: 1.02x faster                                                 |
| xml_etree_generate        | 85.1 ms                                                                | 83.8 ms: 1.02x faster                                                 |
| scimark_monte_carlo       | 64.4 ms                                                                | 63.4 ms: 1.02x faster                                                 |
| xml_etree_parse           | 130 ms                                                                 | 128 ms: 1.01x faster                                                  |
| xml_etree_process         | 59.9 ms                                                                | 59.2 ms: 1.01x faster                                                 |
| genshi_text               | 21.6 ms                                                                | 21.3 ms: 1.01x faster                                                 |
| chaos                     | 55.6 ms                                                                | 54.9 ms: 1.01x faster                                                 |
| create_gc_cycles          | 1.85 ms                                                                | 1.83 ms: 1.01x faster                                                 |
| genshi_xml                | 49.4 ms                                                                | 48.8 ms: 1.01x faster                                                 |
| coverage                  | 79.6 ms                                                                | 78.8 ms: 1.01x faster                                                 |
| sqlite_synth              | 2.22 us                                                                | 2.20 us: 1.01x faster                                                 |
| pathlib                   | 18.3 ms                                                                | 18.1 ms: 1.01x faster                                                 |
| json                      | 5.02 ms                                                                | 4.98 ms: 1.01x faster                                                 |
| json_loads                | 27.8 us                                                                | 27.6 us: 1.01x faster                                                 |
| xml_etree_iterparse       | 90.9 ms                                                                | 90.4 ms: 1.01x faster                                                 |
| scimark_sor               | 115 ms                                                                 | 114 ms: 1.00x faster                                                  |
| bpe_tokeniser             | 4.22 sec                                                               | 4.23 sec: 1.00x slower                                                |
| deepcopy_memo             | 29.9 us                                                                | 29.9 us: 1.00x slower                                                 |
| sympy_integrate           | 19.8 ms                                                                | 19.9 ms: 1.00x slower                                                 |
| crypto_pyaes              | 66.6 ms                                                                | 66.8 ms: 1.00x slower                                                 |
| 2to3                      | 253 ms                                                                 | 254 ms: 1.00x slower                                                  |
| deepcopy                  | 259 us                                                                 | 260 us: 1.00x slower                                                  |
| python_startup_no_site    | 7.45 ms                                                                | 7.48 ms: 1.00x slower                                                 |
| fannkuch                  | 375 ms                                                                 | 377 ms: 1.00x slower                                                  |
| python_startup            | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                 |
| sqlalchemy_declarative    | 129 ms                                                                 | 129 ms: 1.00x slower                                                  |
| json_dumps                | 11.4 ms                                                                | 11.5 ms: 1.01x slower                                                 |
| connected_components      | 390 ms                                                                 | 393 ms: 1.01x slower                                                  |
| django_template           | 35.7 ms                                                                | 36.0 ms: 1.01x slower                                                 |
| sympy_sum                 | 153 ms                                                                 | 154 ms: 1.01x slower                                                  |
| deltablue                 | 3.15 ms                                                                | 3.18 ms: 1.01x slower                                                 |
| async_tree_memoization_tg | 302 ms                                                                 | 304 ms: 1.01x slower                                                  |
| generators                | 28.0 ms                                                                | 28.2 ms: 1.01x slower                                                 |
| sqlalchemy_imperative     | 19.5 ms                                                                | 19.6 ms: 1.01x slower                                                 |
| shortest_path             | 430 ms                                                                 | 434 ms: 1.01x slower                                                  |
| sympy_str                 | 273 ms                                                                 | 275 ms: 1.01x slower                                                  |
| meteor_contest            | 97.7 ms                                                                | 98.8 ms: 1.01x slower                                                 |
| thrift                    | 741 us                                                                 | 750 us: 1.01x slower                                                  |
| mdp                       | 2.46 sec                                                               | 2.49 sec: 1.01x slower                                                |
| gc_traversal              | 4.32 ms                                                                | 4.38 ms: 1.01x slower                                                 |
| async_tree_none_tg        | 252 ms                                                                 | 255 ms: 1.01x slower                                                  |
| logging_format            | 6.87 us                                                                | 6.97 us: 1.01x slower                                                 |
| logging_simple            | 6.16 us                                                                | 6.25 us: 1.01x slower                                                 |
| pyflate                   | 409 ms                                                                 | 415 ms: 1.01x slower                                                  |
| pickle_pure_python        | 308 us                                                                 | 313 us: 1.02x slower                                                  |
| richards_super            | 48.1 ms                                                                | 48.9 ms: 1.02x slower                                                 |
| async_tree_none           | 267 ms                                                                 | 272 ms: 1.02x slower                                                  |
| async_tree_io_tg          | 605 ms                                                                 | 615 ms: 1.02x slower                                                  |
| many_optionals            | 1.02 ms                                                                | 1.04 ms: 1.02x slower                                                 |
| nbody                     | 85.8 ms                                                                | 87.3 ms: 1.02x slower                                                 |
| richards                  | 42.0 ms                                                                | 42.8 ms: 1.02x slower                                                 |
| hexiom                    | 5.73 ms                                                                | 5.85 ms: 1.02x slower                                                 |
| logging_silent            | 102 ns                                                                 | 104 ns: 1.02x slower                                                  |
| subparsers                | 21.9 ms                                                                | 22.4 ms: 1.02x slower                                                 |
| coroutines                | 21.8 ms                                                                | 22.5 ms: 1.03x slower                                                 |
| regex_dna                 | 171 ms                                                                 | 177 ms: 1.04x slower                                                  |
| spectral_norm             | 88.3 ms                                                                | 95.4 ms: 1.08x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (32): float, async_tree_io, unpickle_pure_python, pprint_pformat, sympy_expand, dulwich_log, k_core, nqueens, sqlglot_normalize, pprint_safe_repr, regex_compile, tomli_loads, go, sqlglot_parse, async_tree_cpu_io_mixed_tg, typing_runtime_protocols, mako, asyncio_websockets, sqlglot_optimize, bench_thread_pool, docutils, deepcopy_reduce, sqlglot_transpile, comprehensions, async_generators, raytrace, pycparser, pylint, sphinx, bench_mp_pool, async_tree_memoization, async_tree_cpu_io_mixed

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 97.72% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x