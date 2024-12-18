# Results vs. base

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 6ef74ac
- commit date: 2024-12-18
- overall geometric mean: 1.005x slower
- HPT reliability: 99.62%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 258 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization     | 345 ms                                                                 | 341 ms: 1.01x faster                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 332 ms: 1.01x faster                                                     |
| coroutines                 | 22.1 ms                                                                | 21.9 ms: 1.01x faster                                                    |
| async_tree_none_tg         | 276 ms                                                                 | 273 ms: 1.01x faster                                                     |
| async_tree_io              | 611 ms                                                                 | 607 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 597 ms: 1.19x slower                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 603 ms: 1.19x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                             |

Benchmark hidden because not significant (4): async_tree_io_tg, async_tree_none, asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.2 ms                                                                | 78.6 ms: 1.02x faster                                                    |
| pidigits       | 186 ms                                                                 | 221 ms: 1.19x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                                 | 175 ms: 1.03x faster                                                     |
| regex_effbot   | 2.76 ms                                                                | 2.70 ms: 1.02x faster                                                    |
| regex_compile  | 130 ms                                                                 | 129 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.13 sec                                                               | 2.10 sec: 1.01x faster                                                   |
| pickle_pure_python   | 321 us                                                                 | 319 us: 1.01x faster                                                     |
| unpickle_pure_python | 215 us                                                                 | 214 us: 1.00x faster                                                     |
| xml_etree_parse      | 127 ms                                                                 | 127 ms: 1.00x slower                                                     |
| xml_etree_generate   | 84.8 ms                                                                | 85.2 ms: 1.00x slower                                                    |
| xml_etree_process    | 59.0 ms                                                                | 59.5 ms: 1.01x slower                                                    |
| xml_etree_iterparse  | 90.5 ms                                                                | 91.3 ms: 1.01x slower                                                    |
| json_dumps           | 11.5 ms                                                                | 11.6 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.7 ms: 1.01x slower                                                    |
| python_startup_no_site | 7.46 ms                                                                | 7.53 ms: 1.01x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 35.5 ms                                                                | 35.2 ms: 1.01x faster                                                    |
| mako            | 11.7 ms                                                                | 11.9 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| logging_silent             | 108 ns                                                                 | 102 ns: 1.05x faster                                                     |
| crypto_pyaes               | 68.7 ms                                                                | 66.5 ms: 1.03x faster                                                    |
| scimark_monte_carlo        | 66.4 ms                                                                | 64.5 ms: 1.03x faster                                                    |
| regex_dna                  | 180 ms                                                                 | 175 ms: 1.03x faster                                                     |
| generators                 | 29.2 ms                                                                | 28.6 ms: 1.02x faster                                                    |
| float                      | 80.2 ms                                                                | 78.6 ms: 1.02x faster                                                    |
| regex_effbot               | 2.76 ms                                                                | 2.70 ms: 1.02x faster                                                    |
| go                         | 121 ms                                                                 | 119 ms: 1.02x faster                                                     |
| richards                   | 45.8 ms                                                                | 45.0 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 2.68 us                                                                | 2.64 us: 1.02x faster                                                    |
| deltablue                  | 3.24 ms                                                                | 3.19 ms: 1.02x faster                                                    |
| spectral_norm              | 110 ms                                                                 | 109 ms: 1.01x faster                                                     |
| tomli_loads                | 2.13 sec                                                               | 2.10 sec: 1.01x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 132 ms: 1.01x faster                                                     |
| async_tree_memoization     | 345 ms                                                                 | 341 ms: 1.01x faster                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 332 ms: 1.01x faster                                                     |
| telco                      | 7.31 ms                                                                | 7.22 ms: 1.01x faster                                                    |
| raytrace                   | 266 ms                                                                 | 263 ms: 1.01x faster                                                     |
| json                       | 4.59 ms                                                                | 4.54 ms: 1.01x faster                                                    |
| scimark_lu                 | 111 ms                                                                 | 110 ms: 1.01x faster                                                     |
| richards_super             | 52.1 ms                                                                | 51.6 ms: 1.01x faster                                                    |
| pycparser                  | 1.13 sec                                                               | 1.12 sec: 1.01x faster                                                   |
| django_template            | 35.5 ms                                                                | 35.2 ms: 1.01x faster                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                | 19.3 ms: 1.01x faster                                                    |
| coroutines                 | 22.1 ms                                                                | 21.9 ms: 1.01x faster                                                    |
| async_tree_none_tg         | 276 ms                                                                 | 273 ms: 1.01x faster                                                     |
| meteor_contest             | 101 ms                                                                 | 101 ms: 1.01x faster                                                     |
| async_tree_io              | 611 ms                                                                 | 607 ms: 1.01x faster                                                     |
| regex_compile              | 130 ms                                                                 | 129 ms: 1.01x faster                                                     |
| pickle_pure_python         | 321 us                                                                 | 319 us: 1.01x faster                                                     |
| coverage                   | 80.1 ms                                                                | 79.7 ms: 1.01x faster                                                    |
| sympy_integrate            | 20.1 ms                                                                | 20.0 ms: 1.01x faster                                                    |
| sympy_sum                  | 155 ms                                                                 | 154 ms: 1.01x faster                                                     |
| many_optionals             | 1.03 ms                                                                | 1.03 ms: 1.00x faster                                                    |
| chaos                      | 59.2 ms                                                                | 58.9 ms: 1.00x faster                                                    |
| unpickle_pure_python       | 215 us                                                                 | 214 us: 1.00x faster                                                     |
| 2to3                       | 258 ms                                                                 | 258 ms: 1.00x faster                                                     |
| sqlglot_parse              | 1.30 ms                                                                | 1.29 ms: 1.00x faster                                                    |
| deepcopy_memo              | 30.6 us                                                                | 30.6 us: 1.00x faster                                                    |
| bpe_tokeniser              | 4.34 sec                                                               | 4.35 sec: 1.00x slower                                                   |
| xml_etree_parse            | 127 ms                                                                 | 127 ms: 1.00x slower                                                     |
| xml_etree_generate         | 84.8 ms                                                                | 85.2 ms: 1.00x slower                                                    |
| deepcopy                   | 263 us                                                                 | 264 us: 1.01x slower                                                     |
| pprint_pformat             | 1.47 sec                                                               | 1.48 sec: 1.01x slower                                                   |
| fannkuch                   | 371 ms                                                                 | 373 ms: 1.01x slower                                                     |
| mdp                        | 2.49 sec                                                               | 2.50 sec: 1.01x slower                                                   |
| pprint_safe_repr           | 723 ms                                                                 | 727 ms: 1.01x slower                                                     |
| python_startup             | 14.6 ms                                                                | 14.7 ms: 1.01x slower                                                    |
| shortest_path              | 441 ms                                                                 | 444 ms: 1.01x slower                                                     |
| bench_mp_pool              | 85.5 ms                                                                | 86.2 ms: 1.01x slower                                                    |
| thrift                     | 736 us                                                                 | 742 us: 1.01x slower                                                     |
| python_startup_no_site     | 7.46 ms                                                                | 7.53 ms: 1.01x slower                                                    |
| xml_etree_process          | 59.0 ms                                                                | 59.5 ms: 1.01x slower                                                    |
| xml_etree_iterparse        | 90.5 ms                                                                | 91.3 ms: 1.01x slower                                                    |
| json_dumps                 | 11.5 ms                                                                | 11.6 ms: 1.01x slower                                                    |
| connected_components       | 399 ms                                                                 | 404 ms: 1.01x slower                                                     |
| mako                       | 11.7 ms                                                                | 11.9 ms: 1.02x slower                                                    |
| create_gc_cycles           | 1.70 ms                                                                | 1.73 ms: 1.02x slower                                                    |
| gc_traversal               | 4.04 ms                                                                | 4.77 ms: 1.18x slower                                                    |
| pidigits                   | 186 ms                                                                 | 221 ms: 1.19x slower                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 597 ms: 1.19x slower                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 603 ms: 1.19x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (33): sqlite_synth, subparsers, sympy_expand, sympy_str, hexiom, logging_simple, dulwich_log, regex_v8, docutils, pathlib, bench_thread_pool, async_tree_io_tg, async_tree_none, pyflate, sphinx, pylint, k_core, sqlglot_transpile, asyncio_websockets, sqlglot_optimize, sqlalchemy_declarative, genshi_text, scimark_fft, nqueens, json_loads, async_generators, logging_format, nbody, typing_runtime_protocols, comprehensions, genshi_xml, sqlglot_normalize, scimark_sparse_mat_mult

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 99.62% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x