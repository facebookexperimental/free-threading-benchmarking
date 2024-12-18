# Results vs. base

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 6ef74ac
- commit date: 2024-12-18
- overall geometric mean: 1.011x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 369 ms                                                                 | 366 ms: 1.01x faster                                                     |
| html5lib       | 97.6 ms                                                                | 98.1 ms: 1.01x slower                                                    |
| sphinx         | 1.19 sec                                                               | 1.18 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg          | 838 ms                                                                 | 827 ms: 1.01x faster                                                     |
| async_tree_none_tg        | 361 ms                                                                 | 356 ms: 1.01x faster                                                     |
| async_tree_memoization_tg | 449 ms                                                                 | 445 ms: 1.01x faster                                                     |
| coroutines                | 25.0 ms                                                                | 24.8 ms: 1.01x faster                                                    |
| async_tree_io             | 855 ms                                                                 | 849 ms: 1.01x faster                                                     |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, asyncio_websockets, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 138 ms                                                                 | 130 ms: 1.06x faster                                                     |
| float          | 143 ms                                                                 | 138 ms: 1.03x faster                                                     |
| pidigits       | 181 ms                                                                 | 184 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 193 ms                                                                 | 184 ms: 1.05x faster                                                     |
| regex_compile  | 181 ms                                                                 | 179 ms: 1.01x faster                                                     |
| regex_v8       | 24.7 ms                                                                | 25.5 ms: 1.03x slower                                                    |
| regex_effbot   | 2.81 ms                                                                | 2.92 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|---------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads          | 28.9 us                                                                | 28.1 us: 1.03x faster                                                    |
| xml_etree_process   | 80.2 ms                                                                | 78.3 ms: 1.02x faster                                                    |
| pickle_pure_python  | 521 us                                                                 | 516 us: 1.01x faster                                                     |
| xml_etree_iterparse | 91.8 ms                                                                | 91.0 ms: 1.01x faster                                                    |
| xml_etree_generate  | 98.8 ms                                                                | 98.4 ms: 1.00x faster                                                    |
| xml_etree_parse     | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| tomli_loads         | 2.66 sec                                                               | 2.69 sec: 1.01x slower                                                   |
| Geometric mean      | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (2): json_dumps, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.4 ms: 1.00x faster                                                    |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 32.1 ms                                                                | 31.4 ms: 1.02x faster                                                    |
| django_template | 51.4 ms                                                                | 50.7 ms: 1.01x faster                                                    |
| genshi_xml      | 64.1 ms                                                                | 63.4 ms: 1.01x faster                                                    |
| mako            | 17.9 ms                                                                | 17.8 ms: 1.01x faster                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                 | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241218-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-6ef74ac |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| scimark_lu                | 187 ms                                                                 | 155 ms: 1.21x faster                                                     |
| gc_traversal              | 3.54 ms                                                                | 3.17 ms: 1.11x faster                                                    |
| nbody                     | 138 ms                                                                 | 130 ms: 1.06x faster                                                     |
| regex_dna                 | 193 ms                                                                 | 184 ms: 1.05x faster                                                     |
| scimark_sor               | 237 ms                                                                 | 226 ms: 1.05x faster                                                     |
| deltablue                 | 8.33 ms                                                                | 8.02 ms: 1.04x faster                                                    |
| float                     | 143 ms                                                                 | 138 ms: 1.03x faster                                                     |
| json_loads                | 28.9 us                                                                | 28.1 us: 1.03x faster                                                    |
| sqlglot_parse             | 2.62 ms                                                                | 2.55 ms: 1.03x faster                                                    |
| go                        | 276 ms                                                                 | 269 ms: 1.03x faster                                                     |
| create_gc_cycles          | 1.86 ms                                                                | 1.81 ms: 1.03x faster                                                    |
| richards                  | 78.4 ms                                                                | 76.5 ms: 1.03x faster                                                    |
| sqlglot_transpile         | 3.03 ms                                                                | 2.96 ms: 1.02x faster                                                    |
| xml_etree_process         | 80.2 ms                                                                | 78.3 ms: 1.02x faster                                                    |
| pprint_pformat            | 2.05 sec                                                               | 2.00 sec: 1.02x faster                                                   |
| pprint_safe_repr          | 986 ms                                                                 | 964 ms: 1.02x faster                                                     |
| genshi_text               | 32.1 ms                                                                | 31.4 ms: 1.02x faster                                                    |
| many_optionals            | 1.31 ms                                                                | 1.28 ms: 1.02x faster                                                    |
| typing_runtime_protocols  | 205 us                                                                 | 201 us: 1.02x faster                                                     |
| sqlite_synth              | 2.30 us                                                                | 2.26 us: 1.02x faster                                                    |
| thrift                    | 1.19 ms                                                                | 1.16 ms: 1.02x faster                                                    |
| raytrace                  | 560 ms                                                                 | 549 ms: 1.02x faster                                                     |
| scimark_fft               | 405 ms                                                                 | 397 ms: 1.02x faster                                                     |
| dulwich_log               | 97.0 ms                                                                | 95.4 ms: 1.02x faster                                                    |
| hexiom                    | 9.91 ms                                                                | 9.75 ms: 1.02x faster                                                    |
| deepcopy_reduce           | 3.55 us                                                                | 3.49 us: 1.02x faster                                                    |
| json                      | 5.12 ms                                                                | 5.04 ms: 1.01x faster                                                    |
| django_template           | 51.4 ms                                                                | 50.7 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult   | 5.75 ms                                                                | 5.68 ms: 1.01x faster                                                    |
| async_tree_io_tg          | 838 ms                                                                 | 827 ms: 1.01x faster                                                     |
| async_tree_none_tg        | 361 ms                                                                 | 356 ms: 1.01x faster                                                     |
| genshi_xml                | 64.1 ms                                                                | 63.4 ms: 1.01x faster                                                    |
| sympy_str                 | 481 ms                                                                 | 475 ms: 1.01x faster                                                     |
| regex_compile             | 181 ms                                                                 | 179 ms: 1.01x faster                                                     |
| sqlglot_normalize         | 138 ms                                                                 | 136 ms: 1.01x faster                                                     |
| sympy_expand              | 963 ms                                                                 | 953 ms: 1.01x faster                                                     |
| pickle_pure_python        | 521 us                                                                 | 516 us: 1.01x faster                                                     |
| sqlglot_optimize          | 69.7 ms                                                                | 68.9 ms: 1.01x faster                                                    |
| async_tree_memoization_tg | 449 ms                                                                 | 445 ms: 1.01x faster                                                     |
| bpe_tokeniser             | 5.06 sec                                                               | 5.01 sec: 1.01x faster                                                   |
| scimark_monte_carlo       | 119 ms                                                                 | 118 ms: 1.01x faster                                                     |
| 2to3                      | 369 ms                                                                 | 366 ms: 1.01x faster                                                     |
| subparsers                | 31.6 ms                                                                | 31.3 ms: 1.01x faster                                                    |
| crypto_pyaes              | 93.3 ms                                                                | 92.5 ms: 1.01x faster                                                    |
| xml_etree_iterparse       | 91.8 ms                                                                | 91.0 ms: 1.01x faster                                                    |
| logging_silent            | 190 ns                                                                 | 189 ns: 1.01x faster                                                     |
| deepcopy                  | 332 us                                                                 | 329 us: 1.01x faster                                                     |
| sympy_integrate           | 29.7 ms                                                                | 29.4 ms: 1.01x faster                                                    |
| coroutines                | 25.0 ms                                                                | 24.8 ms: 1.01x faster                                                    |
| sphinx                    | 1.19 sec                                                               | 1.18 sec: 1.01x faster                                                   |
| async_tree_io             | 855 ms                                                                 | 849 ms: 1.01x faster                                                     |
| sympy_sum                 | 352 ms                                                                 | 350 ms: 1.01x faster                                                     |
| pycparser                 | 1.54 sec                                                               | 1.53 sec: 1.01x faster                                                   |
| mdp                       | 2.79 sec                                                               | 2.77 sec: 1.01x faster                                                   |
| comprehensions            | 27.3 us                                                                | 27.1 us: 1.01x faster                                                    |
| mako                      | 17.9 ms                                                                | 17.8 ms: 1.01x faster                                                    |
| chaos                     | 105 ms                                                                 | 104 ms: 1.01x faster                                                     |
| sqlalchemy_declarative    | 204 ms                                                                 | 203 ms: 1.01x faster                                                     |
| xml_etree_generate        | 98.8 ms                                                                | 98.4 ms: 1.00x faster                                                    |
| python_startup            | 17.5 ms                                                                | 17.4 ms: 1.00x faster                                                    |
| bench_mp_pool             | 109 ms                                                                 | 109 ms: 1.00x faster                                                     |
| python_startup_no_site    | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| k_core                    | 2.43 sec                                                               | 2.42 sec: 1.00x faster                                                   |
| nqueens                   | 97.2 ms                                                                | 97.6 ms: 1.00x slower                                                    |
| html5lib                  | 97.6 ms                                                                | 98.1 ms: 1.01x slower                                                    |
| xml_etree_parse           | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| spectral_norm             | 123 ms                                                                 | 124 ms: 1.01x slower                                                     |
| connected_components      | 498 ms                                                                 | 503 ms: 1.01x slower                                                     |
| logging_simple            | 10.7 us                                                                | 10.8 us: 1.01x slower                                                    |
| pathlib                   | 20.3 ms                                                                | 20.5 ms: 1.01x slower                                                    |
| tomli_loads               | 2.66 sec                                                               | 2.69 sec: 1.01x slower                                                   |
| logging_format            | 11.9 us                                                                | 12.1 us: 1.01x slower                                                    |
| fannkuch                  | 496 ms                                                                 | 504 ms: 1.02x slower                                                     |
| pidigits                  | 181 ms                                                                 | 184 ms: 1.02x slower                                                     |
| regex_v8                  | 24.7 ms                                                                | 25.5 ms: 1.03x slower                                                    |
| regex_effbot              | 2.81 ms                                                                | 2.92 ms: 1.04x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (20): sqlalchemy_imperative, richards_super, telco, pylint, async_tree_cpu_io_mixed, json_dumps, asyncio_websockets, async_tree_none, async_tree_cpu_io_mixed_tg, bench_thread_pool, coverage, async_tree_memoization, unpickle_pure_python, docutils, pyflate, async_generators, deepcopy_memo, shortest_path, generators, meteor_contest

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x