# Results vs. base

- fork: Yhg1s
- ref: frame_threadsafety
- machine: linux-x86_64
- commit hash: d3f6063
- commit date: 2025-03-21
- overall geometric mean: 1.009x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 296 ms                                                                 | 297 ms: 1.00x slower                                                |
| html5lib       | 69.2 ms                                                                | 71.2 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| coroutines                 | 23.7 ms                                                                | 23.3 ms: 1.02x faster                                               |
| async_generators           | 380 ms                                                                 | 383 ms: 1.01x slower                                                |
| async_tree_io_tg           | 546 ms                                                                 | 551 ms: 1.01x slower                                                |
| async_tree_none            | 273 ms                                                                 | 277 ms: 1.01x slower                                                |
| async_tree_io              | 577 ms                                                                 | 588 ms: 1.02x slower                                                |
| async_tree_cpu_io_mixed    | 519 ms                                                                 | 568 ms: 1.09x slower                                                |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 535 ms: 1.10x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                        |

Benchmark hidden because not significant (4): asyncio_websockets, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 77.1 ms                                                                | 78.1 ms: 1.01x slower                                               |
| nbody          | 129 ms                                                                 | 137 ms: 1.06x slower                                                |
| pidigits       | 191 ms                                                                 | 216 ms: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                | 21.3 ms: 1.02x faster                                               |
| regex_compile  | 156 ms                                                                 | 157 ms: 1.01x slower                                                |
| regex_dna      | 169 ms                                                                 | 172 ms: 1.02x slower                                                |
| regex_effbot   | 2.77 ms                                                                | 2.85 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| tomli_loads          | 2.35 sec                                                               | 2.34 sec: 1.01x faster                                              |
| xml_etree_process    | 70.4 ms                                                                | 70.5 ms: 1.00x slower                                               |
| xml_etree_generate   | 96.8 ms                                                                | 97.2 ms: 1.00x slower                                               |
| unpickle_pure_python | 252 us                                                                 | 254 us: 1.01x slower                                                |
| xml_etree_iterparse  | 87.4 ms                                                                | 88.0 ms: 1.01x slower                                               |
| pickle_pure_python   | 356 us                                                                 | 360 us: 1.01x slower                                                |
| json_dumps           | 12.9 ms                                                                | 13.0 ms: 1.01x slower                                               |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 11.0 ms                                                                | 11.1 ms: 1.00x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml     | 60.7 ms                                                                | 59.6 ms: 1.02x faster                                               |
| genshi_text    | 28.4 ms                                                                | 28.6 ms: 1.01x slower                                               |
| mako           | 15.8 ms                                                                | 15.9 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250321-vultr-x86_64-python-b70d45ab22e1d0f3b8a0-3.14.0a6+-b70d45a | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| thrift                     | 872 us                                                                 | 855 us: 1.02x faster                                                |
| genshi_xml                 | 60.7 ms                                                                | 59.6 ms: 1.02x faster                                               |
| coroutines                 | 23.7 ms                                                                | 23.3 ms: 1.02x faster                                               |
| regex_v8                   | 21.6 ms                                                                | 21.3 ms: 1.02x faster                                               |
| sqlite_synth               | 2.02 us                                                                | 1.99 us: 1.01x faster                                               |
| deepcopy                   | 314 us                                                                 | 310 us: 1.01x faster                                                |
| connected_components       | 507 ms                                                                 | 502 ms: 1.01x faster                                                |
| tomli_loads                | 2.35 sec                                                               | 2.34 sec: 1.01x faster                                              |
| sympy_integrate            | 23.6 ms                                                                | 23.5 ms: 1.01x faster                                               |
| dulwich_log                | 73.2 ms                                                                | 72.8 ms: 1.00x faster                                               |
| sympy_sum                  | 186 ms                                                                 | 185 ms: 1.00x faster                                                |
| python_startup_no_site     | 11.0 ms                                                                | 11.1 ms: 1.00x slower                                               |
| xml_etree_process          | 70.4 ms                                                                | 70.5 ms: 1.00x slower                                               |
| richards                   | 55.1 ms                                                                | 55.2 ms: 1.00x slower                                               |
| nqueens                    | 97.4 ms                                                                | 97.8 ms: 1.00x slower                                               |
| xml_etree_generate         | 96.8 ms                                                                | 97.2 ms: 1.00x slower                                               |
| 2to3                       | 296 ms                                                                 | 297 ms: 1.00x slower                                                |
| scimark_monte_carlo        | 82.9 ms                                                                | 83.2 ms: 1.00x slower                                               |
| k_core                     | 2.31 sec                                                               | 2.32 sec: 1.00x slower                                              |
| deltablue                  | 3.85 ms                                                                | 3.86 ms: 1.00x slower                                               |
| bpe_tokeniser              | 4.83 sec                                                               | 4.86 sec: 1.00x slower                                              |
| unpickle_pure_python       | 252 us                                                                 | 254 us: 1.01x slower                                                |
| deepcopy_memo              | 39.0 us                                                                | 39.2 us: 1.01x slower                                               |
| genshi_text                | 28.4 ms                                                                | 28.6 ms: 1.01x slower                                               |
| mako                       | 15.8 ms                                                                | 15.9 ms: 1.01x slower                                               |
| deepcopy_reduce            | 3.15 us                                                                | 3.17 us: 1.01x slower                                               |
| xml_etree_iterparse        | 87.4 ms                                                                | 88.0 ms: 1.01x slower                                               |
| create_gc_cycles           | 1.34 ms                                                                | 1.35 ms: 1.01x slower                                               |
| async_generators           | 380 ms                                                                 | 383 ms: 1.01x slower                                                |
| regex_compile              | 156 ms                                                                 | 157 ms: 1.01x slower                                                |
| gc_traversal               | 1.78 ms                                                                | 1.79 ms: 1.01x slower                                               |
| async_tree_io_tg           | 546 ms                                                                 | 551 ms: 1.01x slower                                                |
| pprint_safe_repr           | 834 ms                                                                 | 843 ms: 1.01x slower                                                |
| pyflate                    | 494 ms                                                                 | 499 ms: 1.01x slower                                                |
| sqlglot_v2_parse           | 1.58 ms                                                                | 1.60 ms: 1.01x slower                                               |
| pickle_pure_python         | 356 us                                                                 | 360 us: 1.01x slower                                                |
| json_dumps                 | 12.9 ms                                                                | 13.0 ms: 1.01x slower                                               |
| float                      | 77.1 ms                                                                | 78.1 ms: 1.01x slower                                               |
| scimark_sparse_mat_mult    | 5.64 ms                                                                | 5.71 ms: 1.01x slower                                               |
| scimark_sor                | 135 ms                                                                 | 137 ms: 1.01x slower                                                |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                                |
| raytrace                   | 321 ms                                                                 | 326 ms: 1.01x slower                                                |
| hexiom                     | 7.58 ms                                                                | 7.69 ms: 1.01x slower                                               |
| crypto_pyaes               | 87.8 ms                                                                | 89.0 ms: 1.01x slower                                               |
| async_tree_none            | 273 ms                                                                 | 277 ms: 1.01x slower                                                |
| fannkuch                   | 492 ms                                                                 | 500 ms: 1.01x slower                                                |
| comprehensions             | 20.4 us                                                                | 20.8 us: 1.02x slower                                               |
| go                         | 144 ms                                                                 | 146 ms: 1.02x slower                                                |
| chaos                      | 68.2 ms                                                                | 69.4 ms: 1.02x slower                                               |
| regex_dna                  | 169 ms                                                                 | 172 ms: 1.02x slower                                                |
| async_tree_io              | 577 ms                                                                 | 588 ms: 1.02x slower                                                |
| pprint_pformat             | 1.72 sec                                                               | 1.75 sec: 1.02x slower                                              |
| scimark_fft                | 391 ms                                                                 | 400 ms: 1.02x slower                                                |
| logging_silent             | 111 ns                                                                 | 114 ns: 1.02x slower                                                |
| meteor_contest             | 130 ms                                                                 | 133 ms: 1.02x slower                                                |
| scimark_lu                 | 141 ms                                                                 | 144 ms: 1.03x slower                                                |
| html5lib                   | 69.2 ms                                                                | 71.2 ms: 1.03x slower                                               |
| regex_effbot               | 2.77 ms                                                                | 2.85 ms: 1.03x slower                                               |
| nbody                      | 129 ms                                                                 | 137 ms: 1.06x slower                                                |
| mdp                        | 2.60 sec                                                               | 2.78 sec: 1.07x slower                                              |
| async_tree_cpu_io_mixed    | 519 ms                                                                 | 568 ms: 1.09x slower                                                |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 535 ms: 1.10x slower                                                |
| pidigits                   | 191 ms                                                                 | 216 ms: 1.13x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (33): subparsers, sympy_expand, json_loads, docutils, many_optionals, bench_mp_pool, django_template, coverage, asyncio_websockets, python_startup, richards_super, json, shortest_path, pathlib, sphinx, pylint, bench_thread_pool, generators, sqlalchemy_declarative, sympy_str, async_tree_memoization_tg, pycparser, async_tree_memoization, typing_runtime_protocols, logging_simple, sqlglot_v2_normalize, sqlglot_v2_optimize, telco, sqlglot_v2_transpile, spectral_norm, async_tree_none_tg, sqlalchemy_imperative, logging_format

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x