# Results vs. base

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 73aa5a2
- commit date: 2025-01-15
- overall geometric mean: 1.021x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 250 ms: 1.02x faster                                                  |
| docutils       | 2.58 sec                                                               | 2.54 sec: 1.02x faster                                                |
| sphinx         | 989 ms                                                                 | 975 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 506 ms: 1.09x faster                                                  |
| async_tree_cpu_io_mixed    | 569 ms                                                                 | 525 ms: 1.09x faster                                                  |
| async_tree_io_tg           | 612 ms                                                                 | 595 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 256 ms                                                                 | 249 ms: 1.03x faster                                                  |
| async_tree_none            | 268 ms                                                                 | 263 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 303 ms                                                                 | 296 ms: 1.02x faster                                                  |
| async_tree_memoization     | 325 ms                                                                 | 319 ms: 1.02x faster                                                  |
| coroutines                 | 21.9 ms                                                                | 21.7 ms: 1.01x faster                                                 |
| async_generators           | 322 ms                                                                 | 320 ms: 1.01x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 522 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 96.1 ms                                                                | 82.2 ms: 1.17x faster                                                 |
| pidigits       | 229 ms                                                                 | 207 ms: 1.11x faster                                                  |
| float          | 74.9 ms                                                                | 70.9 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.80 ms                                                                | 2.62 ms: 1.07x faster                                                 |
| regex_compile  | 127 ms                                                                 | 124 ms: 1.02x faster                                                  |
| regex_dna      | 172 ms                                                                 | 169 ms: 1.02x faster                                                  |
| regex_v8       | 22.8 ms                                                                | 22.9 ms: 1.00x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 214 us                                                                 | 204 us: 1.05x faster                                                  |
| tomli_loads          | 1.92 sec                                                               | 1.86 sec: 1.04x faster                                                |
| pickle_pure_python   | 314 us                                                                 | 305 us: 1.03x faster                                                  |
| xml_etree_iterparse  | 91.5 ms                                                                | 89.5 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                                | 57.8 ms: 1.02x faster                                                 |
| json_dumps           | 11.7 ms                                                                | 11.5 ms: 1.02x faster                                                 |
| xml_etree_generate   | 83.7 ms                                                                | 82.4 ms: 1.02x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 14.6 ms: 1.01x faster                                                 |
| python_startup_no_site | 7.46 ms                                                                | 7.43 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.1 ms                                                                | 46.9 ms: 1.02x faster                                                 |
| genshi_text     | 20.8 ms                                                                | 20.4 ms: 1.02x faster                                                 |
| django_template | 34.8 ms                                                                | 34.2 ms: 1.02x faster                                                 |
| mako            | 11.7 ms                                                                | 11.6 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody                      | 96.1 ms                                                                | 82.2 ms: 1.17x faster                                                 |
| pidigits                   | 229 ms                                                                 | 207 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 506 ms: 1.09x faster                                                  |
| async_tree_cpu_io_mixed    | 569 ms                                                                 | 525 ms: 1.09x faster                                                  |
| regex_effbot               | 2.80 ms                                                                | 2.62 ms: 1.07x faster                                                 |
| go                         | 119 ms                                                                 | 112 ms: 1.06x faster                                                  |
| float                      | 74.9 ms                                                                | 70.9 ms: 1.06x faster                                                 |
| raytrace                   | 268 ms                                                                 | 253 ms: 1.06x faster                                                  |
| richards_super             | 49.6 ms                                                                | 47.1 ms: 1.05x faster                                                 |
| richards                   | 43.5 ms                                                                | 41.4 ms: 1.05x faster                                                 |
| pyflate                    | 420 ms                                                                 | 400 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 214 us                                                                 | 204 us: 1.05x faster                                                  |
| sqlglot_parse              | 1.28 ms                                                                | 1.23 ms: 1.04x faster                                                 |
| chaos                      | 58.6 ms                                                                | 56.4 ms: 1.04x faster                                                 |
| sqlglot_transpile          | 1.58 ms                                                                | 1.53 ms: 1.04x faster                                                 |
| deltablue                  | 3.21 ms                                                                | 3.10 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 64.0 ms                                                                | 61.8 ms: 1.04x faster                                                 |
| tomli_loads                | 1.92 sec                                                               | 1.86 sec: 1.04x faster                                                |
| comprehensions             | 16.9 us                                                                | 16.4 us: 1.03x faster                                                 |
| generators                 | 28.1 ms                                                                | 27.2 ms: 1.03x faster                                                 |
| pickle_pure_python         | 314 us                                                                 | 305 us: 1.03x faster                                                  |
| async_tree_io_tg           | 612 ms                                                                 | 595 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 256 ms                                                                 | 249 ms: 1.03x faster                                                  |
| crypto_pyaes               | 66.5 ms                                                                | 64.8 ms: 1.03x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.02x faster                                                |
| genshi_xml                 | 48.1 ms                                                                | 46.9 ms: 1.02x faster                                                 |
| sqlglot_optimize           | 52.6 ms                                                                | 51.4 ms: 1.02x faster                                                 |
| genshi_text                | 20.8 ms                                                                | 20.4 ms: 1.02x faster                                                 |
| scimark_lu                 | 113 ms                                                                 | 110 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 91.5 ms                                                                | 89.5 ms: 1.02x faster                                                 |
| async_tree_none            | 268 ms                                                                 | 263 ms: 1.02x faster                                                  |
| regex_compile              | 127 ms                                                                 | 124 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 303 ms                                                                 | 296 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 104 ms                                                                 | 101 ms: 1.02x faster                                                  |
| meteor_contest             | 99.5 ms                                                                | 97.5 ms: 1.02x faster                                                 |
| telco                      | 7.25 ms                                                                | 7.11 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                                | 57.8 ms: 1.02x faster                                                 |
| async_tree_memoization     | 325 ms                                                                 | 319 ms: 1.02x faster                                                  |
| django_template            | 34.8 ms                                                                | 34.2 ms: 1.02x faster                                                 |
| regex_dna                  | 172 ms                                                                 | 169 ms: 1.02x faster                                                  |
| logging_format             | 6.75 us                                                                | 6.63 us: 1.02x faster                                                 |
| json_dumps                 | 11.7 ms                                                                | 11.5 ms: 1.02x faster                                                 |
| bpe_tokeniser              | 4.25 sec                                                               | 4.18 sec: 1.02x faster                                                |
| subparsers                 | 21.8 ms                                                                | 21.5 ms: 1.02x faster                                                 |
| thrift                     | 747 us                                                                 | 735 us: 1.02x faster                                                  |
| deepcopy_memo              | 30.0 us                                                                | 29.5 us: 1.02x faster                                                 |
| xml_etree_generate         | 83.7 ms                                                                | 82.4 ms: 1.02x faster                                                 |
| docutils                   | 2.58 sec                                                               | 2.54 sec: 1.02x faster                                                |
| pprint_safe_repr           | 689 ms                                                                 | 678 ms: 1.02x faster                                                  |
| many_optionals             | 1.03 ms                                                                | 1.01 ms: 1.02x faster                                                 |
| scimark_sor                | 116 ms                                                                 | 114 ms: 1.02x faster                                                  |
| 2to3                       | 253 ms                                                                 | 250 ms: 1.02x faster                                                  |
| shortest_path              | 433 ms                                                                 | 427 ms: 1.01x faster                                                  |
| sphinx                     | 989 ms                                                                 | 975 ms: 1.01x faster                                                  |
| k_core                     | 2.06 sec                                                               | 2.03 sec: 1.01x faster                                                |
| pprint_pformat             | 1.40 sec                                                               | 1.38 sec: 1.01x faster                                                |
| sqlite_synth               | 2.22 us                                                                | 2.20 us: 1.01x faster                                                 |
| hexiom                     | 5.77 ms                                                                | 5.72 ms: 1.01x faster                                                 |
| pathlib                    | 18.2 ms                                                                | 18.1 ms: 1.01x faster                                                 |
| connected_components       | 390 ms                                                                 | 387 ms: 1.01x faster                                                  |
| bench_mp_pool              | 88.8 ms                                                                | 88.1 ms: 1.01x faster                                                 |
| mako                       | 11.7 ms                                                                | 11.6 ms: 1.01x faster                                                 |
| sqlalchemy_declarative     | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| coverage                   | 80.0 ms                                                                | 79.4 ms: 1.01x faster                                                 |
| coroutines                 | 21.9 ms                                                                | 21.7 ms: 1.01x faster                                                 |
| deepcopy                   | 255 us                                                                 | 253 us: 1.01x faster                                                  |
| async_generators           | 322 ms                                                                 | 320 ms: 1.01x faster                                                  |
| mdp                        | 2.32 sec                                                               | 2.30 sec: 1.01x faster                                                |
| python_startup             | 14.7 ms                                                                | 14.6 ms: 1.01x faster                                                 |
| sympy_str                  | 271 ms                                                                 | 269 ms: 1.01x faster                                                  |
| logging_simple             | 5.95 us                                                                | 5.92 us: 1.01x faster                                                 |
| bench_thread_pool          | 1.04 ms                                                                | 1.03 ms: 1.01x faster                                                 |
| python_startup_no_site     | 7.46 ms                                                                | 7.43 ms: 1.01x faster                                                 |
| sympy_expand               | 452 ms                                                                 | 450 ms: 1.00x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 19.6 ms: 1.00x faster                                                 |
| scimark_fft                | 314 ms                                                                 | 313 ms: 1.00x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 522 ms: 1.00x faster                                                  |
| regex_v8                   | 22.8 ms                                                                | 22.9 ms: 1.00x slower                                                 |
| typing_runtime_protocols   | 154 us                                                                 | 155 us: 1.01x slower                                                  |
| logging_silent             | 105 ns                                                                 | 106 ns: 1.01x slower                                                  |
| create_gc_cycles           | 1.82 ms                                                                | 1.84 ms: 1.01x slower                                                 |
| fannkuch                   | 366 ms                                                                 | 376 ms: 1.03x slower                                                  |
| scimark_sparse_mat_mult    | 4.18 ms                                                                | 4.30 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (12): async_tree_io, pylint, json, json_loads, dulwich_log, sqlalchemy_imperative, nqueens, gc_traversal, spectral_norm, deepcopy_reduce, sympy_sum, xml_etree_parse

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x