# Results vs. base

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 3aa9426
- commit date: 2024-12-17
- overall geometric mean: 1.006x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 369 ms                                                                 | 368 ms: 1.00x faster                                                     |
| docutils       | 3.09 sec                                                               | 3.11 sec: 1.01x slower                                                   |
| html5lib       | 97.6 ms                                                                | 98.4 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg          | 838 ms                                                                 | 827 ms: 1.01x faster                                                     |
| async_tree_memoization_tg | 449 ms                                                                 | 445 ms: 1.01x faster                                                     |
| async_tree_none_tg        | 361 ms                                                                 | 358 ms: 1.01x faster                                                     |
| async_tree_io             | 855 ms                                                                 | 849 ms: 1.01x faster                                                     |
| coroutines                | 25.0 ms                                                                | 25.2 ms: 1.01x slower                                                    |
| async_generators          | 451 ms                                                                 | 461 ms: 1.02x slower                                                     |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (5): asyncio_websockets, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 138 ms                                                                 | 132 ms: 1.04x faster                                                     |
| float          | 143 ms                                                                 | 141 ms: 1.02x faster                                                     |
| pidigits       | 181 ms                                                                 | 181 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 193 ms                                                                 | 177 ms: 1.09x faster                                                     |
| regex_compile  | 181 ms                                                                 | 179 ms: 1.01x faster                                                     |
| regex_effbot   | 2.81 ms                                                                | 2.90 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 80.2 ms                                                                | 78.2 ms: 1.03x faster                                                    |
| unpickle_pure_python | 339 us                                                                 | 333 us: 1.02x faster                                                     |
| json_loads           | 28.9 us                                                                | 28.7 us: 1.01x faster                                                    |
| xml_etree_generate   | 98.8 ms                                                                | 98.0 ms: 1.01x faster                                                    |
| pickle_pure_python   | 521 us                                                                 | 517 us: 1.01x faster                                                     |
| tomli_loads          | 2.66 sec                                                               | 2.69 sec: 1.01x slower                                                   |
| xml_etree_parse      | 130 ms                                                                 | 132 ms: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 17.9 ms                                                                | 17.8 ms: 1.00x faster                                                    |
| genshi_xml     | 64.1 ms                                                                | 64.7 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark                 | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| scimark_lu                | 187 ms                                                                 | 155 ms: 1.20x faster                                                     |
| regex_dna                 | 193 ms                                                                 | 177 ms: 1.09x faster                                                     |
| scimark_sor               | 237 ms                                                                 | 224 ms: 1.06x faster                                                     |
| deltablue                 | 8.33 ms                                                                | 7.94 ms: 1.05x faster                                                    |
| nbody                     | 138 ms                                                                 | 132 ms: 1.04x faster                                                     |
| richards_super            | 89.5 ms                                                                | 86.3 ms: 1.04x faster                                                    |
| logging_silent            | 190 ns                                                                 | 184 ns: 1.04x faster                                                     |
| thrift                    | 1.19 ms                                                                | 1.15 ms: 1.03x faster                                                    |
| go                        | 276 ms                                                                 | 269 ms: 1.03x faster                                                     |
| richards                  | 78.4 ms                                                                | 76.4 ms: 1.03x faster                                                    |
| xml_etree_process         | 80.2 ms                                                                | 78.2 ms: 1.03x faster                                                    |
| telco                     | 8.87 ms                                                                | 8.67 ms: 1.02x faster                                                    |
| pathlib                   | 20.3 ms                                                                | 19.8 ms: 1.02x faster                                                    |
| raytrace                  | 560 ms                                                                 | 548 ms: 1.02x faster                                                     |
| hexiom                    | 9.91 ms                                                                | 9.71 ms: 1.02x faster                                                    |
| unpickle_pure_python      | 339 us                                                                 | 333 us: 1.02x faster                                                     |
| float                     | 143 ms                                                                 | 141 ms: 1.02x faster                                                     |
| many_optionals            | 1.31 ms                                                                | 1.29 ms: 1.01x faster                                                    |
| dulwich_log               | 97.0 ms                                                                | 95.7 ms: 1.01x faster                                                    |
| async_tree_io_tg          | 838 ms                                                                 | 827 ms: 1.01x faster                                                     |
| sqlite_synth              | 2.30 us                                                                | 2.27 us: 1.01x faster                                                    |
| regex_compile             | 181 ms                                                                 | 179 ms: 1.01x faster                                                     |
| async_tree_memoization_tg | 449 ms                                                                 | 445 ms: 1.01x faster                                                     |
| json_loads                | 28.9 us                                                                | 28.7 us: 1.01x faster                                                    |
| create_gc_cycles          | 1.86 ms                                                                | 1.84 ms: 1.01x faster                                                    |
| async_tree_none_tg        | 361 ms                                                                 | 358 ms: 1.01x faster                                                     |
| xml_etree_generate        | 98.8 ms                                                                | 98.0 ms: 1.01x faster                                                    |
| sympy_str                 | 481 ms                                                                 | 477 ms: 1.01x faster                                                     |
| pickle_pure_python        | 521 us                                                                 | 517 us: 1.01x faster                                                     |
| crypto_pyaes              | 93.3 ms                                                                | 92.6 ms: 1.01x faster                                                    |
| sympy_expand              | 963 ms                                                                 | 956 ms: 1.01x faster                                                     |
| sqlglot_optimize          | 69.7 ms                                                                | 69.2 ms: 1.01x faster                                                    |
| bpe_tokeniser             | 5.06 sec                                                               | 5.02 sec: 1.01x faster                                                   |
| async_tree_io             | 855 ms                                                                 | 849 ms: 1.01x faster                                                     |
| scimark_monte_carlo       | 119 ms                                                                 | 118 ms: 1.01x faster                                                     |
| sympy_integrate           | 29.7 ms                                                                | 29.5 ms: 1.01x faster                                                    |
| deepcopy_memo             | 40.1 us                                                                | 39.9 us: 1.01x faster                                                    |
| pprint_pformat            | 2.05 sec                                                               | 2.04 sec: 1.01x faster                                                   |
| sympy_sum                 | 352 ms                                                                 | 350 ms: 1.01x faster                                                     |
| json                      | 5.12 ms                                                                | 5.09 ms: 1.01x faster                                                    |
| gc_traversal              | 3.54 ms                                                                | 3.52 ms: 1.01x faster                                                    |
| pprint_safe_repr          | 986 ms                                                                 | 981 ms: 1.01x faster                                                     |
| deepcopy_reduce           | 3.55 us                                                                | 3.53 us: 1.00x faster                                                    |
| mako                      | 17.9 ms                                                                | 17.8 ms: 1.00x faster                                                    |
| pycparser                 | 1.54 sec                                                               | 1.53 sec: 1.00x faster                                                   |
| 2to3                      | 369 ms                                                                 | 368 ms: 1.00x faster                                                     |
| comprehensions            | 27.3 us                                                                | 27.2 us: 1.00x faster                                                    |
| k_core                    | 2.43 sec                                                               | 2.42 sec: 1.00x faster                                                   |
| bench_mp_pool             | 109 ms                                                                 | 109 ms: 1.00x faster                                                     |
| python_startup_no_site    | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| pidigits                  | 181 ms                                                                 | 181 ms: 1.00x slower                                                     |
| pyflate                   | 692 ms                                                                 | 696 ms: 1.01x slower                                                     |
| docutils                  | 3.09 sec                                                               | 3.11 sec: 1.01x slower                                                   |
| coroutines                | 25.0 ms                                                                | 25.2 ms: 1.01x slower                                                    |
| nqueens                   | 97.2 ms                                                                | 98.0 ms: 1.01x slower                                                    |
| html5lib                  | 97.6 ms                                                                | 98.4 ms: 1.01x slower                                                    |
| typing_runtime_protocols  | 205 us                                                                 | 207 us: 1.01x slower                                                     |
| genshi_xml                | 64.1 ms                                                                | 64.7 ms: 1.01x slower                                                    |
| tomli_loads               | 2.66 sec                                                               | 2.69 sec: 1.01x slower                                                   |
| xml_etree_parse           | 130 ms                                                                 | 132 ms: 1.01x slower                                                     |
| generators                | 38.3 ms                                                                | 38.8 ms: 1.01x slower                                                    |
| mdp                       | 2.79 sec                                                               | 2.84 sec: 1.02x slower                                                   |
| async_generators          | 451 ms                                                                 | 461 ms: 1.02x slower                                                     |
| spectral_norm             | 123 ms                                                                 | 126 ms: 1.02x slower                                                     |
| scimark_fft               | 405 ms                                                                 | 414 ms: 1.02x slower                                                     |
| fannkuch                  | 496 ms                                                                 | 512 ms: 1.03x slower                                                     |
| regex_effbot              | 2.81 ms                                                                | 2.90 ms: 1.03x slower                                                    |
| coverage                  | 99.3 ms                                                                | 103 ms: 1.04x slower                                                     |
| scimark_sparse_mat_mult   | 5.75 ms                                                                | 6.10 ms: 1.06x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (27): sqlalchemy_imperative, sqlglot_parse, sqlglot_transpile, pylint, asyncio_websockets, async_tree_memoization, shortest_path, logging_simple, async_tree_none, sqlalchemy_declarative, subparsers, sphinx, deepcopy, async_tree_cpu_io_mixed, json_dumps, python_startup, sqlglot_normalize, django_template, chaos, bench_thread_pool, xml_etree_iterparse, genshi_text, async_tree_cpu_io_mixed_tg, regex_v8, connected_components, meteor_contest, logging_format

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x