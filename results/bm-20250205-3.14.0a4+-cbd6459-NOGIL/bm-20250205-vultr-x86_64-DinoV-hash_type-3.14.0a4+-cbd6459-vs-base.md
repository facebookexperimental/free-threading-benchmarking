# Results vs. base

- fork: DinoV
- ref: hash_type
- machine: linux-x86_64
- commit hash: cbd6459
- commit date: 2025-02-05
- overall geometric mean: 1.008x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 303 ms: 1.00x slower                                       |
| docutils       | 2.79 sec                                                               | 2.85 sec: 1.02x slower                                     |
| sphinx         | 1.11 sec                                                               | 1.14 sec: 1.03x slower                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| async_generators           | 376 ms                                                                 | 375 ms: 1.00x faster                                       |
| async_tree_io              | 601 ms                                                                 | 604 ms: 1.00x slower                                       |
| async_tree_io_tg           | 569 ms                                                                 | 575 ms: 1.01x slower                                       |
| async_tree_memoization     | 349 ms                                                                 | 352 ms: 1.01x slower                                       |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 504 ms: 1.01x slower                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                                 | 537 ms: 1.01x slower                                       |
| coroutines                 | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                      |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (4): async_tree_none, asyncio_websockets, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 207 ms                                                                 | 193 ms: 1.07x faster                                       |
| float          | 75.2 ms                                                                | 76.6 ms: 1.02x slower                                      |
| nbody          | 132 ms                                                                 | 135 ms: 1.02x slower                                       |
| Geometric mean | (ref)                                                                  | 1.01x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_v8       | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                      |
| regex_effbot   | 2.81 ms                                                                | 2.87 ms: 1.02x slower                                      |
| regex_dna      | 179 ms                                                                 | 183 ms: 1.03x slower                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_process    | 68.9 ms                                                                | 68.4 ms: 1.01x faster                                      |
| xml_etree_generate   | 96.3 ms                                                                | 95.7 ms: 1.01x faster                                      |
| xml_etree_parse      | 126 ms                                                                 | 127 ms: 1.01x slower                                       |
| pickle_pure_python   | 364 us                                                                 | 368 us: 1.01x slower                                       |
| tomli_loads          | 2.29 sec                                                               | 2.32 sec: 1.01x slower                                     |
| unpickle_pure_python | 244 us                                                                 | 250 us: 1.03x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (3): json_loads, xml_etree_iterparse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 9.60 ms                                                                | 9.63 ms: 1.00x slower                                      |
| python_startup         | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                      |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 15.9 ms                                                                | 15.8 ms: 1.00x faster                                      |
| django_template | 42.2 ms                                                                | 42.7 ms: 1.01x slower                                      |
| genshi_xml      | 59.4 ms                                                                | 60.2 ms: 1.01x slower                                      |
| genshi_text     | 27.4 ms                                                                | 28.1 ms: 1.03x slower                                      |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits                   | 207 ms                                                                 | 193 ms: 1.07x faster                                       |
| mdp                        | 2.76 sec                                                               | 2.64 sec: 1.04x faster                                     |
| nqueens                    | 99.9 ms                                                                | 96.0 ms: 1.04x faster                                      |
| richards_super             | 66.3 ms                                                                | 65.0 ms: 1.02x faster                                      |
| meteor_contest             | 130 ms                                                                 | 129 ms: 1.01x faster                                       |
| xml_etree_process          | 68.9 ms                                                                | 68.4 ms: 1.01x faster                                      |
| telco                      | 8.73 ms                                                                | 8.66 ms: 1.01x faster                                      |
| xml_etree_generate         | 96.3 ms                                                                | 95.7 ms: 1.01x faster                                      |
| scimark_sparse_mat_mult    | 5.62 ms                                                                | 5.60 ms: 1.00x faster                                      |
| mako                       | 15.9 ms                                                                | 15.8 ms: 1.00x faster                                      |
| comprehensions             | 20.0 us                                                                | 19.9 us: 1.00x faster                                      |
| async_generators           | 376 ms                                                                 | 375 ms: 1.00x faster                                       |
| python_startup_no_site     | 9.60 ms                                                                | 9.63 ms: 1.00x slower                                      |
| python_startup             | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                      |
| k_core                     | 2.32 sec                                                               | 2.32 sec: 1.00x slower                                     |
| scimark_lu                 | 135 ms                                                                 | 135 ms: 1.00x slower                                       |
| 2to3                       | 301 ms                                                                 | 303 ms: 1.00x slower                                       |
| async_tree_io              | 601 ms                                                                 | 604 ms: 1.00x slower                                       |
| pprint_safe_repr           | 818 ms                                                                 | 822 ms: 1.01x slower                                       |
| richards                   | 56.2 ms                                                                | 56.5 ms: 1.01x slower                                      |
| sympy_str                  | 332 ms                                                                 | 334 ms: 1.01x slower                                       |
| sympy_expand               | 547 ms                                                                 | 551 ms: 1.01x slower                                       |
| deepcopy_memo              | 38.0 us                                                                | 38.3 us: 1.01x slower                                      |
| sqlglot_parse              | 1.57 ms                                                                | 1.58 ms: 1.01x slower                                      |
| regex_v8                   | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                      |
| async_tree_io_tg           | 569 ms                                                                 | 575 ms: 1.01x slower                                       |
| xml_etree_parse            | 126 ms                                                                 | 127 ms: 1.01x slower                                       |
| logging_format             | 8.09 us                                                                | 8.17 us: 1.01x slower                                      |
| async_tree_memoization     | 349 ms                                                                 | 352 ms: 1.01x slower                                       |
| pickle_pure_python         | 364 us                                                                 | 368 us: 1.01x slower                                       |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 504 ms: 1.01x slower                                       |
| scimark_fft                | 378 ms                                                                 | 383 ms: 1.01x slower                                       |
| fannkuch                   | 480 ms                                                                 | 486 ms: 1.01x slower                                       |
| django_template            | 42.2 ms                                                                | 42.7 ms: 1.01x slower                                      |
| create_gc_cycles           | 1.37 ms                                                                | 1.39 ms: 1.01x slower                                      |
| async_tree_cpu_io_mixed    | 530 ms                                                                 | 537 ms: 1.01x slower                                       |
| tomli_loads                | 2.29 sec                                                               | 2.32 sec: 1.01x slower                                     |
| hexiom                     | 7.29 ms                                                                | 7.39 ms: 1.01x slower                                      |
| genshi_xml                 | 59.4 ms                                                                | 60.2 ms: 1.01x slower                                      |
| logging_simple             | 7.14 us                                                                | 7.24 us: 1.01x slower                                      |
| pycparser                  | 1.18 sec                                                               | 1.19 sec: 1.01x slower                                     |
| scimark_monte_carlo        | 81.3 ms                                                                | 82.6 ms: 1.02x slower                                      |
| sympy_integrate            | 23.9 ms                                                                | 24.3 ms: 1.02x slower                                      |
| sqlglot_optimize           | 60.8 ms                                                                | 61.9 ms: 1.02x slower                                      |
| float                      | 75.2 ms                                                                | 76.6 ms: 1.02x slower                                      |
| docutils                   | 2.79 sec                                                               | 2.85 sec: 1.02x slower                                     |
| sqlglot_transpile          | 1.88 ms                                                                | 1.92 ms: 1.02x slower                                      |
| scimark_sor                | 130 ms                                                                 | 132 ms: 1.02x slower                                       |
| crypto_pyaes               | 86.3 ms                                                                | 88.1 ms: 1.02x slower                                      |
| nbody                      | 132 ms                                                                 | 135 ms: 1.02x slower                                       |
| coroutines                 | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                      |
| regex_effbot               | 2.81 ms                                                                | 2.87 ms: 1.02x slower                                      |
| sqlalchemy_declarative     | 156 ms                                                                 | 160 ms: 1.02x slower                                       |
| genshi_text                | 27.4 ms                                                                | 28.1 ms: 1.03x slower                                      |
| sphinx                     | 1.11 sec                                                               | 1.14 sec: 1.03x slower                                     |
| regex_dna                  | 179 ms                                                                 | 183 ms: 1.03x slower                                       |
| spectral_norm              | 106 ms                                                                 | 109 ms: 1.03x slower                                       |
| unpickle_pure_python       | 244 us                                                                 | 250 us: 1.03x slower                                       |
| chaos                      | 68.2 ms                                                                | 70.2 ms: 1.03x slower                                      |
| sqlglot_normalize          | 120 ms                                                                 | 123 ms: 1.03x slower                                       |
| deltablue                  | 4.60 ms                                                                | 4.75 ms: 1.03x slower                                      |
| raytrace                   | 319 ms                                                                 | 329 ms: 1.03x slower                                       |
| logging_silent             | 109 ns                                                                 | 113 ns: 1.04x slower                                       |
| sqlalchemy_imperative      | 23.5 ms                                                                | 24.4 ms: 1.04x slower                                      |
| go                         | 134 ms                                                                 | 139 ms: 1.04x slower                                       |
| pyflate                    | 484 ms                                                                 | 511 ms: 1.06x slower                                       |
| gc_traversal               | 1.62 ms                                                                | 1.76 ms: 1.08x slower                                      |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (29): thrift, sqlite_synth, coverage, json, pathlib, html5lib, async_tree_none, deepcopy_reduce, connected_components, bench_thread_pool, bpe_tokeniser, regex_compile, shortest_path, json_loads, asyncio_websockets, xml_etree_iterparse, many_optionals, generators, pprint_pformat, json_dumps, sympy_sum, dulwich_log, bench_mp_pool, typing_runtime_protocols, async_tree_none_tg, deepcopy, async_tree_memoization_tg, subparsers, pylint

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x