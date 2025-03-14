# Results vs. base

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: d4ce112
- commit date: 2025-03-13
- overall geometric mean: 1.009x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5+-db1e582 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                 | 296 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5+-db1e582 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 511 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                 | 480 ms: 1.03x faster                                                     |
| coroutines                 | 24.0 ms                                                                | 23.4 ms: 1.03x faster                                                    |
| async_generators           | 376 ms                                                                 | 368 ms: 1.02x faster                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (7): async_tree_none, async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg, asyncio_websockets, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5+-db1e582 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                                 | 187 ms: 1.06x faster                                                     |
| nbody          | 139 ms                                                                 | 132 ms: 1.05x faster                                                     |
| float          | 79.1 ms                                                                | 77.5 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5+-db1e582 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.72 ms: 1.02x faster                                                    |
| regex_compile  | 159 ms                                                                 | 157 ms: 1.01x faster                                                     |
| regex_v8       | 23.6 ms                                                                | 23.9 ms: 1.01x slower                                                    |
| regex_dna      | 173 ms                                                                 | 185 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5+-db1e582 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_pure_python | 260 us                                                                 | 248 us: 1.05x faster                                                     |
| pickle_pure_python   | 373 us                                                                 | 360 us: 1.04x faster                                                     |
| xml_etree_generate   | 97.6 ms                                                                | 95.5 ms: 1.02x faster                                                    |
| json_dumps           | 12.9 ms                                                                | 12.8 ms: 1.01x faster                                                    |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.01x faster                                                     |
| xml_etree_iterparse  | 88.2 ms                                                                | 87.6 ms: 1.01x faster                                                    |
| tomli_loads          | 2.37 sec                                                               | 2.35 sec: 1.01x faster                                                   |
| json_loads           | 29.2 us                                                                | 30.9 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5+-db1e582 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                    |
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5+-db1e582 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 16.0 ms                                                                | 15.9 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (3): genshi_xml, genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5+-db1e582 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 199 ms                                                                 | 187 ms: 1.06x faster                                                     |
| logging_silent             | 116 ns                                                                 | 109 ns: 1.06x faster                                                     |
| nbody                      | 139 ms                                                                 | 132 ms: 1.05x faster                                                     |
| unpickle_pure_python       | 260 us                                                                 | 248 us: 1.05x faster                                                     |
| deltablue                  | 3.97 ms                                                                | 3.82 ms: 1.04x faster                                                    |
| deepcopy_reduce            | 3.26 us                                                                | 3.14 us: 1.04x faster                                                    |
| pickle_pure_python         | 373 us                                                                 | 360 us: 1.04x faster                                                     |
| raytrace                   | 331 ms                                                                 | 320 ms: 1.03x faster                                                     |
| comprehensions             | 21.2 us                                                                | 20.6 us: 1.03x faster                                                    |
| mdp                        | 2.68 sec                                                               | 2.60 sec: 1.03x faster                                                   |
| hexiom                     | 7.61 ms                                                                | 7.39 ms: 1.03x faster                                                    |
| go                         | 145 ms                                                                 | 141 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 511 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                 | 480 ms: 1.03x faster                                                     |
| coroutines                 | 24.0 ms                                                                | 23.4 ms: 1.03x faster                                                    |
| chaos                      | 70.6 ms                                                                | 69.0 ms: 1.02x faster                                                    |
| pyflate                    | 511 ms                                                                 | 500 ms: 1.02x faster                                                     |
| scimark_sparse_mat_mult    | 5.89 ms                                                                | 5.75 ms: 1.02x faster                                                    |
| crypto_pyaes               | 89.2 ms                                                                | 87.2 ms: 1.02x faster                                                    |
| float                      | 79.1 ms                                                                | 77.5 ms: 1.02x faster                                                    |
| xml_etree_generate         | 97.6 ms                                                                | 95.5 ms: 1.02x faster                                                    |
| async_generators           | 376 ms                                                                 | 368 ms: 1.02x faster                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.31 ms: 1.02x faster                                                    |
| sqlglot_parse              | 1.62 ms                                                                | 1.59 ms: 1.02x faster                                                    |
| regex_effbot               | 2.78 ms                                                                | 2.72 ms: 1.02x faster                                                    |
| sympy_integrate            | 24.4 ms                                                                | 23.9 ms: 1.02x faster                                                    |
| sympy_sum                  | 189 ms                                                                 | 185 ms: 1.02x faster                                                     |
| scimark_sor                | 137 ms                                                                 | 134 ms: 1.02x faster                                                     |
| deepcopy                   | 314 us                                                                 | 308 us: 1.02x faster                                                     |
| dulwich_log                | 74.3 ms                                                                | 73.1 ms: 1.02x faster                                                    |
| pprint_safe_repr           | 853 ms                                                                 | 838 ms: 1.02x faster                                                     |
| scimark_fft                | 399 ms                                                                 | 393 ms: 1.02x faster                                                     |
| sqlglot_transpile          | 1.95 ms                                                                | 1.92 ms: 1.02x faster                                                    |
| fannkuch                   | 497 ms                                                                 | 489 ms: 1.02x faster                                                     |
| deepcopy_memo              | 39.3 us                                                                | 38.7 us: 1.01x faster                                                    |
| scimark_monte_carlo        | 84.4 ms                                                                | 83.2 ms: 1.01x faster                                                    |
| richards                   | 56.1 ms                                                                | 55.3 ms: 1.01x faster                                                    |
| bpe_tokeniser              | 4.85 sec                                                               | 4.79 sec: 1.01x faster                                                   |
| 2to3                       | 300 ms                                                                 | 296 ms: 1.01x faster                                                     |
| logging_format             | 8.20 us                                                                | 8.10 us: 1.01x faster                                                    |
| gc_traversal               | 1.74 ms                                                                | 1.72 ms: 1.01x faster                                                    |
| generators                 | 31.7 ms                                                                | 31.3 ms: 1.01x faster                                                    |
| subparsers                 | 25.4 ms                                                                | 25.1 ms: 1.01x faster                                                    |
| richards_super             | 64.9 ms                                                                | 64.3 ms: 1.01x faster                                                    |
| sympy_str                  | 338 ms                                                                 | 335 ms: 1.01x faster                                                     |
| coverage                   | 97.1 ms                                                                | 96.2 ms: 1.01x faster                                                    |
| json_dumps                 | 12.9 ms                                                                | 12.8 ms: 1.01x faster                                                    |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.01x faster                                                     |
| bench_mp_pool              | 96.1 ms                                                                | 95.3 ms: 1.01x faster                                                    |
| pprint_pformat             | 1.75 sec                                                               | 1.74 sec: 1.01x faster                                                   |
| regex_compile              | 159 ms                                                                 | 157 ms: 1.01x faster                                                     |
| sympy_expand               | 556 ms                                                                 | 552 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 88.2 ms                                                                | 87.6 ms: 1.01x faster                                                    |
| shortest_path              | 547 ms                                                                 | 543 ms: 1.01x faster                                                     |
| tomli_loads                | 2.37 sec                                                               | 2.35 sec: 1.01x faster                                                   |
| python_startup             | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                    |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                    |
| mako                       | 16.0 ms                                                                | 15.9 ms: 1.01x faster                                                    |
| telco                      | 8.69 ms                                                                | 8.65 ms: 1.01x faster                                                    |
| k_core                     | 2.31 sec                                                               | 2.30 sec: 1.00x faster                                                   |
| bench_thread_pool          | 3.16 ms                                                                | 3.16 ms: 1.00x slower                                                    |
| spectral_norm              | 112 ms                                                                 | 112 ms: 1.00x slower                                                     |
| meteor_contest             | 132 ms                                                                 | 133 ms: 1.01x slower                                                     |
| regex_v8                   | 23.6 ms                                                                | 23.9 ms: 1.01x slower                                                    |
| thrift                     | 874 us                                                                 | 888 us: 1.02x slower                                                     |
| scimark_lu                 | 140 ms                                                                 | 144 ms: 1.02x slower                                                     |
| nqueens                    | 97.8 ms                                                                | 101 ms: 1.03x slower                                                     |
| json                       | 5.10 ms                                                                | 5.31 ms: 1.04x slower                                                    |
| json_loads                 | 29.2 us                                                                | 30.9 us: 1.06x slower                                                    |
| regex_dna                  | 173 ms                                                                 | 185 ms: 1.07x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (26): sqlglot_normalize, sqlglot_optimize, pylint, async_tree_none, sphinx, pathlib, async_tree_memoization, xml_etree_process, genshi_xml, many_optionals, html5lib, async_tree_none_tg, genshi_text, docutils, sqlalchemy_imperative, django_template, async_tree_memoization_tg, sqlalchemy_declarative, logging_simple, pycparser, connected_components, asyncio_websockets, typing_runtime_protocols, async_tree_io, sqlite_synth, async_tree_io_tg

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x