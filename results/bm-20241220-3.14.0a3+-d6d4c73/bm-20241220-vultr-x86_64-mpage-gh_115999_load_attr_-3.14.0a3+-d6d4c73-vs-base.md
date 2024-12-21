# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: d6d4c73
- commit date: 2024-12-20
- overall geometric mean: 1.002x faster
- HPT reliability: 99.76%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 255 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                | 22.2 ms                                                                | 21.3 ms: 1.04x faster                                                 |
| async_tree_memoization_tg | 307 ms                                                                 | 302 ms: 1.02x faster                                                  |
| async_generators          | 357 ms                                                                 | 358 ms: 1.00x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_io, async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 91.1 ms                                                                | 89.6 ms: 1.02x faster                                                 |
| pidigits       | 217 ms                                                                 | 217 ms: 1.00x slower                                                  |
| float          | 74.6 ms                                                                | 75.7 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 168 ms: 1.07x faster                                                  |
| regex_v8       | 25.0 ms                                                                | 23.5 ms: 1.07x faster                                                 |
| regex_effbot   | 2.81 ms                                                                | 2.76 ms: 1.02x faster                                                 |
| regex_compile  | 127 ms                                                                 | 126 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 316 us                                                                 | 306 us: 1.03x faster                                                  |
| unpickle_pure_python | 213 us                                                                 | 209 us: 1.02x faster                                                  |
| xml_etree_process    | 57.9 ms                                                                | 57.5 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 90.6 ms                                                                | 90.9 ms: 1.00x slower                                                 |
| json_loads           | 26.1 us                                                                | 26.3 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (4): tomli_loads, xml_etree_generate, json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                 |
| python_startup_no_site | 7.48 ms                                                                | 7.50 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.4 ms                                                                | 21.0 ms: 1.02x faster                                                 |
| django_template | 34.7 ms                                                                | 35.2 ms: 1.01x slower                                                 |
| mako            | 11.5 ms                                                                | 11.8 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna                 | 181 ms                                                                 | 168 ms: 1.07x faster                                                  |
| regex_v8                  | 25.0 ms                                                                | 23.5 ms: 1.07x faster                                                 |
| coroutines                | 22.2 ms                                                                | 21.3 ms: 1.04x faster                                                 |
| pickle_pure_python        | 316 us                                                                 | 306 us: 1.03x faster                                                  |
| chaos                     | 58.9 ms                                                                | 57.6 ms: 1.02x faster                                                 |
| scimark_sor               | 117 ms                                                                 | 114 ms: 1.02x faster                                                  |
| genshi_text               | 21.4 ms                                                                | 21.0 ms: 1.02x faster                                                 |
| pyflate                   | 419 ms                                                                 | 411 ms: 1.02x faster                                                  |
| go                        | 116 ms                                                                 | 114 ms: 1.02x faster                                                  |
| regex_effbot              | 2.81 ms                                                                | 2.76 ms: 1.02x faster                                                 |
| nbody                     | 91.1 ms                                                                | 89.6 ms: 1.02x faster                                                 |
| async_tree_memoization_tg | 307 ms                                                                 | 302 ms: 1.02x faster                                                  |
| unpickle_pure_python      | 213 us                                                                 | 209 us: 1.02x faster                                                  |
| scimark_lu                | 111 ms                                                                 | 110 ms: 1.02x faster                                                  |
| spectral_norm             | 97.3 ms                                                                | 95.9 ms: 1.01x faster                                                 |
| scimark_monte_carlo       | 63.4 ms                                                                | 62.6 ms: 1.01x faster                                                 |
| bpe_tokeniser             | 4.28 sec                                                               | 4.23 sec: 1.01x faster                                                |
| pprint_safe_repr          | 704 ms                                                                 | 696 ms: 1.01x faster                                                  |
| deltablue                 | 3.17 ms                                                                | 3.14 ms: 1.01x faster                                                 |
| many_optionals            | 1.03 ms                                                                | 1.02 ms: 1.01x faster                                                 |
| connected_components      | 394 ms                                                                 | 390 ms: 1.01x faster                                                  |
| regex_compile             | 127 ms                                                                 | 126 ms: 1.01x faster                                                  |
| fannkuch                  | 365 ms                                                                 | 362 ms: 1.01x faster                                                  |
| raytrace                  | 260 ms                                                                 | 258 ms: 1.01x faster                                                  |
| pprint_pformat            | 1.44 sec                                                               | 1.43 sec: 1.01x faster                                                |
| meteor_contest            | 98.9 ms                                                                | 98.1 ms: 1.01x faster                                                 |
| sqlalchemy_imperative     | 19.4 ms                                                                | 19.2 ms: 1.01x faster                                                 |
| xml_etree_process         | 57.9 ms                                                                | 57.5 ms: 1.01x faster                                                 |
| coverage                  | 79.2 ms                                                                | 78.8 ms: 1.01x faster                                                 |
| 2to3                      | 256 ms                                                                 | 255 ms: 1.01x faster                                                  |
| sqlalchemy_declarative    | 128 ms                                                                 | 128 ms: 1.00x faster                                                  |
| sympy_integrate           | 19.8 ms                                                                | 19.8 ms: 1.00x faster                                                 |
| sqlglot_parse             | 1.26 ms                                                                | 1.25 ms: 1.00x faster                                                 |
| crypto_pyaes              | 67.5 ms                                                                | 67.3 ms: 1.00x faster                                                 |
| sqlglot_normalize         | 103 ms                                                                 | 103 ms: 1.00x faster                                                  |
| pidigits                  | 217 ms                                                                 | 217 ms: 1.00x slower                                                  |
| python_startup            | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                 |
| python_startup_no_site    | 7.48 ms                                                                | 7.50 ms: 1.00x slower                                                 |
| xml_etree_iterparse       | 90.6 ms                                                                | 90.9 ms: 1.00x slower                                                 |
| hexiom                    | 5.88 ms                                                                | 5.90 ms: 1.00x slower                                                 |
| async_generators          | 357 ms                                                                 | 358 ms: 1.00x slower                                                  |
| dulwich_log               | 74.3 ms                                                                | 74.7 ms: 1.00x slower                                                 |
| deepcopy                  | 253 us                                                                 | 255 us: 1.01x slower                                                  |
| scimark_fft               | 313 ms                                                                 | 315 ms: 1.01x slower                                                  |
| logging_simple            | 5.95 us                                                                | 5.99 us: 1.01x slower                                                 |
| logging_silent            | 106 ns                                                                 | 107 ns: 1.01x slower                                                  |
| gc_traversal              | 4.37 ms                                                                | 4.41 ms: 1.01x slower                                                 |
| json_loads                | 26.1 us                                                                | 26.3 us: 1.01x slower                                                 |
| richards_super            | 48.6 ms                                                                | 49.2 ms: 1.01x slower                                                 |
| nqueens                   | 77.7 ms                                                                | 78.6 ms: 1.01x slower                                                 |
| generators                | 27.1 ms                                                                | 27.4 ms: 1.01x slower                                                 |
| django_template           | 34.7 ms                                                                | 35.2 ms: 1.01x slower                                                 |
| float                     | 74.6 ms                                                                | 75.7 ms: 1.02x slower                                                 |
| telco                     | 7.25 ms                                                                | 7.37 ms: 1.02x slower                                                 |
| richards                  | 42.3 ms                                                                | 43.0 ms: 1.02x slower                                                 |
| subparsers                | 21.6 ms                                                                | 22.0 ms: 1.02x slower                                                 |
| json                      | 4.79 ms                                                                | 4.88 ms: 1.02x slower                                                 |
| pathlib                   | 17.9 ms                                                                | 18.3 ms: 1.02x slower                                                 |
| mako                      | 11.5 ms                                                                | 11.8 ms: 1.02x slower                                                 |
| deepcopy_reduce           | 2.57 us                                                                | 2.65 us: 1.03x slower                                                 |
| scimark_sparse_mat_mult   | 4.26 ms                                                                | 4.46 ms: 1.05x slower                                                 |
| mdp                       | 2.34 sec                                                               | 2.50 sec: 1.07x slower                                                |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (33): pylint, async_tree_memoization, async_tree_io, async_tree_none_tg, async_tree_none, genshi_xml, k_core, async_tree_cpu_io_mixed_tg, sphinx, sympy_sum, async_tree_cpu_io_mixed, create_gc_cycles, comprehensions, tomli_loads, sqlglot_transpile, sqlite_synth, sympy_str, sqlglot_optimize, typing_runtime_protocols, bench_thread_pool, xml_etree_generate, shortest_path, deepcopy_memo, asyncio_websockets, pycparser, thrift, sympy_expand, json_dumps, docutils, bench_mp_pool, xml_etree_parse, logging_format, async_tree_io_tg

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 99.76% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x