# Results vs. base

- fork: faster-cpython
- ref: remove_most_conditio
- machine: linux-x86_64
- commit hash: 584015a
- commit date: 2025-01-23
- overall geometric mean: 1.006x faster
- HPT reliability: 99.90%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 304 ms: 1.00x faster                                                             |
| docutils       | 2.82 sec                                                               | 2.87 sec: 1.02x slower                                                           |
| sphinx         | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| coroutines                 | 23.9 ms                                                                | 22.9 ms: 1.04x faster                                                            |
| async_tree_none_tg         | 257 ms                                                                 | 250 ms: 1.03x faster                                                             |
| async_tree_memoization     | 360 ms                                                                 | 354 ms: 1.02x faster                                                             |
| async_tree_memoization_tg  | 326 ms                                                                 | 321 ms: 1.02x faster                                                             |
| async_tree_none            | 292 ms                                                                 | 289 ms: 1.01x faster                                                             |
| async_tree_cpu_io_mixed_tg | 559 ms                                                                 | 554 ms: 1.01x faster                                                             |
| async_tree_io_tg           | 587 ms                                                                 | 582 ms: 1.01x faster                                                             |
| async_tree_cpu_io_mixed    | 589 ms                                                                 | 584 ms: 1.01x faster                                                             |
| async_tree_io              | 619 ms                                                                 | 614 ms: 1.01x faster                                                             |
| async_generators           | 371 ms                                                                 | 372 ms: 1.00x slower                                                             |
| asyncio_websockets         | 515 ms                                                                 | 517 ms: 1.00x slower                                                             |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.0 ms                                                                | 74.7 ms: 1.04x faster                                                            |
| nbody          | 134 ms                                                                 | 131 ms: 1.02x faster                                                             |
| pidigits       | 215 ms                                                                 | 215 ms: 1.00x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 187 ms                                                                 | 182 ms: 1.03x faster                                                             |
| regex_v8       | 24.4 ms                                                                | 23.9 ms: 1.02x faster                                                            |
| regex_effbot   | 2.93 ms                                                                | 2.89 ms: 1.01x faster                                                            |
| regex_compile  | 151 ms                                                                 | 149 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_generate   | 98.4 ms                                                                | 96.6 ms: 1.02x faster                                                            |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.02x faster                                                             |
| unpickle_pure_python | 248 us                                                                 | 244 us: 1.02x faster                                                             |
| xml_etree_iterparse  | 88.1 ms                                                                | 86.8 ms: 1.01x faster                                                            |
| pickle_pure_python   | 374 us                                                                 | 370 us: 1.01x faster                                                             |
| xml_etree_process    | 69.8 ms                                                                | 69.0 ms: 1.01x faster                                                            |
| json_dumps           | 13.0 ms                                                                | 12.9 ms: 1.01x faster                                                            |
| tomli_loads          | 2.34 sec                                                               | 2.32 sec: 1.01x faster                                                           |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 9.55 ms                                                                | 9.53 ms: 1.00x faster                                                            |
| python_startup         | 15.2 ms                                                                | 15.2 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 27.8 ms                                                                | 27.5 ms: 1.01x faster                                                            |
| genshi_xml      | 60.0 ms                                                                | 59.2 ms: 1.01x faster                                                            |
| mako            | 15.7 ms                                                                | 15.6 ms: 1.00x faster                                                            |
| django_template | 43.6 ms                                                                | 44.3 ms: 1.02x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20250123-vultr-x86_64-python-a10f99375e7912df863c-3.14.0a4+-a10f993 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| logging_silent             | 116 ns                                                                 | 111 ns: 1.05x faster                                                             |
| go                         | 140 ms                                                                 | 134 ms: 1.05x faster                                                             |
| float                      | 78.0 ms                                                                | 74.7 ms: 1.04x faster                                                            |
| coroutines                 | 23.9 ms                                                                | 22.9 ms: 1.04x faster                                                            |
| raytrace                   | 335 ms                                                                 | 321 ms: 1.04x faster                                                             |
| logging_format             | 8.71 us                                                                | 8.36 us: 1.04x faster                                                            |
| hexiom                     | 7.40 ms                                                                | 7.14 ms: 1.04x faster                                                            |
| deltablue                  | 4.72 ms                                                                | 4.56 ms: 1.03x faster                                                            |
| chaos                      | 70.0 ms                                                                | 67.8 ms: 1.03x faster                                                            |
| regex_dna                  | 187 ms                                                                 | 182 ms: 1.03x faster                                                             |
| async_tree_none_tg         | 257 ms                                                                 | 250 ms: 1.03x faster                                                             |
| scimark_monte_carlo        | 81.9 ms                                                                | 79.8 ms: 1.03x faster                                                            |
| logging_simple             | 7.45 us                                                                | 7.26 us: 1.03x faster                                                            |
| nbody                      | 134 ms                                                                 | 131 ms: 1.02x faster                                                             |
| create_gc_cycles           | 1.36 ms                                                                | 1.33 ms: 1.02x faster                                                            |
| regex_v8                   | 24.4 ms                                                                | 23.9 ms: 1.02x faster                                                            |
| generators                 | 31.8 ms                                                                | 31.1 ms: 1.02x faster                                                            |
| xml_etree_generate         | 98.4 ms                                                                | 96.6 ms: 1.02x faster                                                            |
| async_tree_memoization     | 360 ms                                                                 | 354 ms: 1.02x faster                                                             |
| scimark_sparse_mat_mult    | 5.70 ms                                                                | 5.60 ms: 1.02x faster                                                            |
| async_tree_memoization_tg  | 326 ms                                                                 | 321 ms: 1.02x faster                                                             |
| sqlglot_transpile          | 1.96 ms                                                                | 1.93 ms: 1.02x faster                                                            |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.02x faster                                                             |
| unpickle_pure_python       | 248 us                                                                 | 244 us: 1.02x faster                                                             |
| sqlglot_parse              | 1.57 ms                                                                | 1.55 ms: 1.01x faster                                                            |
| deepcopy_reduce            | 3.24 us                                                                | 3.19 us: 1.01x faster                                                            |
| regex_effbot               | 2.93 ms                                                                | 2.89 ms: 1.01x faster                                                            |
| xml_etree_iterparse        | 88.1 ms                                                                | 86.8 ms: 1.01x faster                                                            |
| deepcopy_memo              | 39.0 us                                                                | 38.4 us: 1.01x faster                                                            |
| genshi_text                | 27.8 ms                                                                | 27.5 ms: 1.01x faster                                                            |
| pickle_pure_python         | 374 us                                                                 | 370 us: 1.01x faster                                                             |
| genshi_xml                 | 60.0 ms                                                                | 59.2 ms: 1.01x faster                                                            |
| xml_etree_process          | 69.8 ms                                                                | 69.0 ms: 1.01x faster                                                            |
| json_dumps                 | 13.0 ms                                                                | 12.9 ms: 1.01x faster                                                            |
| regex_compile              | 151 ms                                                                 | 149 ms: 1.01x faster                                                             |
| async_tree_none            | 292 ms                                                                 | 289 ms: 1.01x faster                                                             |
| telco                      | 8.56 ms                                                                | 8.47 ms: 1.01x faster                                                            |
| pycparser                  | 1.20 sec                                                               | 1.18 sec: 1.01x faster                                                           |
| thrift                     | 925 us                                                                 | 916 us: 1.01x faster                                                             |
| meteor_contest             | 131 ms                                                                 | 130 ms: 1.01x faster                                                             |
| subparsers                 | 25.5 ms                                                                | 25.3 ms: 1.01x faster                                                            |
| async_tree_cpu_io_mixed_tg | 559 ms                                                                 | 554 ms: 1.01x faster                                                             |
| pathlib                    | 18.8 ms                                                                | 18.6 ms: 1.01x faster                                                            |
| async_tree_io_tg           | 587 ms                                                                 | 582 ms: 1.01x faster                                                             |
| async_tree_cpu_io_mixed    | 589 ms                                                                 | 584 ms: 1.01x faster                                                             |
| tomli_loads                | 2.34 sec                                                               | 2.32 sec: 1.01x faster                                                           |
| comprehensions             | 20.6 us                                                                | 20.4 us: 1.01x faster                                                            |
| async_tree_io              | 619 ms                                                                 | 614 ms: 1.01x faster                                                             |
| dulwich_log                | 81.7 ms                                                                | 81.2 ms: 1.01x faster                                                            |
| deepcopy                   | 314 us                                                                 | 312 us: 1.01x faster                                                             |
| bench_thread_pool          | 3.32 ms                                                                | 3.30 ms: 1.01x faster                                                            |
| mdp                        | 2.60 sec                                                               | 2.58 sec: 1.01x faster                                                           |
| pyflate                    | 490 ms                                                                 | 487 ms: 1.01x faster                                                             |
| fannkuch                   | 478 ms                                                                 | 476 ms: 1.00x faster                                                             |
| bpe_tokeniser              | 4.73 sec                                                               | 4.71 sec: 1.00x faster                                                           |
| bench_mp_pool              | 94.6 ms                                                                | 94.2 ms: 1.00x faster                                                            |
| mako                       | 15.7 ms                                                                | 15.6 ms: 1.00x faster                                                            |
| k_core                     | 2.31 sec                                                               | 2.31 sec: 1.00x faster                                                           |
| python_startup_no_site     | 9.55 ms                                                                | 9.53 ms: 1.00x faster                                                            |
| 2to3                       | 305 ms                                                                 | 304 ms: 1.00x faster                                                             |
| python_startup             | 15.2 ms                                                                | 15.2 ms: 1.00x faster                                                            |
| pidigits                   | 215 ms                                                                 | 215 ms: 1.00x faster                                                             |
| async_generators           | 371 ms                                                                 | 372 ms: 1.00x slower                                                             |
| asyncio_websockets         | 515 ms                                                                 | 517 ms: 1.00x slower                                                             |
| crypto_pyaes               | 86.3 ms                                                                | 86.6 ms: 1.00x slower                                                            |
| many_optionals             | 1.18 ms                                                                | 1.18 ms: 1.00x slower                                                            |
| pprint_pformat             | 1.70 sec                                                               | 1.71 sec: 1.00x slower                                                           |
| sympy_integrate            | 24.2 ms                                                                | 24.3 ms: 1.01x slower                                                            |
| sympy_sum                  | 185 ms                                                                 | 186 ms: 1.01x slower                                                             |
| sqlglot_optimize           | 61.0 ms                                                                | 61.3 ms: 1.01x slower                                                            |
| coverage                   | 98.2 ms                                                                | 98.9 ms: 1.01x slower                                                            |
| typing_runtime_protocols   | 202 us                                                                 | 203 us: 1.01x slower                                                             |
| scimark_lu                 | 136 ms                                                                 | 138 ms: 1.01x slower                                                             |
| pprint_safe_repr           | 819 ms                                                                 | 826 ms: 1.01x slower                                                             |
| sqlglot_normalize          | 121 ms                                                                 | 122 ms: 1.01x slower                                                             |
| spectral_norm              | 109 ms                                                                 | 111 ms: 1.01x slower                                                             |
| django_template            | 43.6 ms                                                                | 44.3 ms: 1.02x slower                                                            |
| sphinx                     | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                           |
| docutils                   | 2.82 sec                                                               | 2.87 sec: 1.02x slower                                                           |
| gc_traversal               | 3.16 ms                                                                | 3.25 ms: 1.03x slower                                                            |
| richards                   | 56.9 ms                                                                | 62.2 ms: 1.09x slower                                                            |
| richards_super             | 65.5 ms                                                                | 71.6 ms: 1.09x slower                                                            |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (14): sqlite_synth, json, scimark_fft, sympy_str, shortest_path, nqueens, sqlalchemy_declarative, html5lib, connected_components, sympy_expand, scimark_sor, json_loads, sqlalchemy_imperative, pylint

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 99.90% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x