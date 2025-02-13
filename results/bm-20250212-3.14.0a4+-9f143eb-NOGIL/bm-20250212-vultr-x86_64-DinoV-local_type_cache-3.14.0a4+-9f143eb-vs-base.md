# Results vs. base

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 9f143eb
- commit date: 2025-02-12
- overall geometric mean: 1.004x faster
- HPT reliability: 97.47%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| docutils       | 2.84 sec                                                               | 2.80 sec: 1.01x faster                                            |
| html5lib       | 72.4 ms                                                                | 71.8 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io             | 612 ms                                                                 | 602 ms: 1.02x faster                                              |
| async_tree_none           | 291 ms                                                                 | 287 ms: 1.01x faster                                              |
| async_tree_memoization_tg | 322 ms                                                                 | 318 ms: 1.01x faster                                              |
| async_tree_memoization    | 355 ms                                                                 | 352 ms: 1.01x faster                                              |
| async_tree_io_tg          | 579 ms                                                                 | 574 ms: 1.01x faster                                              |
| asyncio_websockets        | 516 ms                                                                 | 514 ms: 1.00x faster                                              |
| coroutines                | 23.4 ms                                                                | 23.3 ms: 1.00x faster                                             |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (4): async_generators, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 76.6 ms                                                                | 75.3 ms: 1.02x faster                                             |
| pidigits       | 195 ms                                                                 | 199 ms: 1.02x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                      |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 178 ms: 1.02x faster                                              |
| regex_effbot   | 2.84 ms                                                                | 2.80 ms: 1.01x faster                                             |
| regex_v8       | 23.9 ms                                                                | 23.6 ms: 1.01x faster                                             |
| regex_compile  | 152 ms                                                                 | 151 ms: 1.01x faster                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 369 us                                                                 | 358 us: 1.03x faster                                              |
| json_dumps           | 12.8 ms                                                                | 12.7 ms: 1.01x faster                                             |
| unpickle_pure_python | 248 us                                                                 | 245 us: 1.01x faster                                              |
| json_loads           | 31.5 us                                                                | 31.2 us: 1.01x faster                                             |
| xml_etree_iterparse  | 87.7 ms                                                                | 87.0 ms: 1.01x faster                                             |
| tomli_loads          | 2.34 sec                                                               | 2.33 sec: 1.01x faster                                            |
| xml_etree_process    | 68.6 ms                                                                | 68.8 ms: 1.00x slower                                             |
| xml_etree_generate   | 96.7 ms                                                                | 97.6 ms: 1.01x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.4 ms                                                                | 15.5 ms: 1.01x slower                                             |
| python_startup_no_site | 9.62 ms                                                                | 9.69 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 42.3 ms                                                                | 41.7 ms: 1.01x faster                                             |
| genshi_xml      | 59.7 ms                                                                | 59.2 ms: 1.01x faster                                             |
| mako            | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| deltablue                 | 4.74 ms                                                                | 3.88 ms: 1.22x faster                                             |
| logging_silent            | 114 ns                                                                 | 108 ns: 1.05x faster                                              |
| mdp                       | 2.70 sec                                                               | 2.57 sec: 1.05x faster                                            |
| pickle_pure_python        | 369 us                                                                 | 358 us: 1.03x faster                                              |
| thrift                    | 908 us                                                                 | 884 us: 1.03x faster                                              |
| pprint_safe_repr          | 825 ms                                                                 | 804 ms: 1.03x faster                                              |
| regex_dna                 | 182 ms                                                                 | 178 ms: 1.02x faster                                              |
| typing_runtime_protocols  | 200 us                                                                 | 196 us: 1.02x faster                                              |
| deepcopy_memo             | 38.4 us                                                                | 37.7 us: 1.02x faster                                             |
| float                     | 76.6 ms                                                                | 75.3 ms: 1.02x faster                                             |
| pprint_pformat            | 1.70 sec                                                               | 1.68 sec: 1.02x faster                                            |
| raytrace                  | 330 ms                                                                 | 324 ms: 1.02x faster                                              |
| async_tree_io             | 612 ms                                                                 | 602 ms: 1.02x faster                                              |
| sqlite_synth              | 2.03 us                                                                | 2.00 us: 1.02x faster                                             |
| docutils                  | 2.84 sec                                                               | 2.80 sec: 1.01x faster                                            |
| richards_super            | 65.7 ms                                                                | 64.7 ms: 1.01x faster                                             |
| async_tree_none           | 291 ms                                                                 | 287 ms: 1.01x faster                                              |
| django_template           | 42.3 ms                                                                | 41.7 ms: 1.01x faster                                             |
| spectral_norm             | 108 ms                                                                 | 107 ms: 1.01x faster                                              |
| connected_components      | 499 ms                                                                 | 492 ms: 1.01x faster                                              |
| regex_effbot              | 2.84 ms                                                                | 2.80 ms: 1.01x faster                                             |
| logging_format            | 8.32 us                                                                | 8.22 us: 1.01x faster                                             |
| richards                  | 56.6 ms                                                                | 55.9 ms: 1.01x faster                                             |
| pathlib                   | 19.4 ms                                                                | 19.2 ms: 1.01x faster                                             |
| json_dumps                | 12.8 ms                                                                | 12.7 ms: 1.01x faster                                             |
| regex_v8                  | 23.9 ms                                                                | 23.6 ms: 1.01x faster                                             |
| unpickle_pure_python      | 248 us                                                                 | 245 us: 1.01x faster                                              |
| async_tree_memoization_tg | 322 ms                                                                 | 318 ms: 1.01x faster                                              |
| async_tree_memoization    | 355 ms                                                                 | 352 ms: 1.01x faster                                              |
| scimark_sor               | 134 ms                                                                 | 133 ms: 1.01x faster                                              |
| async_tree_io_tg          | 579 ms                                                                 | 574 ms: 1.01x faster                                              |
| json_loads                | 31.5 us                                                                | 31.2 us: 1.01x faster                                             |
| shortest_path             | 548 ms                                                                 | 543 ms: 1.01x faster                                              |
| genshi_xml                | 59.7 ms                                                                | 59.2 ms: 1.01x faster                                             |
| regex_compile             | 152 ms                                                                 | 151 ms: 1.01x faster                                              |
| comprehensions            | 20.0 us                                                                | 19.8 us: 1.01x faster                                             |
| xml_etree_iterparse       | 87.7 ms                                                                | 87.0 ms: 1.01x faster                                             |
| html5lib                  | 72.4 ms                                                                | 71.8 ms: 1.01x faster                                             |
| go                        | 140 ms                                                                 | 140 ms: 1.01x faster                                              |
| tomli_loads               | 2.34 sec                                                               | 2.33 sec: 1.01x faster                                            |
| deepcopy                  | 309 us                                                                 | 307 us: 1.01x faster                                              |
| pyflate                   | 509 ms                                                                 | 507 ms: 1.01x faster                                              |
| asyncio_websockets        | 516 ms                                                                 | 514 ms: 1.00x faster                                              |
| hexiom                    | 7.44 ms                                                                | 7.42 ms: 1.00x faster                                             |
| sqlalchemy_declarative    | 156 ms                                                                 | 156 ms: 1.00x faster                                              |
| coroutines                | 23.4 ms                                                                | 23.3 ms: 1.00x faster                                             |
| bpe_tokeniser             | 4.67 sec                                                               | 4.68 sec: 1.00x slower                                            |
| xml_etree_process         | 68.6 ms                                                                | 68.8 ms: 1.00x slower                                             |
| mako                      | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                             |
| bench_mp_pool             | 95.1 ms                                                                | 95.6 ms: 1.00x slower                                             |
| logging_simple            | 7.22 us                                                                | 7.26 us: 1.01x slower                                             |
| sympy_expand              | 552 ms                                                                 | 555 ms: 1.01x slower                                              |
| python_startup            | 15.4 ms                                                                | 15.5 ms: 1.01x slower                                             |
| many_optionals            | 1.18 ms                                                                | 1.19 ms: 1.01x slower                                             |
| python_startup_no_site    | 9.62 ms                                                                | 9.69 ms: 1.01x slower                                             |
| xml_etree_generate        | 96.7 ms                                                                | 97.6 ms: 1.01x slower                                             |
| sqlglot_parse             | 1.58 ms                                                                | 1.60 ms: 1.01x slower                                             |
| sympy_sum                 | 186 ms                                                                 | 188 ms: 1.01x slower                                              |
| pycparser                 | 1.18 sec                                                               | 1.20 sec: 1.01x slower                                            |
| sympy_integrate           | 24.1 ms                                                                | 24.5 ms: 1.01x slower                                             |
| nqueens                   | 95.4 ms                                                                | 96.8 ms: 1.01x slower                                             |
| chaos                     | 69.2 ms                                                                | 70.3 ms: 1.02x slower                                             |
| deepcopy_reduce           | 3.19 us                                                                | 3.25 us: 1.02x slower                                             |
| generators                | 31.4 ms                                                                | 32.1 ms: 1.02x slower                                             |
| pidigits                  | 195 ms                                                                 | 199 ms: 1.02x slower                                              |
| subparsers                | 25.4 ms                                                                | 25.9 ms: 1.02x slower                                             |
| gc_traversal              | 1.72 ms                                                                | 1.78 ms: 1.03x slower                                             |
| scimark_monte_carlo       | 82.3 ms                                                                | 85.1 ms: 1.03x slower                                             |
| scimark_sparse_mat_mult   | 5.65 ms                                                                | 5.84 ms: 1.03x slower                                             |
| crypto_pyaes              | 87.3 ms                                                                | 90.5 ms: 1.04x slower                                             |
| create_gc_cycles          | 1.37 ms                                                                | 1.42 ms: 1.04x slower                                             |
| scimark_fft               | 385 ms                                                                 | 399 ms: 1.04x slower                                              |
| scimark_lu                | 135 ms                                                                 | 142 ms: 1.05x slower                                              |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (23): sqlalchemy_imperative, sphinx, json, genshi_text, async_generators, sqlglot_optimize, k_core, async_tree_cpu_io_mixed_tg, xml_etree_parse, fannkuch, meteor_contest, bench_thread_pool, 2to3, nbody, async_tree_cpu_io_mixed, telco, sqlglot_normalize, sympy_str, dulwich_log, coverage, sqlglot_transpile, async_tree_none_tg, pylint

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 97.47% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x