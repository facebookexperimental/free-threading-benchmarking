# Results vs. base

- fork: DinoV
- ref: hash_type
- machine: linux-x86_64
- commit hash: cbd6459
- commit date: 2025-02-05
- overall geometric mean: 1.007x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 302 ms: 1.00x slower                                       |
| docutils       | 2.79 sec                                                               | 2.85 sec: 1.02x slower                                     |
| html5lib       | 70.4 ms                                                                | 70.7 ms: 1.01x slower                                      |
| sphinx         | 1.11 sec                                                               | 1.13 sec: 1.02x slower                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| async_generators           | 376 ms                                                                 | 374 ms: 1.00x faster                                       |
| coroutines                 | 23.4 ms                                                                | 23.3 ms: 1.00x faster                                      |
| async_tree_none_tg         | 249 ms                                                                 | 251 ms: 1.01x slower                                       |
| async_tree_memoization_tg  | 317 ms                                                                 | 323 ms: 1.02x slower                                       |
| async_tree_io_tg           | 569 ms                                                                 | 580 ms: 1.02x slower                                       |
| async_tree_io              | 601 ms                                                                 | 613 ms: 1.02x slower                                       |
| async_tree_none            | 286 ms                                                                 | 293 ms: 1.02x slower                                       |
| async_tree_memoization     | 349 ms                                                                 | 361 ms: 1.03x slower                                       |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 516 ms: 1.03x slower                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                                 | 552 ms: 1.04x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                               |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 207 ms                                                                 | 193 ms: 1.07x faster                                       |
| float          | 75.2 ms                                                                | 75.6 ms: 1.01x slower                                      |
| nbody          | 132 ms                                                                 | 134 ms: 1.01x slower                                       |
| Geometric mean | (ref)                                                                  | 1.02x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 2.81 ms                                                                | 2.77 ms: 1.01x faster                                      |
| regex_dna      | 179 ms                                                                 | 177 ms: 1.01x faster                                       |
| regex_v8       | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                               |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| json_loads           | 31.2 us                                                                | 31.0 us: 1.01x faster                                      |
| xml_etree_process    | 68.9 ms                                                                | 69.1 ms: 1.00x slower                                      |
| xml_etree_generate   | 96.3 ms                                                                | 96.7 ms: 1.00x slower                                      |
| xml_etree_parse      | 126 ms                                                                 | 127 ms: 1.01x slower                                       |
| xml_etree_iterparse  | 87.0 ms                                                                | 87.5 ms: 1.01x slower                                      |
| json_dumps           | 12.8 ms                                                                | 12.9 ms: 1.01x slower                                      |
| unpickle_pure_python | 244 us                                                                 | 245 us: 1.01x slower                                       |
| pickle_pure_python   | 364 us                                                                 | 376 us: 1.03x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                      |
| python_startup_no_site | 9.60 ms                                                                | 9.63 ms: 1.00x slower                                      |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 59.4 ms                                                                | 59.9 ms: 1.01x slower                                      |
| mako            | 15.9 ms                                                                | 16.0 ms: 1.01x slower                                      |
| django_template | 42.2 ms                                                                | 42.6 ms: 1.01x slower                                      |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| mdp                        | 2.76 sec                                                               | 2.58 sec: 1.07x faster                                     |
| pidigits                   | 207 ms                                                                 | 193 ms: 1.07x faster                                       |
| nqueens                    | 99.9 ms                                                                | 96.5 ms: 1.04x faster                                      |
| telco                      | 8.73 ms                                                                | 8.55 ms: 1.02x faster                                      |
| comprehensions             | 20.0 us                                                                | 19.8 us: 1.01x faster                                      |
| pprint_safe_repr           | 818 ms                                                                 | 808 ms: 1.01x faster                                       |
| regex_effbot               | 2.81 ms                                                                | 2.77 ms: 1.01x faster                                      |
| meteor_contest             | 130 ms                                                                 | 129 ms: 1.01x faster                                       |
| regex_dna                  | 179 ms                                                                 | 177 ms: 1.01x faster                                       |
| coverage                   | 97.8 ms                                                                | 96.9 ms: 1.01x faster                                      |
| typing_runtime_protocols   | 200 us                                                                 | 198 us: 1.01x faster                                       |
| pprint_pformat             | 1.69 sec                                                               | 1.67 sec: 1.01x faster                                     |
| richards_super             | 66.3 ms                                                                | 65.8 ms: 1.01x faster                                      |
| json_loads                 | 31.2 us                                                                | 31.0 us: 1.01x faster                                      |
| async_generators           | 376 ms                                                                 | 374 ms: 1.00x faster                                       |
| coroutines                 | 23.4 ms                                                                | 23.3 ms: 1.00x faster                                      |
| 2to3                       | 301 ms                                                                 | 302 ms: 1.00x slower                                       |
| python_startup             | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                      |
| python_startup_no_site     | 9.60 ms                                                                | 9.63 ms: 1.00x slower                                      |
| hexiom                     | 7.29 ms                                                                | 7.31 ms: 1.00x slower                                      |
| xml_etree_process          | 68.9 ms                                                                | 69.1 ms: 1.00x slower                                      |
| xml_etree_generate         | 96.3 ms                                                                | 96.7 ms: 1.00x slower                                      |
| many_optionals             | 1.17 ms                                                                | 1.17 ms: 1.00x slower                                      |
| float                      | 75.2 ms                                                                | 75.6 ms: 1.01x slower                                      |
| html5lib                   | 70.4 ms                                                                | 70.7 ms: 1.01x slower                                      |
| bench_mp_pool              | 94.3 ms                                                                | 94.8 ms: 1.01x slower                                      |
| xml_etree_parse            | 126 ms                                                                 | 127 ms: 1.01x slower                                       |
| scimark_fft                | 378 ms                                                                 | 380 ms: 1.01x slower                                       |
| deepcopy_memo              | 38.0 us                                                                | 38.2 us: 1.01x slower                                      |
| xml_etree_iterparse        | 87.0 ms                                                                | 87.5 ms: 1.01x slower                                      |
| shortest_path              | 545 ms                                                                 | 548 ms: 1.01x slower                                       |
| go                         | 134 ms                                                                 | 135 ms: 1.01x slower                                       |
| sqlglot_parse              | 1.57 ms                                                                | 1.58 ms: 1.01x slower                                      |
| dulwich_log                | 81.5 ms                                                                | 82.0 ms: 1.01x slower                                      |
| deltablue                  | 4.60 ms                                                                | 4.63 ms: 1.01x slower                                      |
| json_dumps                 | 12.8 ms                                                                | 12.9 ms: 1.01x slower                                      |
| regex_v8                   | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                      |
| unpickle_pure_python       | 244 us                                                                 | 245 us: 1.01x slower                                       |
| genshi_xml                 | 59.4 ms                                                                | 59.9 ms: 1.01x slower                                      |
| chaos                      | 68.2 ms                                                                | 68.7 ms: 1.01x slower                                      |
| mako                       | 15.9 ms                                                                | 16.0 ms: 1.01x slower                                      |
| bpe_tokeniser              | 4.62 sec                                                               | 4.66 sec: 1.01x slower                                     |
| sympy_sum                  | 185 ms                                                                 | 187 ms: 1.01x slower                                       |
| scimark_monte_carlo        | 81.3 ms                                                                | 82.1 ms: 1.01x slower                                      |
| async_tree_none_tg         | 249 ms                                                                 | 251 ms: 1.01x slower                                       |
| sympy_str                  | 332 ms                                                                 | 336 ms: 1.01x slower                                       |
| nbody                      | 132 ms                                                                 | 134 ms: 1.01x slower                                       |
| django_template            | 42.2 ms                                                                | 42.6 ms: 1.01x slower                                      |
| richards                   | 56.2 ms                                                                | 57.0 ms: 1.01x slower                                      |
| deepcopy                   | 309 us                                                                 | 314 us: 1.01x slower                                       |
| sqlite_synth               | 2.04 us                                                                | 2.07 us: 1.01x slower                                      |
| raytrace                   | 319 ms                                                                 | 323 ms: 1.01x slower                                       |
| spectral_norm              | 106 ms                                                                 | 108 ms: 1.01x slower                                       |
| fannkuch                   | 480 ms                                                                 | 487 ms: 1.01x slower                                       |
| scimark_lu                 | 135 ms                                                                 | 137 ms: 1.02x slower                                       |
| async_tree_memoization_tg  | 317 ms                                                                 | 323 ms: 1.02x slower                                       |
| sqlglot_transpile          | 1.88 ms                                                                | 1.91 ms: 1.02x slower                                      |
| async_tree_io_tg           | 569 ms                                                                 | 580 ms: 1.02x slower                                       |
| logging_simple             | 7.14 us                                                                | 7.27 us: 1.02x slower                                      |
| sqlglot_optimize           | 60.8 ms                                                                | 61.9 ms: 1.02x slower                                      |
| async_tree_io              | 601 ms                                                                 | 613 ms: 1.02x slower                                       |
| sympy_integrate            | 23.9 ms                                                                | 24.3 ms: 1.02x slower                                      |
| logging_format             | 8.09 us                                                                | 8.25 us: 1.02x slower                                      |
| scimark_sparse_mat_mult    | 5.62 ms                                                                | 5.74 ms: 1.02x slower                                      |
| docutils                   | 2.79 sec                                                               | 2.85 sec: 1.02x slower                                     |
| scimark_sor                | 130 ms                                                                 | 132 ms: 1.02x slower                                       |
| create_gc_cycles           | 1.37 ms                                                                | 1.40 ms: 1.02x slower                                      |
| crypto_pyaes               | 86.3 ms                                                                | 88.3 ms: 1.02x slower                                      |
| sqlalchemy_declarative     | 156 ms                                                                 | 160 ms: 1.02x slower                                       |
| async_tree_none            | 286 ms                                                                 | 293 ms: 1.02x slower                                       |
| sphinx                     | 1.11 sec                                                               | 1.13 sec: 1.02x slower                                     |
| pyflate                    | 484 ms                                                                 | 497 ms: 1.03x slower                                       |
| pickle_pure_python         | 364 us                                                                 | 376 us: 1.03x slower                                       |
| sqlglot_normalize          | 120 ms                                                                 | 123 ms: 1.03x slower                                       |
| async_tree_memoization     | 349 ms                                                                 | 361 ms: 1.03x slower                                       |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 516 ms: 1.03x slower                                       |
| sqlalchemy_imperative      | 23.5 ms                                                                | 24.4 ms: 1.04x slower                                      |
| async_tree_cpu_io_mixed    | 530 ms                                                                 | 552 ms: 1.04x slower                                       |
| gc_traversal               | 1.62 ms                                                                | 1.76 ms: 1.08x slower                                      |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (17): thrift, regex_compile, json, logging_silent, bench_thread_pool, asyncio_websockets, tomli_loads, generators, subparsers, genshi_text, sympy_expand, k_core, pycparser, deepcopy_reduce, connected_components, pathlib, pylint

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x