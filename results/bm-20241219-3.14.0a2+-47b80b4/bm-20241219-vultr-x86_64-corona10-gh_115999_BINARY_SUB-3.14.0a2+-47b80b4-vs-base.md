# Results vs. base

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 47b80b4
- commit date: 2024-12-19
- overall geometric mean: 1.003x slower
- HPT reliability: 53.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization     | 345 ms                                                                 | 342 ms: 1.01x faster                                                     |
| async_generators           | 363 ms                                                                 | 360 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 502 ms: 1.00x slower                                                     |
| coroutines                 | 22.1 ms                                                                | 22.5 ms: 1.02x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (7): async_tree_none, async_tree_none_tg, async_tree_memoization_tg, asyncio_websockets, async_tree_io, async_tree_io_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.2 ms                                                                | 79.3 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                                 | 176 ms: 1.02x faster                                                     |
| regex_effbot   | 2.76 ms                                                                | 2.72 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 321 us                                                                 | 316 us: 1.01x faster                                                     |
| xml_etree_parse      | 127 ms                                                                 | 127 ms: 1.00x slower                                                     |
| xml_etree_iterparse  | 90.5 ms                                                                | 91.0 ms: 1.01x slower                                                    |
| unpickle_pure_python | 215 us                                                                 | 219 us: 1.02x slower                                                     |
| json_loads           | 25.0 us                                                                | 25.9 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (4): tomli_loads, xml_etree_generate, xml_etree_process, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| python_startup_no_site | 7.46 ms                                                                | 7.49 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 11.7 ms                                                                | 11.8 ms: 1.01x slower                                                    |
| genshi_text    | 22.0 ms                                                                | 22.2 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna                  | 180 ms                                                                 | 176 ms: 1.02x faster                                                     |
| crypto_pyaes               | 68.7 ms                                                                | 67.4 ms: 1.02x faster                                                    |
| meteor_contest             | 101 ms                                                                 | 99.3 ms: 1.02x faster                                                    |
| pycparser                  | 1.13 sec                                                               | 1.12 sec: 1.02x faster                                                   |
| scimark_monte_carlo        | 66.4 ms                                                                | 65.4 ms: 1.02x faster                                                    |
| regex_effbot               | 2.76 ms                                                                | 2.72 ms: 1.02x faster                                                    |
| deepcopy_memo              | 30.6 us                                                                | 30.2 us: 1.01x faster                                                    |
| pickle_pure_python         | 321 us                                                                 | 316 us: 1.01x faster                                                     |
| generators                 | 29.2 ms                                                                | 28.9 ms: 1.01x faster                                                    |
| async_tree_memoization     | 345 ms                                                                 | 342 ms: 1.01x faster                                                     |
| float                      | 80.2 ms                                                                | 79.3 ms: 1.01x faster                                                    |
| sympy_sum                  | 155 ms                                                                 | 153 ms: 1.01x faster                                                     |
| sympy_integrate            | 20.1 ms                                                                | 19.9 ms: 1.01x faster                                                    |
| scimark_lu                 | 111 ms                                                                 | 110 ms: 1.01x faster                                                     |
| async_generators           | 363 ms                                                                 | 360 ms: 1.01x faster                                                     |
| dulwich_log                | 76.4 ms                                                                | 76.0 ms: 1.00x faster                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 1.03 ms: 1.00x faster                                                    |
| sqlglot_normalize          | 108 ms                                                                 | 108 ms: 1.00x faster                                                     |
| deltablue                  | 3.24 ms                                                                | 3.23 ms: 1.00x faster                                                    |
| sqlglot_optimize           | 53.9 ms                                                                | 53.8 ms: 1.00x faster                                                    |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| python_startup_no_site     | 7.46 ms                                                                | 7.49 ms: 1.00x slower                                                    |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 502 ms: 1.00x slower                                                     |
| xml_etree_parse            | 127 ms                                                                 | 127 ms: 1.00x slower                                                     |
| xml_etree_iterparse        | 90.5 ms                                                                | 91.0 ms: 1.01x slower                                                    |
| connected_components       | 399 ms                                                                 | 401 ms: 1.01x slower                                                     |
| many_optionals             | 1.03 ms                                                                | 1.04 ms: 1.01x slower                                                    |
| mako                       | 11.7 ms                                                                | 11.8 ms: 1.01x slower                                                    |
| hexiom                     | 5.93 ms                                                                | 5.98 ms: 1.01x slower                                                    |
| genshi_text                | 22.0 ms                                                                | 22.2 ms: 1.01x slower                                                    |
| chaos                      | 59.2 ms                                                                | 59.7 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 158 us                                                                 | 159 us: 1.01x slower                                                     |
| thrift                     | 736 us                                                                 | 744 us: 1.01x slower                                                     |
| spectral_norm              | 110 ms                                                                 | 112 ms: 1.01x slower                                                     |
| pyflate                    | 447 ms                                                                 | 453 ms: 1.01x slower                                                     |
| richards                   | 45.8 ms                                                                | 46.5 ms: 1.01x slower                                                    |
| richards_super             | 52.1 ms                                                                | 52.9 ms: 1.02x slower                                                    |
| scimark_fft                | 338 ms                                                                 | 343 ms: 1.02x slower                                                     |
| mdp                        | 2.49 sec                                                               | 2.53 sec: 1.02x slower                                                   |
| json                       | 4.59 ms                                                                | 4.67 ms: 1.02x slower                                                    |
| coroutines                 | 22.1 ms                                                                | 22.5 ms: 1.02x slower                                                    |
| unpickle_pure_python       | 215 us                                                                 | 219 us: 1.02x slower                                                     |
| logging_format             | 6.87 us                                                                | 7.03 us: 1.02x slower                                                    |
| logging_simple             | 6.14 us                                                                | 6.32 us: 1.03x slower                                                    |
| json_loads                 | 25.0 us                                                                | 25.9 us: 1.03x slower                                                    |
| scimark_sparse_mat_mult    | 4.51 ms                                                                | 4.67 ms: 1.04x slower                                                    |
| fannkuch                   | 371 ms                                                                 | 388 ms: 1.05x slower                                                     |
| gc_traversal               | 4.04 ms                                                                | 4.65 ms: 1.15x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (47): nbody, async_tree_none, sqlalchemy_imperative, pylint, pprint_safe_repr, tomli_loads, django_template, raytrace, sympy_str, regex_compile, subparsers, logging_silent, telco, async_tree_none_tg, sympy_expand, 2to3, sqlalchemy_declarative, bpe_tokeniser, deepcopy, create_gc_cycles, deepcopy_reduce, sphinx, pathlib, sqlglot_transpile, async_tree_memoization_tg, xml_etree_generate, asyncio_websockets, docutils, pidigits, sqlglot_parse, shortest_path, xml_etree_process, scimark_sor, json_dumps, pprint_pformat, sqlite_synth, genshi_xml, bench_mp_pool, nqueens, regex_v8, async_tree_io, async_tree_io_tg, k_core, go, comprehensions, coverage, async_tree_cpu_io_mixed

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 53.78% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x