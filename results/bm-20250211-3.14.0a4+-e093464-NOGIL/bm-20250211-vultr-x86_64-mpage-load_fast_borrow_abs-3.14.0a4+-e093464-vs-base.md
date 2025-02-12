# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: e093464
- commit date: 2025-02-11
- overall geometric mean: 1.011x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 301 ms: 1.01x faster                                                  |
| html5lib       | 72.7 ms                                                                | 71.9 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators          | 381 ms                                                                 | 371 ms: 1.03x faster                                                  |
| async_tree_io_tg          | 576 ms                                                                 | 565 ms: 1.02x faster                                                  |
| async_tree_none           | 289 ms                                                                 | 286 ms: 1.01x faster                                                  |
| async_tree_none_tg        | 250 ms                                                                 | 247 ms: 1.01x faster                                                  |
| async_tree_memoization    | 355 ms                                                                 | 351 ms: 1.01x faster                                                  |
| async_tree_io             | 610 ms                                                                 | 604 ms: 1.01x faster                                                  |
| async_tree_memoization_tg | 320 ms                                                                 | 318 ms: 1.01x faster                                                  |
| coroutines                | 23.2 ms                                                                | 24.4 ms: 1.06x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 194 ms: 1.12x faster                                                  |
| float          | 76.2 ms                                                                | 71.8 ms: 1.06x faster                                                 |
| nbody          | 130 ms                                                                 | 124 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 187 ms                                                                 | 177 ms: 1.06x faster                                                  |
| regex_v8       | 24.4 ms                                                                | 23.4 ms: 1.04x faster                                                 |
| regex_compile  | 152 ms                                                                 | 150 ms: 1.01x faster                                                  |
| regex_effbot   | 2.84 ms                                                                | 2.84 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads         | 2.33 sec                                                               | 2.27 sec: 1.03x faster                                                |
| pickle_pure_python  | 368 us                                                                 | 364 us: 1.01x faster                                                  |
| xml_etree_generate  | 96.6 ms                                                                | 96.1 ms: 1.01x faster                                                 |
| xml_etree_iterparse | 88.1 ms                                                                | 88.8 ms: 1.01x slower                                                 |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (5): xml_etree_parse, unpickle_pure_python, json_dumps, xml_etree_process, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.3 ms: 1.00x faster                                                 |
| python_startup_no_site | 9.63 ms                                                                | 9.60 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 27.6 ms                                                                | 27.4 ms: 1.01x faster                                                 |
| mako            | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                 |
| django_template | 42.2 ms                                                                | 42.7 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4+-e41ec8e | bm-20250211-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a4+-e093464 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                  | 216 ms                                                                 | 194 ms: 1.12x faster                                                  |
| scimark_sparse_mat_mult   | 5.67 ms                                                                | 5.17 ms: 1.10x faster                                                 |
| scimark_fft               | 387 ms                                                                 | 360 ms: 1.08x faster                                                  |
| float                     | 76.2 ms                                                                | 71.8 ms: 1.06x faster                                                 |
| regex_dna                 | 187 ms                                                                 | 177 ms: 1.06x faster                                                  |
| nbody                     | 130 ms                                                                 | 124 ms: 1.05x faster                                                  |
| regex_v8                  | 24.4 ms                                                                | 23.4 ms: 1.04x faster                                                 |
| fannkuch                  | 493 ms                                                                 | 473 ms: 1.04x faster                                                  |
| raytrace                  | 330 ms                                                                 | 318 ms: 1.04x faster                                                  |
| scimark_monte_carlo       | 82.4 ms                                                                | 79.5 ms: 1.04x faster                                                 |
| scimark_lu                | 140 ms                                                                 | 135 ms: 1.03x faster                                                  |
| deepcopy_memo             | 37.9 us                                                                | 36.7 us: 1.03x faster                                                 |
| sqlglot_parse             | 1.58 ms                                                                | 1.54 ms: 1.03x faster                                                 |
| sqlglot_transpile         | 1.91 ms                                                                | 1.86 ms: 1.03x faster                                                 |
| tomli_loads               | 2.33 sec                                                               | 2.27 sec: 1.03x faster                                                |
| meteor_contest            | 132 ms                                                                 | 128 ms: 1.03x faster                                                  |
| async_generators          | 381 ms                                                                 | 371 ms: 1.03x faster                                                  |
| connected_components      | 497 ms                                                                 | 484 ms: 1.03x faster                                                  |
| crypto_pyaes              | 88.9 ms                                                                | 86.6 ms: 1.03x faster                                                 |
| telco                     | 8.49 ms                                                                | 8.28 ms: 1.03x faster                                                 |
| richards                  | 56.5 ms                                                                | 55.1 ms: 1.03x faster                                                 |
| many_optionals            | 1.18 ms                                                                | 1.15 ms: 1.02x faster                                                 |
| mdp                       | 2.69 sec                                                               | 2.63 sec: 1.02x faster                                                |
| chaos                     | 71.1 ms                                                                | 69.7 ms: 1.02x faster                                                 |
| thrift                    | 908 us                                                                 | 891 us: 1.02x faster                                                  |
| deepcopy                  | 309 us                                                                 | 303 us: 1.02x faster                                                  |
| richards_super            | 65.3 ms                                                                | 64.1 ms: 1.02x faster                                                 |
| async_tree_io_tg          | 576 ms                                                                 | 565 ms: 1.02x faster                                                  |
| logging_silent            | 113 ns                                                                 | 111 ns: 1.02x faster                                                  |
| logging_format            | 8.42 us                                                                | 8.29 us: 1.01x faster                                                 |
| shortest_path             | 547 ms                                                                 | 539 ms: 1.01x faster                                                  |
| create_gc_cycles          | 1.39 ms                                                                | 1.37 ms: 1.01x faster                                                 |
| regex_compile             | 152 ms                                                                 | 150 ms: 1.01x faster                                                  |
| deltablue                 | 4.70 ms                                                                | 4.64 ms: 1.01x faster                                                 |
| 2to3                      | 305 ms                                                                 | 301 ms: 1.01x faster                                                  |
| pprint_pformat            | 1.66 sec                                                               | 1.64 sec: 1.01x faster                                                |
| async_tree_none           | 289 ms                                                                 | 286 ms: 1.01x faster                                                  |
| scimark_sor               | 135 ms                                                                 | 133 ms: 1.01x faster                                                  |
| logging_simple            | 7.36 us                                                                | 7.27 us: 1.01x faster                                                 |
| async_tree_none_tg        | 250 ms                                                                 | 247 ms: 1.01x faster                                                  |
| async_tree_memoization    | 355 ms                                                                 | 351 ms: 1.01x faster                                                  |
| hexiom                    | 7.48 ms                                                                | 7.39 ms: 1.01x faster                                                 |
| pickle_pure_python        | 368 us                                                                 | 364 us: 1.01x faster                                                  |
| html5lib                  | 72.7 ms                                                                | 71.9 ms: 1.01x faster                                                 |
| nqueens                   | 97.4 ms                                                                | 96.4 ms: 1.01x faster                                                 |
| go                        | 138 ms                                                                 | 137 ms: 1.01x faster                                                  |
| gc_traversal              | 1.76 ms                                                                | 1.74 ms: 1.01x faster                                                 |
| async_tree_io             | 610 ms                                                                 | 604 ms: 1.01x faster                                                  |
| sqlite_synth              | 2.06 us                                                                | 2.04 us: 1.01x faster                                                 |
| sympy_str                 | 337 ms                                                                 | 335 ms: 1.01x faster                                                  |
| genshi_text               | 27.6 ms                                                                | 27.4 ms: 1.01x faster                                                 |
| async_tree_memoization_tg | 320 ms                                                                 | 318 ms: 1.01x faster                                                  |
| deepcopy_reduce           | 3.19 us                                                                | 3.17 us: 1.01x faster                                                 |
| mako                      | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                 |
| pprint_safe_repr          | 801 ms                                                                 | 797 ms: 1.01x faster                                                  |
| xml_etree_generate        | 96.6 ms                                                                | 96.1 ms: 1.01x faster                                                 |
| sympy_integrate           | 24.0 ms                                                                | 23.9 ms: 1.00x faster                                                 |
| bench_thread_pool         | 3.30 ms                                                                | 3.29 ms: 1.00x faster                                                 |
| bpe_tokeniser             | 4.68 sec                                                               | 4.66 sec: 1.00x faster                                                |
| python_startup            | 15.3 ms                                                                | 15.3 ms: 1.00x faster                                                 |
| python_startup_no_site    | 9.63 ms                                                                | 9.60 ms: 1.00x faster                                                 |
| regex_effbot              | 2.84 ms                                                                | 2.84 ms: 1.00x faster                                                 |
| comprehensions            | 19.9 us                                                                | 20.0 us: 1.01x slower                                                 |
| sympy_expand              | 549 ms                                                                 | 552 ms: 1.01x slower                                                  |
| subparsers                | 25.3 ms                                                                | 25.5 ms: 1.01x slower                                                 |
| sqlalchemy_declarative    | 157 ms                                                                 | 158 ms: 1.01x slower                                                  |
| xml_etree_iterparse       | 88.1 ms                                                                | 88.8 ms: 1.01x slower                                                 |
| dulwich_log               | 81.9 ms                                                                | 82.5 ms: 1.01x slower                                                 |
| pyflate                   | 492 ms                                                                 | 496 ms: 1.01x slower                                                  |
| spectral_norm             | 110 ms                                                                 | 111 ms: 1.01x slower                                                  |
| django_template           | 42.2 ms                                                                | 42.7 ms: 1.01x slower                                                 |
| pathlib                   | 18.6 ms                                                                | 18.8 ms: 1.01x slower                                                 |
| pycparser                 | 1.18 sec                                                               | 1.20 sec: 1.01x slower                                                |
| coverage                  | 96.5 ms                                                                | 99.0 ms: 1.03x slower                                                 |
| typing_runtime_protocols  | 198 us                                                                 | 203 us: 1.03x slower                                                  |
| coroutines                | 23.2 ms                                                                | 24.4 ms: 1.06x slower                                                 |
| generators                | 32.1 ms                                                                | 35.2 ms: 1.09x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (19): sqlalchemy_imperative, sqlglot_optimize, xml_etree_parse, k_core, docutils, bench_mp_pool, unpickle_pure_python, sphinx, async_tree_cpu_io_mixed, json_dumps, sqlglot_normalize, async_tree_cpu_io_mixed_tg, asyncio_websockets, json, genshi_xml, xml_etree_process, sympy_sum, json_loads, pylint

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x