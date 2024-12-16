# Results vs. base

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 7b72e7b
- commit date: 2024-12-17
- overall geometric mean: 1.000x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 257 ms: 1.00x faster                                                     |
| docutils       | 2.57 sec                                                               | 2.56 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization     | 345 ms                                                                 | 338 ms: 1.02x faster                                                     |
| async_tree_memoization_tg  | 336 ms                                                                 | 330 ms: 1.02x faster                                                     |
| async_tree_io              | 611 ms                                                                 | 601 ms: 1.02x faster                                                     |
| coroutines                 | 22.1 ms                                                                | 21.8 ms: 1.01x faster                                                    |
| async_tree_io_tg           | 625 ms                                                                 | 617 ms: 1.01x faster                                                     |
| async_generators           | 363 ms                                                                 | 359 ms: 1.01x faster                                                     |
| async_tree_none_tg         | 276 ms                                                                 | 274 ms: 1.01x faster                                                     |
| asyncio_websockets         | 523 ms                                                                 | 522 ms: 1.00x faster                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 601 ms: 1.19x slower                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 598 ms: 1.20x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 95.2 ms                                                                | 93.9 ms: 1.01x faster                                                    |
| pidigits       | 186 ms                                                                 | 219 ms: 1.18x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                                 | 172 ms: 1.05x faster                                                     |
| regex_v8       | 24.8 ms                                                                | 24.0 ms: 1.03x faster                                                    |
| regex_compile  | 130 ms                                                                 | 128 ms: 1.01x faster                                                     |
| regex_effbot   | 2.76 ms                                                                | 2.78 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 11.5 ms                                                                | 11.3 ms: 1.01x faster                                                    |
| pickle_pure_python   | 321 us                                                                 | 316 us: 1.01x faster                                                     |
| tomli_loads          | 2.13 sec                                                               | 2.10 sec: 1.01x faster                                                   |
| unpickle_pure_python | 215 us                                                                 | 214 us: 1.00x faster                                                     |
| json_loads           | 25.0 us                                                                | 24.9 us: 1.00x faster                                                    |
| xml_etree_iterparse  | 90.5 ms                                                                | 90.2 ms: 1.00x faster                                                    |
| xml_etree_process    | 59.0 ms                                                                | 59.7 ms: 1.01x slower                                                    |
| xml_etree_generate   | 84.8 ms                                                                | 85.8 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup | 14.6 ms                                                                | 14.5 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml     | 50.6 ms                                                                | 50.0 ms: 1.01x faster                                                    |
| mako           | 11.7 ms                                                                | 11.8 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.49 sec                                                               | 2.35 sec: 1.06x faster                                                   |
| regex_dna                  | 180 ms                                                                 | 172 ms: 1.05x faster                                                     |
| regex_v8                   | 24.8 ms                                                                | 24.0 ms: 1.03x faster                                                    |
| pycparser                  | 1.13 sec                                                               | 1.10 sec: 1.03x faster                                                   |
| async_tree_memoization     | 345 ms                                                                 | 338 ms: 1.02x faster                                                     |
| json                       | 4.59 ms                                                                | 4.49 ms: 1.02x faster                                                    |
| logging_format             | 6.87 us                                                                | 6.73 us: 1.02x faster                                                    |
| meteor_contest             | 101 ms                                                                 | 99.2 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 2.68 us                                                                | 2.63 us: 1.02x faster                                                    |
| scimark_monte_carlo        | 66.4 ms                                                                | 65.1 ms: 1.02x faster                                                    |
| generators                 | 29.2 ms                                                                | 28.7 ms: 1.02x faster                                                    |
| async_tree_memoization_tg  | 336 ms                                                                 | 330 ms: 1.02x faster                                                     |
| spectral_norm              | 110 ms                                                                 | 109 ms: 1.02x faster                                                     |
| async_tree_io              | 611 ms                                                                 | 601 ms: 1.02x faster                                                     |
| logging_simple             | 6.14 us                                                                | 6.04 us: 1.02x faster                                                    |
| comprehensions             | 17.5 us                                                                | 17.2 us: 1.02x faster                                                    |
| nqueens                    | 79.0 ms                                                                | 77.8 ms: 1.02x faster                                                    |
| deepcopy_memo              | 30.6 us                                                                | 30.2 us: 1.01x faster                                                    |
| coroutines                 | 22.1 ms                                                                | 21.8 ms: 1.01x faster                                                    |
| json_dumps                 | 11.5 ms                                                                | 11.3 ms: 1.01x faster                                                    |
| pickle_pure_python         | 321 us                                                                 | 316 us: 1.01x faster                                                     |
| tomli_loads                | 2.13 sec                                                               | 2.10 sec: 1.01x faster                                                   |
| dulwich_log                | 76.4 ms                                                                | 75.3 ms: 1.01x faster                                                    |
| nbody                      | 95.2 ms                                                                | 93.9 ms: 1.01x faster                                                    |
| async_tree_io_tg           | 625 ms                                                                 | 617 ms: 1.01x faster                                                     |
| sympy_integrate            | 20.1 ms                                                                | 19.8 ms: 1.01x faster                                                    |
| regex_compile              | 130 ms                                                                 | 128 ms: 1.01x faster                                                     |
| scimark_lu                 | 111 ms                                                                 | 110 ms: 1.01x faster                                                     |
| genshi_xml                 | 50.6 ms                                                                | 50.0 ms: 1.01x faster                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                | 19.2 ms: 1.01x faster                                                    |
| sqlglot_optimize           | 53.9 ms                                                                | 53.3 ms: 1.01x faster                                                    |
| sympy_sum                  | 155 ms                                                                 | 153 ms: 1.01x faster                                                     |
| sqlglot_normalize          | 108 ms                                                                 | 107 ms: 1.01x faster                                                     |
| async_generators           | 363 ms                                                                 | 359 ms: 1.01x faster                                                     |
| many_optionals             | 1.03 ms                                                                | 1.03 ms: 1.01x faster                                                    |
| deltablue                  | 3.24 ms                                                                | 3.22 ms: 1.01x faster                                                    |
| deepcopy                   | 263 us                                                                 | 261 us: 1.01x faster                                                     |
| scimark_sparse_mat_mult    | 4.51 ms                                                                | 4.47 ms: 1.01x faster                                                    |
| sympy_str                  | 275 ms                                                                 | 273 ms: 1.01x faster                                                     |
| async_tree_none_tg         | 276 ms                                                                 | 274 ms: 1.01x faster                                                     |
| sympy_expand               | 465 ms                                                                 | 462 ms: 1.01x faster                                                     |
| pprint_safe_repr           | 723 ms                                                                 | 718 ms: 1.01x faster                                                     |
| sqlglot_parse              | 1.30 ms                                                                | 1.29 ms: 1.01x faster                                                    |
| logging_silent             | 108 ns                                                                 | 107 ns: 1.01x faster                                                     |
| docutils                   | 2.57 sec                                                               | 2.56 sec: 1.01x faster                                                   |
| sqlalchemy_declarative     | 127 ms                                                                 | 126 ms: 1.00x faster                                                     |
| unpickle_pure_python       | 215 us                                                                 | 214 us: 1.00x faster                                                     |
| bench_thread_pool          | 1.03 ms                                                                | 1.03 ms: 1.00x faster                                                    |
| json_loads                 | 25.0 us                                                                | 24.9 us: 1.00x faster                                                    |
| sqlglot_transpile          | 1.60 ms                                                                | 1.60 ms: 1.00x faster                                                    |
| hexiom                     | 5.93 ms                                                                | 5.91 ms: 1.00x faster                                                    |
| 2to3                       | 258 ms                                                                 | 257 ms: 1.00x faster                                                     |
| scimark_fft                | 338 ms                                                                 | 337 ms: 1.00x faster                                                     |
| asyncio_websockets         | 523 ms                                                                 | 522 ms: 1.00x faster                                                     |
| xml_etree_iterparse        | 90.5 ms                                                                | 90.2 ms: 1.00x faster                                                    |
| python_startup             | 14.6 ms                                                                | 14.5 ms: 1.00x faster                                                    |
| pyflate                    | 447 ms                                                                 | 449 ms: 1.00x slower                                                     |
| go                         | 121 ms                                                                 | 122 ms: 1.01x slower                                                     |
| regex_effbot               | 2.76 ms                                                                | 2.78 ms: 1.01x slower                                                    |
| connected_components       | 399 ms                                                                 | 401 ms: 1.01x slower                                                     |
| mako                       | 11.7 ms                                                                | 11.8 ms: 1.01x slower                                                    |
| xml_etree_process          | 59.0 ms                                                                | 59.7 ms: 1.01x slower                                                    |
| xml_etree_generate         | 84.8 ms                                                                | 85.8 ms: 1.01x slower                                                    |
| fannkuch                   | 371 ms                                                                 | 377 ms: 1.01x slower                                                     |
| gc_traversal               | 4.04 ms                                                                | 4.41 ms: 1.09x slower                                                    |
| pidigits                   | 186 ms                                                                 | 219 ms: 1.18x slower                                                     |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 601 ms: 1.19x slower                                                     |
| async_tree_cpu_io_mixed_tg | 500 ms                                                                 | 598 ms: 1.20x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (27): float, async_tree_none, django_template, sphinx, pylint, typing_runtime_protocols, richards, richards_super, coverage, xml_etree_parse, chaos, subparsers, pathlib, bpe_tokeniser, bench_mp_pool, python_startup_no_site, crypto_pyaes, shortest_path, k_core, sqlite_synth, raytrace, scimark_sor, pprint_pformat, genshi_text, create_gc_cycles, telco, thrift

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x