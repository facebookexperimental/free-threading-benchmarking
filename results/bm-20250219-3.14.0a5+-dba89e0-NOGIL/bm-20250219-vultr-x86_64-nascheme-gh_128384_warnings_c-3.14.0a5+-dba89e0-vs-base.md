# Results vs. base

- fork: nascheme
- ref: gh_128384_warnings_c
- machine: linux-x86_64
- commit hash: dba89e0
- commit date: 2025-02-19
- overall geometric mean: 1.002x slower
- HPT reliability: 94.57%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5+-a7427f2 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 307 ms: 1.01x slower                                                     |
| html5lib       | 70.8 ms                                                                | 71.3 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5+-a7427f2 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 260 ms                                                                 | 251 ms: 1.04x faster                                                     |
| async_generators           | 372 ms                                                                 | 375 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed    | 535 ms                                                                 | 540 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 508 ms: 1.01x slower                                                     |
| coroutines                 | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                    |
| async_tree_none            | 288 ms                                                                 | 292 ms: 1.01x slower                                                     |
| async_tree_io_tg           | 577 ms                                                                 | 593 ms: 1.03x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (4): async_tree_memoization_tg, asyncio_websockets, async_tree_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5+-a7427f2 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 76.6 ms                                                                | 75.5 ms: 1.01x faster                                                    |
| nbody          | 133 ms                                                                 | 132 ms: 1.01x faster                                                     |
| pidigits       | 193 ms                                                                 | 200 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5+-a7427f2 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                | 2.75 ms: 1.03x faster                                                    |
| regex_dna      | 180 ms                                                                 | 181 ms: 1.00x slower                                                     |
| regex_v8       | 23.4 ms                                                                | 23.8 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5+-a7427f2 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 366 us                                                                 | 365 us: 1.00x faster                                                     |
| xml_etree_generate   | 96.3 ms                                                                | 96.7 ms: 1.00x slower                                                    |
| xml_etree_process    | 68.5 ms                                                                | 69.1 ms: 1.01x slower                                                    |
| json_loads           | 31.3 us                                                                | 31.6 us: 1.01x slower                                                    |
| unpickle_pure_python | 247 us                                                                 | 250 us: 1.01x slower                                                     |
| tomli_loads          | 2.32 sec                                                               | 2.34 sec: 1.01x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (3): json_dumps, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5+-a7427f2 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 9.64 ms                                                                | 9.62 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5+-a7427f2 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 15.7 ms                                                                | 15.5 ms: 1.01x faster                                                    |
| django_template | 42.2 ms                                                                | 42.0 ms: 1.00x faster                                                    |
| genshi_text     | 27.9 ms                                                                | 28.0 ms: 1.00x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250211-vultr-x86_64-python-a7427f2db937adb4c787-3.14.0a5+-a7427f2 | bm-20250219-vultr-x86_64-nascheme-gh_128384_warnings_c-3.14.0a5+-dba89e0 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| scimark_sparse_mat_mult    | 5.71 ms                                                                | 5.47 ms: 1.05x faster                                                    |
| async_tree_none_tg         | 260 ms                                                                 | 251 ms: 1.04x faster                                                     |
| regex_effbot               | 2.84 ms                                                                | 2.75 ms: 1.03x faster                                                    |
| logging_simple             | 7.40 us                                                                | 7.19 us: 1.03x faster                                                    |
| scimark_lu                 | 139 ms                                                                 | 136 ms: 1.02x faster                                                     |
| coverage                   | 98.1 ms                                                                | 96.3 ms: 1.02x faster                                                    |
| thrift                     | 908 us                                                                 | 893 us: 1.02x faster                                                     |
| logging_format             | 8.44 us                                                                | 8.31 us: 1.02x faster                                                    |
| crypto_pyaes               | 88.7 ms                                                                | 87.4 ms: 1.02x faster                                                    |
| pprint_pformat             | 1.70 sec                                                               | 1.68 sec: 1.01x faster                                                   |
| float                      | 76.6 ms                                                                | 75.5 ms: 1.01x faster                                                    |
| scimark_fft                | 388 ms                                                                 | 383 ms: 1.01x faster                                                     |
| mako                       | 15.7 ms                                                                | 15.5 ms: 1.01x faster                                                    |
| pprint_safe_repr           | 819 ms                                                                 | 811 ms: 1.01x faster                                                     |
| nqueens                    | 96.5 ms                                                                | 95.8 ms: 1.01x faster                                                    |
| nbody                      | 133 ms                                                                 | 132 ms: 1.01x faster                                                     |
| comprehensions             | 19.8 us                                                                | 19.7 us: 1.00x faster                                                    |
| pickle_pure_python         | 366 us                                                                 | 365 us: 1.00x faster                                                     |
| django_template            | 42.2 ms                                                                | 42.0 ms: 1.00x faster                                                    |
| k_core                     | 2.32 sec                                                               | 2.31 sec: 1.00x faster                                                   |
| dulwich_log                | 82.9 ms                                                                | 82.5 ms: 1.00x faster                                                    |
| sqlalchemy_declarative     | 157 ms                                                                 | 157 ms: 1.00x faster                                                     |
| python_startup_no_site     | 9.64 ms                                                                | 9.62 ms: 1.00x faster                                                    |
| deepcopy_reduce            | 3.17 us                                                                | 3.18 us: 1.00x slower                                                    |
| regex_dna                  | 180 ms                                                                 | 181 ms: 1.00x slower                                                     |
| sqlglot_normalize          | 119 ms                                                                 | 120 ms: 1.00x slower                                                     |
| xml_etree_generate         | 96.3 ms                                                                | 96.7 ms: 1.00x slower                                                    |
| genshi_text                | 27.9 ms                                                                | 28.0 ms: 1.00x slower                                                    |
| pathlib                    | 19.1 ms                                                                | 19.2 ms: 1.00x slower                                                    |
| sympy_str                  | 333 ms                                                                 | 335 ms: 1.01x slower                                                     |
| html5lib                   | 70.8 ms                                                                | 71.3 ms: 1.01x slower                                                    |
| deepcopy                   | 308 us                                                                 | 310 us: 1.01x slower                                                     |
| async_generators           | 372 ms                                                                 | 375 ms: 1.01x slower                                                     |
| bpe_tokeniser              | 4.66 sec                                                               | 4.70 sec: 1.01x slower                                                   |
| sympy_sum                  | 186 ms                                                                 | 187 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed    | 535 ms                                                                 | 540 ms: 1.01x slower                                                     |
| 2to3                       | 305 ms                                                                 | 307 ms: 1.01x slower                                                     |
| xml_etree_process          | 68.5 ms                                                                | 69.1 ms: 1.01x slower                                                    |
| logging_silent             | 114 ns                                                                 | 115 ns: 1.01x slower                                                     |
| hexiom                     | 7.37 ms                                                                | 7.44 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 508 ms: 1.01x slower                                                     |
| sympy_expand               | 546 ms                                                                 | 551 ms: 1.01x slower                                                     |
| json                       | 5.37 ms                                                                | 5.43 ms: 1.01x slower                                                    |
| coroutines                 | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                    |
| json_loads                 | 31.3 us                                                                | 31.6 us: 1.01x slower                                                    |
| unpickle_pure_python       | 247 us                                                                 | 250 us: 1.01x slower                                                     |
| tomli_loads                | 2.32 sec                                                               | 2.34 sec: 1.01x slower                                                   |
| richards                   | 56.6 ms                                                                | 57.2 ms: 1.01x slower                                                    |
| pyflate                    | 488 ms                                                                 | 495 ms: 1.01x slower                                                     |
| fannkuch                   | 483 ms                                                                 | 489 ms: 1.01x slower                                                     |
| async_tree_none            | 288 ms                                                                 | 292 ms: 1.01x slower                                                     |
| bench_thread_pool          | 3.33 ms                                                                | 3.38 ms: 1.01x slower                                                    |
| raytrace                   | 329 ms                                                                 | 334 ms: 1.01x slower                                                     |
| regex_v8                   | 23.4 ms                                                                | 23.8 ms: 1.01x slower                                                    |
| richards_super             | 64.9 ms                                                                | 66.1 ms: 1.02x slower                                                    |
| go                         | 138 ms                                                                 | 141 ms: 1.02x slower                                                     |
| deltablue                  | 4.64 ms                                                                | 4.75 ms: 1.02x slower                                                    |
| chaos                      | 69.2 ms                                                                | 70.9 ms: 1.03x slower                                                    |
| async_tree_io_tg           | 577 ms                                                                 | 593 ms: 1.03x slower                                                     |
| pidigits                   | 193 ms                                                                 | 200 ms: 1.03x slower                                                     |
| spectral_norm              | 106 ms                                                                 | 110 ms: 1.04x slower                                                     |
| mdp                        | 2.59 sec                                                               | 2.78 sec: 1.07x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (34): async_tree_memoization_tg, meteor_contest, json_dumps, subparsers, genshi_xml, sqlglot_transpile, telco, bench_mp_pool, create_gc_cycles, pycparser, asyncio_websockets, sqlglot_parse, gc_traversal, deepcopy_memo, sqlite_synth, async_tree_memoization, generators, docutils, xml_etree_parse, sphinx, python_startup, many_optionals, sqlglot_optimize, scimark_monte_carlo, pylint, sympy_integrate, shortest_path, typing_runtime_protocols, sqlalchemy_imperative, async_tree_io, connected_components, xml_etree_iterparse, regex_compile, scimark_sor

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 94.57% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x