# Results vs. base

- fork: DinoV
- ref: noclock_clear
- machine: linux-x86_64
- commit hash: 08975df
- commit date: 2025-02-04
- overall geometric mean: 1.012x slower
- HPT reliability: 95.30%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 303 ms: 1.00x slower                                           |
| html5lib       | 70.4 ms                                                                | 69.0 ms: 1.02x faster                                          |
| sphinx         | 1.11 sec                                                               | 1.09 sec: 1.01x faster                                         |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                   |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_generators       | 376 ms                                                                 | 373 ms: 1.01x faster                                           |
| asyncio_websockets     | 518 ms                                                                 | 516 ms: 1.00x faster                                           |
| async_tree_memoization | 349 ms                                                                 | 351 ms: 1.01x slower                                           |
| coroutines             | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                          |
| async_tree_io          | 601 ms                                                                 | 608 ms: 1.01x slower                                           |
| async_tree_io_tg       | 569 ms                                                                 | 577 ms: 1.01x slower                                           |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                   |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 207 ms                                                                 | 190 ms: 1.09x faster                                           |
| float          | 75.2 ms                                                                | 76.7 ms: 1.02x slower                                          |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                   |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_v8       | 23.5 ms                                                                | 23.3 ms: 1.01x faster                                          |
| regex_compile  | 149 ms                                                                 | 148 ms: 1.01x faster                                           |
| regex_effbot   | 2.81 ms                                                                | 2.82 ms: 1.00x slower                                          |
| regex_dna      | 179 ms                                                                 | 185 ms: 1.03x slower                                           |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| tomli_loads          | 2.29 sec                                                               | 2.30 sec: 1.01x slower                                         |
| unpickle_pure_python | 244 us                                                                 | 246 us: 1.01x slower                                           |
| xml_etree_iterparse  | 87.0 ms                                                                | 87.9 ms: 1.01x slower                                          |
| json_loads           | 31.2 us                                                                | 31.6 us: 1.01x slower                                          |
| pickle_pure_python   | 364 us                                                                 | 369 us: 1.01x slower                                           |
| xml_etree_parse      | 126 ms                                                                 | 130 ms: 1.03x slower                                           |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                   |

Benchmark hidden because not significant (3): json_dumps, xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 9.60 ms                                                                | 9.62 ms: 1.00x slower                                          |
| python_startup         | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                          |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| mako            | 15.9 ms                                                                | 16.0 ms: 1.00x slower                                          |
| genshi_text     | 27.4 ms                                                                | 27.5 ms: 1.01x slower                                          |
| genshi_xml      | 59.4 ms                                                                | 60.0 ms: 1.01x slower                                          |
| django_template | 42.2 ms                                                                | 42.6 ms: 1.01x slower                                          |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                   |

All benchmarks:
===============

| Benchmark                | bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4+-49f2465 | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits                 | 207 ms                                                                 | 190 ms: 1.09x faster                                           |
| mdp                      | 2.76 sec                                                               | 2.63 sec: 1.05x faster                                         |
| nqueens                  | 99.9 ms                                                                | 96.2 ms: 1.04x faster                                          |
| scimark_sparse_mat_mult  | 5.62 ms                                                                | 5.45 ms: 1.03x faster                                          |
| thrift                   | 914 us                                                                 | 896 us: 1.02x faster                                           |
| telco                    | 8.73 ms                                                                | 8.56 ms: 1.02x faster                                          |
| html5lib                 | 70.4 ms                                                                | 69.0 ms: 1.02x faster                                          |
| scimark_fft              | 378 ms                                                                 | 371 ms: 1.02x faster                                           |
| create_gc_cycles         | 1.37 ms                                                                | 1.35 ms: 1.02x faster                                          |
| sphinx                   | 1.11 sec                                                               | 1.09 sec: 1.01x faster                                         |
| pprint_safe_repr         | 818 ms                                                                 | 808 ms: 1.01x faster                                           |
| meteor_contest           | 130 ms                                                                 | 129 ms: 1.01x faster                                           |
| generators               | 33.5 ms                                                                | 33.2 ms: 1.01x faster                                          |
| regex_v8                 | 23.5 ms                                                                | 23.3 ms: 1.01x faster                                          |
| scimark_monte_carlo      | 81.3 ms                                                                | 80.5 ms: 1.01x faster                                          |
| async_generators         | 376 ms                                                                 | 373 ms: 1.01x faster                                           |
| regex_compile            | 149 ms                                                                 | 148 ms: 1.01x faster                                           |
| pycparser                | 1.18 sec                                                               | 1.17 sec: 1.01x faster                                         |
| bench_thread_pool        | 3.31 ms                                                                | 3.29 ms: 1.01x faster                                          |
| deepcopy_memo            | 38.0 us                                                                | 37.8 us: 1.01x faster                                          |
| asyncio_websockets       | 518 ms                                                                 | 516 ms: 1.00x faster                                           |
| pprint_pformat           | 1.69 sec                                                               | 1.68 sec: 1.00x faster                                         |
| raytrace                 | 319 ms                                                                 | 318 ms: 1.00x faster                                           |
| python_startup_no_site   | 9.60 ms                                                                | 9.62 ms: 1.00x slower                                          |
| python_startup           | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                          |
| richards                 | 56.2 ms                                                                | 56.4 ms: 1.00x slower                                          |
| regex_effbot             | 2.81 ms                                                                | 2.82 ms: 1.00x slower                                          |
| 2to3                     | 301 ms                                                                 | 303 ms: 1.00x slower                                           |
| mako                     | 15.9 ms                                                                | 16.0 ms: 1.00x slower                                          |
| genshi_text              | 27.4 ms                                                                | 27.5 ms: 1.01x slower                                          |
| sqlglot_normalize        | 120 ms                                                                 | 120 ms: 1.01x slower                                           |
| tomli_loads              | 2.29 sec                                                               | 2.30 sec: 1.01x slower                                         |
| async_tree_memoization   | 349 ms                                                                 | 351 ms: 1.01x slower                                           |
| subparsers               | 25.5 ms                                                                | 25.7 ms: 1.01x slower                                          |
| sympy_integrate          | 23.9 ms                                                                | 24.1 ms: 1.01x slower                                          |
| genshi_xml               | 59.4 ms                                                                | 60.0 ms: 1.01x slower                                          |
| unpickle_pure_python     | 244 us                                                                 | 246 us: 1.01x slower                                           |
| typing_runtime_protocols | 200 us                                                                 | 201 us: 1.01x slower                                           |
| django_template          | 42.2 ms                                                                | 42.6 ms: 1.01x slower                                          |
| coroutines               | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                          |
| xml_etree_iterparse      | 87.0 ms                                                                | 87.9 ms: 1.01x slower                                          |
| async_tree_io            | 601 ms                                                                 | 608 ms: 1.01x slower                                           |
| json_loads               | 31.2 us                                                                | 31.6 us: 1.01x slower                                          |
| deltablue                | 4.60 ms                                                                | 4.65 ms: 1.01x slower                                          |
| pathlib                  | 18.7 ms                                                                | 18.9 ms: 1.01x slower                                          |
| sqlglot_parse            | 1.57 ms                                                                | 1.59 ms: 1.01x slower                                          |
| bpe_tokeniser            | 4.62 sec                                                               | 4.68 sec: 1.01x slower                                         |
| async_tree_io_tg         | 569 ms                                                                 | 577 ms: 1.01x slower                                           |
| pyflate                  | 484 ms                                                                 | 491 ms: 1.01x slower                                           |
| pickle_pure_python       | 364 us                                                                 | 369 us: 1.01x slower                                           |
| coverage                 | 97.8 ms                                                                | 99.3 ms: 1.02x slower                                          |
| sympy_expand             | 547 ms                                                                 | 556 ms: 1.02x slower                                           |
| sympy_str                | 332 ms                                                                 | 337 ms: 1.02x slower                                           |
| go                       | 134 ms                                                                 | 136 ms: 1.02x slower                                           |
| dulwich_log              | 81.5 ms                                                                | 82.8 ms: 1.02x slower                                          |
| hexiom                   | 7.29 ms                                                                | 7.43 ms: 1.02x slower                                          |
| crypto_pyaes             | 86.3 ms                                                                | 87.9 ms: 1.02x slower                                          |
| float                    | 75.2 ms                                                                | 76.7 ms: 1.02x slower                                          |
| sqlglot_transpile        | 1.88 ms                                                                | 1.92 ms: 1.02x slower                                          |
| fannkuch                 | 480 ms                                                                 | 490 ms: 1.02x slower                                           |
| xml_etree_parse          | 126 ms                                                                 | 130 ms: 1.03x slower                                           |
| logging_silent           | 109 ns                                                                 | 112 ns: 1.03x slower                                           |
| regex_dna                | 179 ms                                                                 | 185 ms: 1.03x slower                                           |
| deepcopy                 | 309 us                                                                 | 328 us: 1.06x slower                                           |
| deepcopy_reduce          | 3.20 us                                                                | 3.42 us: 1.07x slower                                          |
| gc_traversal             | 1.62 ms                                                                | 1.76 ms: 1.09x slower                                          |
| logging_simple           | 7.14 us                                                                | 7.96 us: 1.12x slower                                          |
| logging_format           | 8.09 us                                                                | 10.3 us: 1.27x slower                                          |
| sqlalchemy_imperative    | 23.5 ms                                                                | 30.3 ms: 1.29x slower                                          |
| sqlalchemy_declarative   | 156 ms                                                                 | 225 ms: 1.44x slower                                           |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                   |

Benchmark hidden because not significant (26): async_tree_none_tg, docutils, chaos, k_core, async_tree_none, json_dumps, scimark_lu, richards_super, xml_etree_process, nbody, spectral_norm, sqlite_synth, scimark_sor, sqlglot_optimize, xml_etree_generate, async_tree_cpu_io_mixed_tg, many_optionals, connected_components, sympy_sum, async_tree_memoization_tg, bench_mp_pool, async_tree_cpu_io_mixed, shortest_path, json, pylint, comprehensions

- Geometric mean (including insignificant results): 1.012x slower

# HPT report

- Reliability score: 95.30% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x