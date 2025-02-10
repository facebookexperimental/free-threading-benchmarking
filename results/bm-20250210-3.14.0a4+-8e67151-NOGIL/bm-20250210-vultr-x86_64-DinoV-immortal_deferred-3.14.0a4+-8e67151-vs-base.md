# Results vs. base

- fork: DinoV
- ref: immortal_deferred
- machine: linux-x86_64
- commit hash: 8e67151
- commit date: 2025-02-10
- overall geometric mean: 1.004x slower
- HPT reliability: 98.77%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 302 ms: 1.00x slower                                               |
| html5lib       | 70.4 ms                                                                | 69.9 ms: 1.01x faster                                              |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                       |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| coroutines                 | 23.4 ms                                                                | 23.2 ms: 1.01x faster                                              |
| async_generators           | 376 ms                                                                 | 374 ms: 1.01x faster                                               |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                               |
| async_tree_io              | 601 ms                                                                 | 605 ms: 1.01x slower                                               |
| async_tree_memoization     | 349 ms                                                                 | 351 ms: 1.01x slower                                               |
| async_tree_memoization_tg  | 317 ms                                                                 | 320 ms: 1.01x slower                                               |
| async_tree_io_tg           | 569 ms                                                                 | 577 ms: 1.01x slower                                               |
| async_tree_none_tg         | 249 ms                                                                 | 252 ms: 1.01x slower                                               |
| async_tree_none            | 286 ms                                                                 | 291 ms: 1.02x slower                                               |
| async_tree_cpu_io_mixed    | 530 ms                                                                 | 555 ms: 1.05x slower                                               |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 523 ms: 1.05x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 207 ms                                                                 | 200 ms: 1.03x faster                                               |
| nbody          | 132 ms                                                                 | 135 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                       |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_compile  | 149 ms                                                                 | 148 ms: 1.01x faster                                               |
| regex_v8       | 23.5 ms                                                                | 24.2 ms: 1.03x slower                                              |
| regex_effbot   | 2.81 ms                                                                | 2.92 ms: 1.04x slower                                              |
| regex_dna      | 179 ms                                                                 | 186 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| json_dumps           | 12.8 ms                                                                | 12.7 ms: 1.01x faster                                              |
| xml_etree_generate   | 96.3 ms                                                                | 95.8 ms: 1.01x faster                                              |
| json_loads           | 31.2 us                                                                | 31.1 us: 1.00x faster                                              |
| xml_etree_parse      | 126 ms                                                                 | 127 ms: 1.00x slower                                               |
| tomli_loads          | 2.29 sec                                                               | 2.30 sec: 1.01x slower                                             |
| xml_etree_iterparse  | 87.0 ms                                                                | 88.0 ms: 1.01x slower                                              |
| unpickle_pure_python | 244 us                                                                 | 250 us: 1.03x slower                                               |
| pickle_pure_python   | 364 us                                                                 | 374 us: 1.03x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                       |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                       |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| mako            | 15.9 ms                                                                | 16.0 ms: 1.01x slower                                              |
| django_template | 42.2 ms                                                                | 42.6 ms: 1.01x slower                                              |
| genshi_xml      | 59.4 ms                                                                | 60.4 ms: 1.02x slower                                              |
| genshi_text     | 27.4 ms                                                                | 28.1 ms: 1.03x slower                                              |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| deltablue                  | 4.60 ms                                                                | 3.86 ms: 1.19x faster                                              |
| pidigits                   | 207 ms                                                                 | 200 ms: 1.03x faster                                               |
| nqueens                    | 99.9 ms                                                                | 96.9 ms: 1.03x faster                                              |
| thrift                     | 914 us                                                                 | 894 us: 1.02x faster                                               |
| mdp                        | 2.76 sec                                                               | 2.72 sec: 1.02x faster                                             |
| pprint_pformat             | 1.69 sec                                                               | 1.67 sec: 1.01x faster                                             |
| json                       | 5.42 ms                                                                | 5.36 ms: 1.01x faster                                              |
| json_dumps                 | 12.8 ms                                                                | 12.7 ms: 1.01x faster                                              |
| sqlite_synth               | 2.04 us                                                                | 2.02 us: 1.01x faster                                              |
| coroutines                 | 23.4 ms                                                                | 23.2 ms: 1.01x faster                                              |
| typing_runtime_protocols   | 200 us                                                                 | 198 us: 1.01x faster                                               |
| pprint_safe_repr           | 818 ms                                                                 | 811 ms: 1.01x faster                                               |
| telco                      | 8.73 ms                                                                | 8.66 ms: 1.01x faster                                              |
| logging_silent             | 109 ns                                                                 | 108 ns: 1.01x faster                                               |
| sympy_sum                  | 185 ms                                                                 | 184 ms: 1.01x faster                                               |
| spectral_norm              | 106 ms                                                                 | 105 ms: 1.01x faster                                               |
| html5lib                   | 70.4 ms                                                                | 69.9 ms: 1.01x faster                                              |
| async_generators           | 376 ms                                                                 | 374 ms: 1.01x faster                                               |
| regex_compile              | 149 ms                                                                 | 148 ms: 1.01x faster                                               |
| xml_etree_generate         | 96.3 ms                                                                | 95.8 ms: 1.01x faster                                              |
| many_optionals             | 1.17 ms                                                                | 1.16 ms: 1.00x faster                                              |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                               |
| bench_thread_pool          | 3.31 ms                                                                | 3.30 ms: 1.00x faster                                              |
| json_loads                 | 31.2 us                                                                | 31.1 us: 1.00x faster                                              |
| bpe_tokeniser              | 4.62 sec                                                               | 4.62 sec: 1.00x faster                                             |
| python_startup             | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                              |
| 2to3                       | 301 ms                                                                 | 302 ms: 1.00x slower                                               |
| comprehensions             | 20.0 us                                                                | 20.1 us: 1.00x slower                                              |
| xml_etree_parse            | 126 ms                                                                 | 127 ms: 1.00x slower                                               |
| hexiom                     | 7.29 ms                                                                | 7.32 ms: 1.00x slower                                              |
| pycparser                  | 1.18 sec                                                               | 1.18 sec: 1.00x slower                                             |
| dulwich_log                | 81.5 ms                                                                | 81.9 ms: 1.00x slower                                              |
| sympy_integrate            | 23.9 ms                                                                | 24.0 ms: 1.00x slower                                              |
| sympy_str                  | 332 ms                                                                 | 334 ms: 1.00x slower                                               |
| pyflate                    | 484 ms                                                                 | 487 ms: 1.01x slower                                               |
| tomli_loads                | 2.29 sec                                                               | 2.30 sec: 1.01x slower                                             |
| logging_simple             | 7.14 us                                                                | 7.18 us: 1.01x slower                                              |
| async_tree_io              | 601 ms                                                                 | 605 ms: 1.01x slower                                               |
| sqlalchemy_declarative     | 156 ms                                                                 | 157 ms: 1.01x slower                                               |
| mako                       | 15.9 ms                                                                | 16.0 ms: 1.01x slower                                              |
| async_tree_memoization     | 349 ms                                                                 | 351 ms: 1.01x slower                                               |
| async_tree_memoization_tg  | 317 ms                                                                 | 320 ms: 1.01x slower                                               |
| django_template            | 42.2 ms                                                                | 42.6 ms: 1.01x slower                                              |
| xml_etree_iterparse        | 87.0 ms                                                                | 88.0 ms: 1.01x slower                                              |
| deepcopy_memo              | 38.0 us                                                                | 38.4 us: 1.01x slower                                              |
| scimark_lu                 | 135 ms                                                                 | 136 ms: 1.01x slower                                               |
| chaos                      | 68.2 ms                                                                | 68.9 ms: 1.01x slower                                              |
| scimark_sparse_mat_mult    | 5.62 ms                                                                | 5.70 ms: 1.01x slower                                              |
| logging_format             | 8.09 us                                                                | 8.20 us: 1.01x slower                                              |
| async_tree_io_tg           | 569 ms                                                                 | 577 ms: 1.01x slower                                               |
| async_tree_none_tg         | 249 ms                                                                 | 252 ms: 1.01x slower                                               |
| scimark_monte_carlo        | 81.3 ms                                                                | 82.6 ms: 1.02x slower                                              |
| genshi_xml                 | 59.4 ms                                                                | 60.4 ms: 1.02x slower                                              |
| nbody                      | 132 ms                                                                 | 135 ms: 1.02x slower                                               |
| fannkuch                   | 480 ms                                                                 | 488 ms: 1.02x slower                                               |
| async_tree_none            | 286 ms                                                                 | 291 ms: 1.02x slower                                               |
| go                         | 134 ms                                                                 | 137 ms: 1.02x slower                                               |
| unpickle_pure_python       | 244 us                                                                 | 250 us: 1.03x slower                                               |
| pickle_pure_python         | 364 us                                                                 | 374 us: 1.03x slower                                               |
| scimark_fft                | 378 ms                                                                 | 388 ms: 1.03x slower                                               |
| regex_v8                   | 23.5 ms                                                                | 24.2 ms: 1.03x slower                                              |
| genshi_text                | 27.4 ms                                                                | 28.1 ms: 1.03x slower                                              |
| crypto_pyaes               | 86.3 ms                                                                | 88.7 ms: 1.03x slower                                              |
| raytrace                   | 319 ms                                                                 | 328 ms: 1.03x slower                                               |
| regex_effbot               | 2.81 ms                                                                | 2.92 ms: 1.04x slower                                              |
| regex_dna                  | 179 ms                                                                 | 186 ms: 1.04x slower                                               |
| async_tree_cpu_io_mixed    | 530 ms                                                                 | 555 ms: 1.05x slower                                               |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 523 ms: 1.05x slower                                               |
| gc_traversal               | 1.62 ms                                                                | 1.73 ms: 1.07x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                       |

Benchmark hidden because not significant (27): meteor_contest, coverage, xml_etree_process, float, sphinx, docutils, sympy_expand, k_core, pylint, sqlglot_parse, python_startup_no_site, connected_components, pathlib, deepcopy_reduce, deepcopy, scimark_sor, create_gc_cycles, richards, sqlglot_optimize, subparsers, bench_mp_pool, shortest_path, sqlglot_normalize, sqlglot_transpile, sqlalchemy_imperative, richards_super, generators

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 98.77% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x