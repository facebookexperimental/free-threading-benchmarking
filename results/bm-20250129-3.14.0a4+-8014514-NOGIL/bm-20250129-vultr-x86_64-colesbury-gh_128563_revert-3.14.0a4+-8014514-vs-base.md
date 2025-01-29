# Results vs. base

- fork: colesbury
- ref: gh_128563_revert
- machine: linux-x86_64
- commit hash: 8014514
- commit date: 2025-01-29
- overall geometric mean: 1.002x faster
- HPT reliability: 53.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-99ed3025fe8fa9079b4c-3.14.0a4+-99ed302 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 302 ms: 1.00x slower                                                  |
| html5lib       | 69.4 ms                                                                | 70.9 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250129-vultr-x86_64-python-99ed3025fe8fa9079b4c-3.14.0a4+-99ed302 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 553 ms                                                                 | 536 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed_tg | 521 ms                                                                 | 507 ms: 1.03x faster                                                  |
| coroutines                 | 23.7 ms                                                                | 23.0 ms: 1.03x faster                                                 |
| async_generators           | 373 ms                                                                 | 377 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, asyncio_websockets, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250129-vultr-x86_64-python-99ed3025fe8fa9079b4c-3.14.0a4+-99ed302 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 205 ms                                                                 | 190 ms: 1.08x faster                                                  |
| float          | 77.4 ms                                                                | 76.6 ms: 1.01x faster                                                 |
| nbody          | 130 ms                                                                 | 133 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250129-vultr-x86_64-python-99ed3025fe8fa9079b4c-3.14.0a4+-99ed302 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 177 ms: 1.03x faster                                                  |
| regex_v8       | 23.9 ms                                                                | 23.7 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250129-vultr-x86_64-python-99ed3025fe8fa9079b4c-3.14.0a4+-99ed302 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python  | 371 us                                                                 | 365 us: 1.02x faster                                                  |
| xml_etree_process   | 69.0 ms                                                                | 68.3 ms: 1.01x faster                                                 |
| xml_etree_generate  | 96.3 ms                                                                | 95.9 ms: 1.00x faster                                                 |
| xml_etree_iterparse | 87.3 ms                                                                | 87.6 ms: 1.00x slower                                                 |
| json_loads          | 30.9 us                                                                | 31.2 us: 1.01x slower                                                 |
| tomli_loads         | 2.27 sec                                                               | 2.32 sec: 1.02x slower                                                |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): unpickle_pure_python, xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250129-vultr-x86_64-python-99ed3025fe8fa9079b4c-3.14.0a4+-99ed302 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.59 ms                                                                | 9.62 ms: 1.00x slower                                                 |
| python_startup         | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250129-vultr-x86_64-python-99ed3025fe8fa9079b4c-3.14.0a4+-99ed302 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 27.8 ms                                                                | 27.4 ms: 1.01x faster                                                 |
| genshi_xml      | 59.3 ms                                                                | 59.8 ms: 1.01x slower                                                 |
| django_template | 41.9 ms                                                                | 42.4 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20250129-vultr-x86_64-python-99ed3025fe8fa9079b4c-3.14.0a4+-99ed302 | bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4+-8014514 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 205 ms                                                                 | 190 ms: 1.08x faster                                                  |
| generators                 | 33.3 ms                                                                | 31.5 ms: 1.06x faster                                                 |
| mdp                        | 2.75 sec                                                               | 2.65 sec: 1.04x faster                                                |
| richards                   | 57.8 ms                                                                | 55.9 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 553 ms                                                                 | 536 ms: 1.03x faster                                                  |
| regex_dna                  | 182 ms                                                                 | 177 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed_tg | 521 ms                                                                 | 507 ms: 1.03x faster                                                  |
| coroutines                 | 23.7 ms                                                                | 23.0 ms: 1.03x faster                                                 |
| shortest_path              | 545 ms                                                                 | 534 ms: 1.02x faster                                                  |
| logging_silent             | 113 ns                                                                 | 111 ns: 1.02x faster                                                  |
| pickle_pure_python         | 371 us                                                                 | 365 us: 1.02x faster                                                  |
| sqlite_synth               | 2.08 us                                                                | 2.05 us: 1.02x faster                                                 |
| typing_runtime_protocols   | 198 us                                                                 | 195 us: 1.02x faster                                                  |
| fannkuch                   | 491 ms                                                                 | 483 ms: 1.02x faster                                                  |
| richards_super             | 66.5 ms                                                                | 65.5 ms: 1.02x faster                                                 |
| scimark_sor                | 133 ms                                                                 | 131 ms: 1.02x faster                                                  |
| sqlglot_transpile          | 1.91 ms                                                                | 1.88 ms: 1.02x faster                                                 |
| sqlglot_parse              | 1.58 ms                                                                | 1.56 ms: 1.02x faster                                                 |
| pycparser                  | 1.18 sec                                                               | 1.17 sec: 1.01x faster                                                |
| comprehensions             | 19.9 us                                                                | 19.7 us: 1.01x faster                                                 |
| xml_etree_process          | 69.0 ms                                                                | 68.3 ms: 1.01x faster                                                 |
| genshi_text                | 27.8 ms                                                                | 27.4 ms: 1.01x faster                                                 |
| connected_components       | 491 ms                                                                 | 486 ms: 1.01x faster                                                  |
| float                      | 77.4 ms                                                                | 76.6 ms: 1.01x faster                                                 |
| logging_simple             | 7.32 us                                                                | 7.26 us: 1.01x faster                                                 |
| regex_v8                   | 23.9 ms                                                                | 23.7 ms: 1.01x faster                                                 |
| json                       | 5.40 ms                                                                | 5.36 ms: 1.01x faster                                                 |
| scimark_monte_carlo        | 81.7 ms                                                                | 81.1 ms: 1.01x faster                                                 |
| deltablue                  | 4.62 ms                                                                | 4.59 ms: 1.01x faster                                                 |
| deepcopy_memo              | 37.7 us                                                                | 37.5 us: 1.00x faster                                                 |
| dulwich_log                | 82.1 ms                                                                | 81.7 ms: 1.00x faster                                                 |
| many_optionals             | 1.17 ms                                                                | 1.17 ms: 1.00x faster                                                 |
| hexiom                     | 7.30 ms                                                                | 7.27 ms: 1.00x faster                                                 |
| nqueens                    | 95.7 ms                                                                | 95.3 ms: 1.00x faster                                                 |
| deepcopy                   | 308 us                                                                 | 307 us: 1.00x faster                                                  |
| xml_etree_generate         | 96.3 ms                                                                | 95.9 ms: 1.00x faster                                                 |
| go                         | 137 ms                                                                 | 137 ms: 1.00x slower                                                  |
| 2to3                       | 301 ms                                                                 | 302 ms: 1.00x slower                                                  |
| crypto_pyaes               | 88.2 ms                                                                | 88.4 ms: 1.00x slower                                                 |
| python_startup_no_site     | 9.59 ms                                                                | 9.62 ms: 1.00x slower                                                 |
| bpe_tokeniser              | 4.60 sec                                                               | 4.62 sec: 1.00x slower                                                |
| python_startup             | 15.3 ms                                                                | 15.3 ms: 1.00x slower                                                 |
| sqlglot_normalize          | 119 ms                                                                 | 120 ms: 1.00x slower                                                  |
| xml_etree_iterparse        | 87.3 ms                                                                | 87.6 ms: 1.00x slower                                                 |
| sympy_expand               | 540 ms                                                                 | 544 ms: 1.01x slower                                                  |
| raytrace                   | 326 ms                                                                 | 328 ms: 1.01x slower                                                  |
| bench_thread_pool          | 3.30 ms                                                                | 3.32 ms: 1.01x slower                                                 |
| subparsers                 | 25.6 ms                                                                | 25.8 ms: 1.01x slower                                                 |
| genshi_xml                 | 59.3 ms                                                                | 59.8 ms: 1.01x slower                                                 |
| json_loads                 | 30.9 us                                                                | 31.2 us: 1.01x slower                                                 |
| spectral_norm              | 109 ms                                                                 | 110 ms: 1.01x slower                                                  |
| thrift                     | 895 us                                                                 | 904 us: 1.01x slower                                                  |
| pprint_safe_repr           | 798 ms                                                                 | 807 ms: 1.01x slower                                                  |
| async_generators           | 373 ms                                                                 | 377 ms: 1.01x slower                                                  |
| pprint_pformat             | 1.65 sec                                                               | 1.67 sec: 1.01x slower                                                |
| django_template            | 41.9 ms                                                                | 42.4 ms: 1.01x slower                                                 |
| chaos                      | 68.7 ms                                                                | 69.8 ms: 1.02x slower                                                 |
| nbody                      | 130 ms                                                                 | 133 ms: 1.02x slower                                                  |
| html5lib                   | 69.4 ms                                                                | 70.9 ms: 1.02x slower                                                 |
| scimark_lu                 | 132 ms                                                                 | 135 ms: 1.02x slower                                                  |
| tomli_loads                | 2.27 sec                                                               | 2.32 sec: 1.02x slower                                                |
| scimark_fft                | 375 ms                                                                 | 386 ms: 1.03x slower                                                  |
| telco                      | 8.55 ms                                                                | 8.94 ms: 1.05x slower                                                 |
| gc_traversal               | 1.64 ms                                                                | 1.75 ms: 1.07x slower                                                 |
| scimark_sparse_mat_mult    | 5.31 ms                                                                | 5.72 ms: 1.08x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (31): pylint, async_tree_memoization, async_tree_memoization_tg, async_tree_none, meteor_contest, sqlalchemy_imperative, coverage, async_tree_none_tg, pyflate, asyncio_websockets, bench_mp_pool, regex_compile, deepcopy_reduce, sqlglot_optimize, sqlalchemy_declarative, pathlib, sympy_integrate, sympy_str, sphinx, unpickle_pure_python, mako, k_core, xml_etree_parse, docutils, json_dumps, sympy_sum, logging_format, async_tree_io, async_tree_io_tg, regex_effbot, create_gc_cycles

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 53.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x