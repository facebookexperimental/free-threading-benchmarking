# Results vs. base

- fork: Yhg1s
- ref: load_const_defer
- machine: linux-x86_64
- commit hash: fcfb942
- commit date: 2025-01-29
- overall geometric mean: 1.008x slower
- HPT reliability: 91.41%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 311 ms: 1.00x slower                                              |
| html5lib       | 70.6 ms                                                                | 72.5 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_generators           | 384 ms                                                                 | 376 ms: 1.02x faster                                              |
| coroutines                 | 25.3 ms                                                                | 24.9 ms: 1.01x faster                                             |
| async_tree_io              | 621 ms                                                                 | 617 ms: 1.01x faster                                              |
| async_tree_memoization_tg  | 326 ms                                                                 | 330 ms: 1.01x slower                                              |
| async_tree_none_tg         | 254 ms                                                                 | 258 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed    | 550 ms                                                                 | 629 ms: 1.14x slower                                              |
| async_tree_cpu_io_mixed_tg | 518 ms                                                                 | 604 ms: 1.17x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                      |

Benchmark hidden because not significant (4): async_tree_memoization, asyncio_websockets, async_tree_none, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 79.2 ms                                                                | 78.1 ms: 1.01x faster                                             |
| nbody          | 138 ms                                                                 | 143 ms: 1.04x slower                                              |
| pidigits       | 198 ms                                                                 | 227 ms: 1.15x slower                                              |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 2.87 ms                                                                | 2.84 ms: 1.01x faster                                             |
| regex_v8       | 23.1 ms                                                                | 23.5 ms: 1.01x slower                                             |
| regex_dna      | 177 ms                                                                 | 188 ms: 1.06x slower                                              |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                      |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_loads           | 31.6 us                                                                | 30.9 us: 1.02x faster                                             |
| tomli_loads          | 2.43 sec                                                               | 2.41 sec: 1.01x faster                                            |
| xml_etree_process    | 70.4 ms                                                                | 70.0 ms: 1.01x faster                                             |
| pickle_pure_python   | 385 us                                                                 | 383 us: 1.01x faster                                              |
| xml_etree_generate   | 97.9 ms                                                                | 97.5 ms: 1.00x faster                                             |
| unpickle_pure_python | 256 us                                                                 | 258 us: 1.01x slower                                              |
| json_dumps           | 13.1 ms                                                                | 13.2 ms: 1.01x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.2 ms: 1.00x faster                                             |
| python_startup_no_site | 9.59 ms                                                                | 9.57 ms: 1.00x faster                                             |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 16.2 ms                                                                | 16.0 ms: 1.02x faster                                             |
| genshi_text     | 28.6 ms                                                                | 28.7 ms: 1.00x slower                                             |
| django_template | 43.3 ms                                                                | 43.7 ms: 1.01x slower                                             |
| genshi_xml      | 61.5 ms                                                                | 62.3 ms: 1.01x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250129-vultr-x86_64-python-25cf79a0829422bd8479-3.14.0a4+-25cf79a | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_loads                 | 31.6 us                                                                | 30.9 us: 1.02x faster                                             |
| async_generators           | 384 ms                                                                 | 376 ms: 1.02x faster                                              |
| scimark_sparse_mat_mult    | 5.77 ms                                                                | 5.67 ms: 1.02x faster                                             |
| mako                       | 16.2 ms                                                                | 16.0 ms: 1.02x faster                                             |
| pyflate                    | 515 ms                                                                 | 507 ms: 1.02x faster                                              |
| coroutines                 | 25.3 ms                                                                | 24.9 ms: 1.01x faster                                             |
| float                      | 79.2 ms                                                                | 78.1 ms: 1.01x faster                                             |
| nqueens                    | 98.9 ms                                                                | 97.6 ms: 1.01x faster                                             |
| fannkuch                   | 493 ms                                                                 | 488 ms: 1.01x faster                                              |
| comprehensions             | 20.3 us                                                                | 20.1 us: 1.01x faster                                             |
| regex_effbot               | 2.87 ms                                                                | 2.84 ms: 1.01x faster                                             |
| scimark_lu                 | 142 ms                                                                 | 140 ms: 1.01x faster                                              |
| bpe_tokeniser              | 4.70 sec                                                               | 4.66 sec: 1.01x faster                                            |
| telco                      | 8.75 ms                                                                | 8.69 ms: 1.01x faster                                             |
| coverage                   | 98.4 ms                                                                | 97.7 ms: 1.01x faster                                             |
| async_tree_io              | 621 ms                                                                 | 617 ms: 1.01x faster                                              |
| tomli_loads                | 2.43 sec                                                               | 2.41 sec: 1.01x faster                                            |
| crypto_pyaes               | 89.4 ms                                                                | 88.9 ms: 1.01x faster                                             |
| xml_etree_process          | 70.4 ms                                                                | 70.0 ms: 1.01x faster                                             |
| pickle_pure_python         | 385 us                                                                 | 383 us: 1.01x faster                                              |
| scimark_sor                | 140 ms                                                                 | 139 ms: 1.00x faster                                              |
| many_optionals             | 1.20 ms                                                                | 1.20 ms: 1.00x faster                                             |
| create_gc_cycles           | 1.35 ms                                                                | 1.35 ms: 1.00x faster                                             |
| xml_etree_generate         | 97.9 ms                                                                | 97.5 ms: 1.00x faster                                             |
| bench_mp_pool              | 95.3 ms                                                                | 94.9 ms: 1.00x faster                                             |
| python_startup             | 15.3 ms                                                                | 15.2 ms: 1.00x faster                                             |
| spectral_norm              | 115 ms                                                                 | 114 ms: 1.00x faster                                              |
| python_startup_no_site     | 9.59 ms                                                                | 9.57 ms: 1.00x faster                                             |
| sympy_str                  | 340 ms                                                                 | 341 ms: 1.00x slower                                              |
| genshi_text                | 28.6 ms                                                                | 28.7 ms: 1.00x slower                                             |
| pprint_safe_repr           | 826 ms                                                                 | 830 ms: 1.00x slower                                              |
| sympy_sum                  | 189 ms                                                                 | 190 ms: 1.00x slower                                              |
| sqlalchemy_declarative     | 161 ms                                                                 | 162 ms: 1.00x slower                                              |
| 2to3                       | 310 ms                                                                 | 311 ms: 1.00x slower                                              |
| bench_thread_pool          | 3.31 ms                                                                | 3.33 ms: 1.01x slower                                             |
| deltablue                  | 4.77 ms                                                                | 4.79 ms: 1.01x slower                                             |
| sqlglot_parse              | 1.63 ms                                                                | 1.64 ms: 1.01x slower                                             |
| pathlib                    | 18.9 ms                                                                | 19.0 ms: 1.01x slower                                             |
| scimark_fft                | 396 ms                                                                 | 399 ms: 1.01x slower                                              |
| logging_silent             | 122 ns                                                                 | 123 ns: 1.01x slower                                              |
| sympy_expand               | 557 ms                                                                 | 562 ms: 1.01x slower                                              |
| django_template            | 43.3 ms                                                                | 43.7 ms: 1.01x slower                                             |
| pprint_pformat             | 1.71 sec                                                               | 1.72 sec: 1.01x slower                                            |
| unpickle_pure_python       | 256 us                                                                 | 258 us: 1.01x slower                                              |
| deepcopy                   | 316 us                                                                 | 320 us: 1.01x slower                                              |
| go                         | 141 ms                                                                 | 143 ms: 1.01x slower                                              |
| json_dumps                 | 13.1 ms                                                                | 13.2 ms: 1.01x slower                                             |
| sqlglot_transpile          | 1.95 ms                                                                | 1.97 ms: 1.01x slower                                             |
| async_tree_memoization_tg  | 326 ms                                                                 | 330 ms: 1.01x slower                                              |
| genshi_xml                 | 61.5 ms                                                                | 62.3 ms: 1.01x slower                                             |
| regex_v8                   | 23.1 ms                                                                | 23.5 ms: 1.01x slower                                             |
| logging_format             | 8.52 us                                                                | 8.63 us: 1.01x slower                                             |
| async_tree_none_tg         | 254 ms                                                                 | 258 ms: 1.01x slower                                              |
| pycparser                  | 1.19 sec                                                               | 1.21 sec: 1.02x slower                                            |
| richards_super             | 67.7 ms                                                                | 69.0 ms: 1.02x slower                                             |
| scimark_monte_carlo        | 83.3 ms                                                                | 84.9 ms: 1.02x slower                                             |
| thrift                     | 916 us                                                                 | 935 us: 1.02x slower                                              |
| deepcopy_reduce            | 3.26 us                                                                | 3.33 us: 1.02x slower                                             |
| raytrace                   | 334 ms                                                                 | 342 ms: 1.02x slower                                              |
| mdp                        | 2.62 sec                                                               | 2.68 sec: 1.03x slower                                            |
| html5lib                   | 70.6 ms                                                                | 72.5 ms: 1.03x slower                                             |
| nbody                      | 138 ms                                                                 | 143 ms: 1.04x slower                                              |
| regex_dna                  | 177 ms                                                                 | 188 ms: 1.06x slower                                              |
| gc_traversal               | 3.14 ms                                                                | 3.36 ms: 1.07x slower                                             |
| async_tree_cpu_io_mixed    | 550 ms                                                                 | 629 ms: 1.14x slower                                              |
| pidigits                   | 198 ms                                                                 | 227 ms: 1.15x slower                                              |
| async_tree_cpu_io_mixed_tg | 518 ms                                                                 | 604 ms: 1.17x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                      |

Benchmark hidden because not significant (29): json, generators, sqlite_synth, richards, meteor_contest, sqlglot_optimize, async_tree_memoization, asyncio_websockets, pylint, async_tree_none, sphinx, sqlglot_normalize, sympy_integrate, xml_etree_iterparse, xml_etree_parse, typing_runtime_protocols, k_core, async_tree_io_tg, hexiom, logging_simple, chaos, sqlalchemy_imperative, dulwich_log, connected_components, deepcopy_memo, regex_compile, subparsers, docutils, shortest_path

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 91.41% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x