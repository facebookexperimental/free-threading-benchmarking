# Results vs. base

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 47b80b4
- commit date: 2024-12-19
- overall geometric mean: 1.012x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 369 ms                                                                 | 366 ms: 1.01x faster                                                     |
| html5lib       | 97.6 ms                                                                | 98.8 ms: 1.01x slower                                                    |
| sphinx         | 1.19 sec                                                               | 1.19 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg          | 838 ms                                                                 | 823 ms: 1.02x faster                                                     |
| coroutines                | 25.0 ms                                                                | 24.6 ms: 1.02x faster                                                    |
| async_tree_memoization_tg | 449 ms                                                                 | 443 ms: 1.01x faster                                                     |
| async_tree_none_tg        | 361 ms                                                                 | 358 ms: 1.01x faster                                                     |
| async_tree_none           | 389 ms                                                                 | 387 ms: 1.01x faster                                                     |
| asyncio_websockets        | 520 ms                                                                 | 517 ms: 1.00x faster                                                     |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (5): async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed, async_generators, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 138 ms                                                                 | 134 ms: 1.03x faster                                                     |
| float          | 143 ms                                                                 | 140 ms: 1.02x faster                                                     |
| pidigits       | 181 ms                                                                 | 182 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 193 ms                                                                 | 184 ms: 1.05x faster                                                     |
| regex_compile  | 181 ms                                                                 | 179 ms: 1.01x faster                                                     |
| regex_v8       | 24.7 ms                                                                | 24.9 ms: 1.01x slower                                                    |
| regex_effbot   | 2.81 ms                                                                | 2.90 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 80.2 ms                                                                | 77.4 ms: 1.04x faster                                                    |
| json_loads           | 28.9 us                                                                | 28.2 us: 1.03x faster                                                    |
| pickle_pure_python   | 521 us                                                                 | 511 us: 1.02x faster                                                     |
| xml_etree_generate   | 98.8 ms                                                                | 97.3 ms: 1.02x faster                                                    |
| unpickle_pure_python | 339 us                                                                 | 335 us: 1.01x faster                                                     |
| xml_etree_iterparse  | 91.8 ms                                                                | 91.1 ms: 1.01x faster                                                    |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| json_dumps           | 14.2 ms                                                                | 14.5 ms: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                    |
| python_startup         | 17.5 ms                                                                | 17.4 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml     | 64.1 ms                                                                | 63.3 ms: 1.01x faster                                                    |
| genshi_text    | 32.1 ms                                                                | 31.7 ms: 1.01x faster                                                    |
| mako           | 17.9 ms                                                                | 17.7 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                 | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|---------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| scimark_lu                | 187 ms                                                                 | 156 ms: 1.20x faster                                                     |
| gc_traversal              | 3.54 ms                                                                | 3.17 ms: 1.11x faster                                                    |
| scimark_sor               | 237 ms                                                                 | 221 ms: 1.07x faster                                                     |
| regex_dna                 | 193 ms                                                                 | 184 ms: 1.05x faster                                                     |
| deltablue                 | 8.33 ms                                                                | 7.98 ms: 1.04x faster                                                    |
| logging_silent            | 190 ns                                                                 | 184 ns: 1.04x faster                                                     |
| xml_etree_process         | 80.2 ms                                                                | 77.4 ms: 1.04x faster                                                    |
| thrift                    | 1.19 ms                                                                | 1.15 ms: 1.03x faster                                                    |
| create_gc_cycles          | 1.86 ms                                                                | 1.80 ms: 1.03x faster                                                    |
| richards_super            | 89.5 ms                                                                | 86.9 ms: 1.03x faster                                                    |
| nbody                     | 138 ms                                                                 | 134 ms: 1.03x faster                                                     |
| json_loads                | 28.9 us                                                                | 28.2 us: 1.03x faster                                                    |
| spectral_norm             | 123 ms                                                                 | 120 ms: 1.03x faster                                                     |
| telco                     | 8.87 ms                                                                | 8.66 ms: 1.02x faster                                                    |
| float                     | 143 ms                                                                 | 140 ms: 1.02x faster                                                     |
| raytrace                  | 560 ms                                                                 | 547 ms: 1.02x faster                                                     |
| sqlglot_parse             | 2.62 ms                                                                | 2.57 ms: 1.02x faster                                                    |
| go                        | 276 ms                                                                 | 271 ms: 1.02x faster                                                     |
| pickle_pure_python        | 521 us                                                                 | 511 us: 1.02x faster                                                     |
| sqlglot_transpile         | 3.03 ms                                                                | 2.97 ms: 1.02x faster                                                    |
| richards                  | 78.4 ms                                                                | 76.9 ms: 1.02x faster                                                    |
| hexiom                    | 9.91 ms                                                                | 9.72 ms: 1.02x faster                                                    |
| async_tree_io_tg          | 838 ms                                                                 | 823 ms: 1.02x faster                                                     |
| deepcopy_reduce           | 3.55 us                                                                | 3.48 us: 1.02x faster                                                    |
| sqlglot_normalize         | 138 ms                                                                 | 135 ms: 1.02x faster                                                     |
| coroutines                | 25.0 ms                                                                | 24.6 ms: 1.02x faster                                                    |
| pprint_safe_repr          | 986 ms                                                                 | 970 ms: 1.02x faster                                                     |
| xml_etree_generate        | 98.8 ms                                                                | 97.3 ms: 1.02x faster                                                    |
| dulwich_log               | 97.0 ms                                                                | 95.5 ms: 1.02x faster                                                    |
| deepcopy_memo             | 40.1 us                                                                | 39.5 us: 1.02x faster                                                    |
| many_optionals            | 1.31 ms                                                                | 1.29 ms: 1.02x faster                                                    |
| deepcopy                  | 332 us                                                                 | 327 us: 1.01x faster                                                     |
| async_tree_memoization_tg | 449 ms                                                                 | 443 ms: 1.01x faster                                                     |
| genshi_xml                | 64.1 ms                                                                | 63.3 ms: 1.01x faster                                                    |
| pprint_pformat            | 2.05 sec                                                               | 2.02 sec: 1.01x faster                                                   |
| logging_simple            | 10.7 us                                                                | 10.6 us: 1.01x faster                                                    |
| crypto_pyaes              | 93.3 ms                                                                | 92.1 ms: 1.01x faster                                                    |
| sqlglot_optimize          | 69.7 ms                                                                | 68.8 ms: 1.01x faster                                                    |
| nqueens                   | 97.2 ms                                                                | 96.0 ms: 1.01x faster                                                    |
| genshi_text               | 32.1 ms                                                                | 31.7 ms: 1.01x faster                                                    |
| mako                      | 17.9 ms                                                                | 17.7 ms: 1.01x faster                                                    |
| unpickle_pure_python      | 339 us                                                                 | 335 us: 1.01x faster                                                     |
| meteor_contest            | 130 ms                                                                 | 128 ms: 1.01x faster                                                     |
| regex_compile             | 181 ms                                                                 | 179 ms: 1.01x faster                                                     |
| sympy_expand              | 963 ms                                                                 | 953 ms: 1.01x faster                                                     |
| logging_format            | 11.9 us                                                                | 11.8 us: 1.01x faster                                                    |
| bpe_tokeniser             | 5.06 sec                                                               | 5.00 sec: 1.01x faster                                                   |
| subparsers                | 31.6 ms                                                                | 31.2 ms: 1.01x faster                                                    |
| pycparser                 | 1.54 sec                                                               | 1.52 sec: 1.01x faster                                                   |
| sympy_str                 | 481 ms                                                                 | 476 ms: 1.01x faster                                                     |
| sympy_integrate           | 29.7 ms                                                                | 29.4 ms: 1.01x faster                                                    |
| 2to3                      | 369 ms                                                                 | 366 ms: 1.01x faster                                                     |
| async_tree_none_tg        | 361 ms                                                                 | 358 ms: 1.01x faster                                                     |
| fannkuch                  | 496 ms                                                                 | 492 ms: 1.01x faster                                                     |
| xml_etree_iterparse       | 91.8 ms                                                                | 91.1 ms: 1.01x faster                                                    |
| scimark_fft               | 405 ms                                                                 | 402 ms: 1.01x faster                                                     |
| generators                | 38.3 ms                                                                | 38.1 ms: 1.01x faster                                                    |
| shortest_path             | 549 ms                                                                 | 546 ms: 1.01x faster                                                     |
| async_tree_none           | 389 ms                                                                 | 387 ms: 1.01x faster                                                     |
| sympy_sum                 | 352 ms                                                                 | 350 ms: 1.01x faster                                                     |
| python_startup_no_site    | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                    |
| sphinx                    | 1.19 sec                                                               | 1.19 sec: 1.01x faster                                                   |
| python_startup            | 17.5 ms                                                                | 17.4 ms: 1.00x faster                                                    |
| k_core                    | 2.43 sec                                                               | 2.42 sec: 1.00x faster                                                   |
| asyncio_websockets        | 520 ms                                                                 | 517 ms: 1.00x faster                                                     |
| sqlalchemy_declarative    | 204 ms                                                                 | 203 ms: 1.00x faster                                                     |
| bench_mp_pool             | 109 ms                                                                 | 109 ms: 1.00x faster                                                     |
| chaos                     | 105 ms                                                                 | 105 ms: 1.01x slower                                                     |
| pidigits                  | 181 ms                                                                 | 182 ms: 1.01x slower                                                     |
| xml_etree_parse           | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| pathlib                   | 20.3 ms                                                                | 20.4 ms: 1.01x slower                                                    |
| comprehensions            | 27.3 us                                                                | 27.5 us: 1.01x slower                                                    |
| scimark_monte_carlo       | 119 ms                                                                 | 120 ms: 1.01x slower                                                     |
| regex_v8                  | 24.7 ms                                                                | 24.9 ms: 1.01x slower                                                    |
| html5lib                  | 97.6 ms                                                                | 98.8 ms: 1.01x slower                                                    |
| mdp                       | 2.79 sec                                                               | 2.84 sec: 1.02x slower                                                   |
| json_dumps                | 14.2 ms                                                                | 14.5 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult   | 5.75 ms                                                                | 5.93 ms: 1.03x slower                                                    |
| regex_effbot              | 2.81 ms                                                                | 2.90 ms: 1.04x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (17): pylint, typing_runtime_protocols, sqlite_synth, sqlalchemy_imperative, async_tree_io, pyflate, async_tree_memoization, coverage, json, async_tree_cpu_io_mixed, bench_thread_pool, tomli_loads, django_template, async_generators, docutils, async_tree_cpu_io_mixed_tg, connected_components

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x