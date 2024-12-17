# Results vs. base

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 3aa9426
- commit date: 2024-12-17
- overall geometric mean: 1.004x slower
- HPT reliability: 99.60%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 257 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 336 ms                                                                 | 330 ms: 1.02x faster                                                     |
| async_tree_memoization     | 345 ms                                                                 | 341 ms: 1.01x faster                                                     |
| async_tree_none_tg         | 276 ms                                                                 | 273 ms: 1.01x faster                                                     |
| coroutines                 | 22.1 ms                                                                | 22.0 ms: 1.01x faster                                                    |
| async_generators           | 363 ms                                                                 | 362 ms: 1.00x faster                                                     |
| asyncio_websockets         | 523 ms                                                                 | 523 ms: 1.00x faster                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 605 ms: 1.20x slower                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 601 ms: 1.20x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                             |

Benchmark hidden because not significant (3): async_tree_io_tg, async_tree_none, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                 | 222 ms: 1.20x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                             |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                                 | 171 ms: 1.05x faster                                                     |
| regex_v8       | 24.8 ms                                                                | 24.3 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (2): regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.13 sec                                                               | 2.11 sec: 1.01x faster                                                   |
| unpickle_pure_python | 215 us                                                                 | 215 us: 1.00x slower                                                     |
| pickle_pure_python   | 321 us                                                                 | 322 us: 1.00x slower                                                     |
| json_loads           | 25.0 us                                                                | 25.1 us: 1.00x slower                                                    |
| xml_etree_generate   | 84.8 ms                                                                | 85.2 ms: 1.00x slower                                                    |
| xml_etree_iterparse  | 90.5 ms                                                                | 91.0 ms: 1.01x slower                                                    |
| xml_etree_parse      | 127 ms                                                                 | 128 ms: 1.01x slower                                                     |
| xml_etree_process    | 59.0 ms                                                                | 59.6 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.46 ms                                                                | 7.48 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 35.5 ms                                                                | 35.3 ms: 1.01x faster                                                    |
| genshi_text     | 22.0 ms                                                                | 21.8 ms: 1.01x faster                                                    |
| mako            | 11.7 ms                                                                | 11.9 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.49 sec                                                               | 2.35 sec: 1.06x faster                                                   |
| regex_dna                  | 180 ms                                                                 | 171 ms: 1.05x faster                                                     |
| pycparser                  | 1.13 sec                                                               | 1.11 sec: 1.03x faster                                                   |
| regex_v8                   | 24.8 ms                                                                | 24.3 ms: 1.02x faster                                                    |
| async_tree_memoization_tg  | 336 ms                                                                 | 330 ms: 1.02x faster                                                     |
| scimark_lu                 | 111 ms                                                                 | 109 ms: 1.02x faster                                                     |
| scimark_monte_carlo        | 66.4 ms                                                                | 65.5 ms: 1.01x faster                                                    |
| generators                 | 29.2 ms                                                                | 28.8 ms: 1.01x faster                                                    |
| async_tree_memoization     | 345 ms                                                                 | 341 ms: 1.01x faster                                                     |
| sympy_expand               | 465 ms                                                                 | 460 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult    | 4.51 ms                                                                | 4.46 ms: 1.01x faster                                                    |
| logging_format             | 6.87 us                                                                | 6.80 us: 1.01x faster                                                    |
| logging_simple             | 6.14 us                                                                | 6.08 us: 1.01x faster                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                | 19.3 ms: 1.01x faster                                                    |
| dulwich_log                | 76.4 ms                                                                | 75.7 ms: 1.01x faster                                                    |
| async_tree_none_tg         | 276 ms                                                                 | 273 ms: 1.01x faster                                                     |
| sympy_str                  | 275 ms                                                                 | 273 ms: 1.01x faster                                                     |
| sympy_integrate            | 20.1 ms                                                                | 19.9 ms: 1.01x faster                                                    |
| logging_silent             | 108 ns                                                                 | 107 ns: 1.01x faster                                                     |
| coroutines                 | 22.1 ms                                                                | 22.0 ms: 1.01x faster                                                    |
| many_optionals             | 1.03 ms                                                                | 1.03 ms: 1.01x faster                                                    |
| tomli_loads                | 2.13 sec                                                               | 2.11 sec: 1.01x faster                                                   |
| sqlglot_parse              | 1.30 ms                                                                | 1.29 ms: 1.01x faster                                                    |
| sympy_sum                  | 155 ms                                                                 | 154 ms: 1.01x faster                                                     |
| django_template            | 35.5 ms                                                                | 35.3 ms: 1.01x faster                                                    |
| deepcopy_reduce            | 2.68 us                                                                | 2.66 us: 1.01x faster                                                    |
| 2to3                       | 258 ms                                                                 | 257 ms: 1.01x faster                                                     |
| pprint_safe_repr           | 723 ms                                                                 | 718 ms: 1.01x faster                                                     |
| sqlglot_transpile          | 1.60 ms                                                                | 1.59 ms: 1.01x faster                                                    |
| deltablue                  | 3.24 ms                                                                | 3.23 ms: 1.01x faster                                                    |
| genshi_text                | 22.0 ms                                                                | 21.8 ms: 1.01x faster                                                    |
| crypto_pyaes               | 68.7 ms                                                                | 68.4 ms: 1.01x faster                                                    |
| sqlalchemy_declarative     | 127 ms                                                                 | 127 ms: 1.00x faster                                                     |
| meteor_contest             | 101 ms                                                                 | 101 ms: 1.00x faster                                                     |
| bpe_tokeniser              | 4.34 sec                                                               | 4.33 sec: 1.00x faster                                                   |
| sqlglot_optimize           | 53.9 ms                                                                | 53.8 ms: 1.00x faster                                                    |
| async_generators           | 363 ms                                                                 | 362 ms: 1.00x faster                                                     |
| asyncio_websockets         | 523 ms                                                                 | 523 ms: 1.00x faster                                                     |
| python_startup_no_site     | 7.46 ms                                                                | 7.48 ms: 1.00x slower                                                    |
| scimark_fft                | 338 ms                                                                 | 339 ms: 1.00x slower                                                     |
| unpickle_pure_python       | 215 us                                                                 | 215 us: 1.00x slower                                                     |
| pickle_pure_python         | 321 us                                                                 | 322 us: 1.00x slower                                                     |
| json_loads                 | 25.0 us                                                                | 25.1 us: 1.00x slower                                                    |
| xml_etree_generate         | 84.8 ms                                                                | 85.2 ms: 1.00x slower                                                    |
| spectral_norm              | 110 ms                                                                 | 111 ms: 1.01x slower                                                     |
| xml_etree_iterparse        | 90.5 ms                                                                | 91.0 ms: 1.01x slower                                                    |
| chaos                      | 59.2 ms                                                                | 59.6 ms: 1.01x slower                                                    |
| create_gc_cycles           | 1.70 ms                                                                | 1.71 ms: 1.01x slower                                                    |
| telco                      | 7.31 ms                                                                | 7.37 ms: 1.01x slower                                                    |
| subparsers                 | 22.1 ms                                                                | 22.3 ms: 1.01x slower                                                    |
| thrift                     | 736 us                                                                 | 743 us: 1.01x slower                                                     |
| xml_etree_parse            | 127 ms                                                                 | 128 ms: 1.01x slower                                                     |
| xml_etree_process          | 59.0 ms                                                                | 59.6 ms: 1.01x slower                                                    |
| pathlib                    | 18.2 ms                                                                | 18.5 ms: 1.01x slower                                                    |
| mako                       | 11.7 ms                                                                | 11.9 ms: 1.02x slower                                                    |
| fannkuch                   | 371 ms                                                                 | 382 ms: 1.03x slower                                                     |
| sqlite_synth               | 2.23 us                                                                | 2.31 us: 1.04x slower                                                    |
| gc_traversal               | 4.04 ms                                                                | 4.29 ms: 1.06x slower                                                    |
| pidigits                   | 186 ms                                                                 | 222 ms: 1.20x slower                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 605 ms: 1.20x slower                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 601 ms: 1.20x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (34): json, pylint, float, async_tree_io_tg, coverage, async_tree_none, richards, sqlglot_normalize, bench_thread_pool, deepcopy, richards_super, scimark_sor, async_tree_io, nqueens, go, deepcopy_memo, docutils, regex_compile, bench_mp_pool, python_startup, pprint_pformat, pyflate, sphinx, hexiom, nbody, raytrace, connected_components, comprehensions, genshi_xml, json_dumps, regex_effbot, k_core, shortest_path, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 99.60% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x