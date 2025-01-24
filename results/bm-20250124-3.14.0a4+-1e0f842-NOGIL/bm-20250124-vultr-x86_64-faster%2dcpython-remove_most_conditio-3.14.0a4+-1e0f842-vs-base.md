# Results vs. base

- fork: faster-cpython
- ref: remove_most_conditio
- machine: linux-x86_64
- commit hash: 1e0f842
- commit date: 2025-01-24
- overall geometric mean: 1.010x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 303 ms: 1.01x faster                                                             |
| docutils       | 2.82 sec                                                               | 2.80 sec: 1.01x faster                                                           |
| html5lib       | 70.2 ms                                                                | 69.5 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 559 ms                                                                 | 504 ms: 1.11x faster                                                             |
| async_tree_cpu_io_mixed    | 589 ms                                                                 | 535 ms: 1.10x faster                                                             |
| async_tree_none_tg         | 257 ms                                                                 | 249 ms: 1.03x faster                                                             |
| async_tree_none            | 292 ms                                                                 | 285 ms: 1.02x faster                                                             |
| async_tree_memoization_tg  | 326 ms                                                                 | 319 ms: 1.02x faster                                                             |
| async_tree_memoization     | 360 ms                                                                 | 352 ms: 1.02x faster                                                             |
| async_tree_io_tg           | 587 ms                                                                 | 577 ms: 1.02x faster                                                             |
| coroutines                 | 23.9 ms                                                                | 23.6 ms: 1.01x faster                                                            |
| async_generators           | 371 ms                                                                 | 368 ms: 1.01x faster                                                             |
| asyncio_websockets         | 515 ms                                                                 | 517 ms: 1.00x slower                                                             |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 215 ms                                                                 | 190 ms: 1.13x faster                                                             |
| float          | 78.0 ms                                                                | 75.6 ms: 1.03x faster                                                            |
| nbody          | 134 ms                                                                 | 131 ms: 1.03x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                | 23.4 ms: 1.05x faster                                                            |
| regex_effbot   | 2.93 ms                                                                | 2.85 ms: 1.03x faster                                                            |
| regex_compile  | 151 ms                                                                 | 150 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_generate   | 98.4 ms                                                                | 96.7 ms: 1.02x faster                                                            |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.02x faster                                                             |
| xml_etree_iterparse  | 88.1 ms                                                                | 87.0 ms: 1.01x faster                                                            |
| xml_etree_process    | 69.8 ms                                                                | 69.4 ms: 1.01x faster                                                            |
| unpickle_pure_python | 248 us                                                                 | 247 us: 1.00x faster                                                             |
| json_dumps           | 13.0 ms                                                                | 13.0 ms: 1.00x faster                                                            |
| json_loads           | 30.2 us                                                                | 30.5 us: 1.01x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): pickle_pure_python, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                                | 15.2 ms: 1.00x faster                                                            |
| python_startup_no_site | 9.55 ms                                                                | 9.52 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 27.8 ms                                                                | 27.7 ms: 1.01x faster                                                            |
| mako            | 15.7 ms                                                                | 15.9 ms: 1.01x slower                                                            |
| django_template | 43.6 ms                                                                | 44.4 ms: 1.02x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits                   | 215 ms                                                                 | 190 ms: 1.13x faster                                                             |
| async_tree_cpu_io_mixed_tg | 559 ms                                                                 | 504 ms: 1.11x faster                                                             |
| async_tree_cpu_io_mixed    | 589 ms                                                                 | 535 ms: 1.10x faster                                                             |
| regex_v8                   | 24.4 ms                                                                | 23.4 ms: 1.05x faster                                                            |
| logging_silent             | 116 ns                                                                 | 112 ns: 1.04x faster                                                             |
| scimark_sparse_mat_mult    | 5.70 ms                                                                | 5.51 ms: 1.03x faster                                                            |
| async_tree_none_tg         | 257 ms                                                                 | 249 ms: 1.03x faster                                                             |
| float                      | 78.0 ms                                                                | 75.6 ms: 1.03x faster                                                            |
| richards                   | 56.9 ms                                                                | 55.2 ms: 1.03x faster                                                            |
| regex_effbot               | 2.93 ms                                                                | 2.85 ms: 1.03x faster                                                            |
| raytrace                   | 335 ms                                                                 | 325 ms: 1.03x faster                                                             |
| richards_super             | 65.5 ms                                                                | 63.7 ms: 1.03x faster                                                            |
| go                         | 140 ms                                                                 | 137 ms: 1.03x faster                                                             |
| nbody                      | 134 ms                                                                 | 131 ms: 1.03x faster                                                             |
| deepcopy_memo              | 39.0 us                                                                | 38.0 us: 1.03x faster                                                            |
| async_tree_none            | 292 ms                                                                 | 285 ms: 1.02x faster                                                             |
| hexiom                     | 7.40 ms                                                                | 7.22 ms: 1.02x faster                                                            |
| sqlglot_transpile          | 1.96 ms                                                                | 1.91 ms: 1.02x faster                                                            |
| scimark_fft                | 386 ms                                                                 | 377 ms: 1.02x faster                                                             |
| async_tree_memoization_tg  | 326 ms                                                                 | 319 ms: 1.02x faster                                                             |
| async_tree_memoization     | 360 ms                                                                 | 352 ms: 1.02x faster                                                             |
| sqlglot_parse              | 1.57 ms                                                                | 1.54 ms: 1.02x faster                                                            |
| create_gc_cycles           | 1.36 ms                                                                | 1.33 ms: 1.02x faster                                                            |
| spectral_norm              | 109 ms                                                                 | 107 ms: 1.02x faster                                                             |
| logging_format             | 8.71 us                                                                | 8.55 us: 1.02x faster                                                            |
| deltablue                  | 4.72 ms                                                                | 4.63 ms: 1.02x faster                                                            |
| xml_etree_generate         | 98.4 ms                                                                | 96.7 ms: 1.02x faster                                                            |
| async_tree_io_tg           | 587 ms                                                                 | 577 ms: 1.02x faster                                                             |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.02x faster                                                             |
| generators                 | 31.8 ms                                                                | 31.3 ms: 1.01x faster                                                            |
| xml_etree_iterparse        | 88.1 ms                                                                | 87.0 ms: 1.01x faster                                                            |
| coroutines                 | 23.9 ms                                                                | 23.6 ms: 1.01x faster                                                            |
| bpe_tokeniser              | 4.73 sec                                                               | 4.68 sec: 1.01x faster                                                           |
| scimark_monte_carlo        | 81.9 ms                                                                | 81.0 ms: 1.01x faster                                                            |
| pprint_pformat             | 1.70 sec                                                               | 1.68 sec: 1.01x faster                                                           |
| html5lib                   | 70.2 ms                                                                | 69.5 ms: 1.01x faster                                                            |
| async_generators           | 371 ms                                                                 | 368 ms: 1.01x faster                                                             |
| sqlite_synth               | 2.06 us                                                                | 2.04 us: 1.01x faster                                                            |
| docutils                   | 2.82 sec                                                               | 2.80 sec: 1.01x faster                                                           |
| chaos                      | 70.0 ms                                                                | 69.4 ms: 1.01x faster                                                            |
| telco                      | 8.56 ms                                                                | 8.49 ms: 1.01x faster                                                            |
| pycparser                  | 1.20 sec                                                               | 1.19 sec: 1.01x faster                                                           |
| regex_compile              | 151 ms                                                                 | 150 ms: 1.01x faster                                                             |
| sqlglot_normalize          | 121 ms                                                                 | 120 ms: 1.01x faster                                                             |
| 2to3                       | 305 ms                                                                 | 303 ms: 1.01x faster                                                             |
| xml_etree_process          | 69.8 ms                                                                | 69.4 ms: 1.01x faster                                                            |
| scimark_sor                | 132 ms                                                                 | 131 ms: 1.01x faster                                                             |
| genshi_text                | 27.8 ms                                                                | 27.7 ms: 1.01x faster                                                            |
| pprint_safe_repr           | 819 ms                                                                 | 814 ms: 1.01x faster                                                             |
| unpickle_pure_python       | 248 us                                                                 | 247 us: 1.00x faster                                                             |
| bench_mp_pool              | 94.6 ms                                                                | 94.2 ms: 1.00x faster                                                            |
| many_optionals             | 1.18 ms                                                                | 1.17 ms: 1.00x faster                                                            |
| json_dumps                 | 13.0 ms                                                                | 13.0 ms: 1.00x faster                                                            |
| python_startup             | 15.2 ms                                                                | 15.2 ms: 1.00x faster                                                            |
| python_startup_no_site     | 9.55 ms                                                                | 9.52 ms: 1.00x faster                                                            |
| sympy_sum                  | 185 ms                                                                 | 186 ms: 1.00x slower                                                             |
| crypto_pyaes               | 86.3 ms                                                                | 86.7 ms: 1.00x slower                                                            |
| asyncio_websockets         | 515 ms                                                                 | 517 ms: 1.00x slower                                                             |
| json_loads                 | 30.2 us                                                                | 30.5 us: 1.01x slower                                                            |
| comprehensions             | 20.6 us                                                                | 20.8 us: 1.01x slower                                                            |
| pyflate                    | 490 ms                                                                 | 495 ms: 1.01x slower                                                             |
| deepcopy_reduce            | 3.24 us                                                                | 3.27 us: 1.01x slower                                                            |
| fannkuch                   | 478 ms                                                                 | 484 ms: 1.01x slower                                                             |
| mako                       | 15.7 ms                                                                | 15.9 ms: 1.01x slower                                                            |
| django_template            | 43.6 ms                                                                | 44.4 ms: 1.02x slower                                                            |
| mdp                        | 2.60 sec                                                               | 2.65 sec: 1.02x slower                                                           |
| pathlib                    | 18.8 ms                                                                | 19.2 ms: 1.02x slower                                                            |
| gc_traversal               | 3.16 ms                                                                | 3.29 ms: 1.04x slower                                                            |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (28): async_tree_io, sphinx, json, pylint, genshi_xml, sqlglot_optimize, sympy_str, bench_thread_pool, pickle_pure_python, sympy_integrate, subparsers, typing_runtime_protocols, sympy_expand, sqlalchemy_declarative, k_core, coverage, nqueens, meteor_contest, scimark_lu, regex_dna, shortest_path, deepcopy, tomli_loads, dulwich_log, thrift, logging_simple, connected_components, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x