# Results vs. base

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 7b72e7b
- commit date: 2024-12-17
- overall geometric mean: 1.008x faster
- HPT reliability: 99.45%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 369 ms                                                                 | 368 ms: 1.00x faster                                                     |
| html5lib       | 97.6 ms                                                                | 96.9 ms: 1.01x faster                                                    |
| sphinx         | 1.19 sec                                                               | 1.19 sec: 1.00x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                 | 25.0 ms                                                                | 24.4 ms: 1.03x faster                                                    |
| async_tree_io_tg           | 838 ms                                                                 | 833 ms: 1.01x faster                                                     |
| async_generators           | 451 ms                                                                 | 454 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed_tg | 621 ms                                                                 | 625 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, asyncio_websockets, async_tree_memoization, async_tree_io, async_tree_none, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 138 ms                                                                 | 131 ms: 1.06x faster                                                     |
| float          | 143 ms                                                                 | 139 ms: 1.03x faster                                                     |
| pidigits       | 181 ms                                                                 | 181 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 193 ms                                                                 | 185 ms: 1.04x faster                                                     |
| regex_compile  | 181 ms                                                                 | 178 ms: 1.02x faster                                                     |
| regex_effbot   | 2.81 ms                                                                | 2.83 ms: 1.01x slower                                                    |
| regex_v8       | 24.7 ms                                                                | 25.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_process    | 80.2 ms                                                                | 78.2 ms: 1.03x faster                                                    |
| xml_etree_generate   | 98.8 ms                                                                | 97.5 ms: 1.01x faster                                                    |
| json_loads           | 28.9 us                                                                | 28.6 us: 1.01x faster                                                    |
| unpickle_pure_python | 339 us                                                                 | 335 us: 1.01x faster                                                     |
| tomli_loads          | 2.66 sec                                                               | 2.67 sec: 1.00x slower                                                   |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_pure_python, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| python_startup         | 17.5 ms                                                                | 17.5 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text    | 32.1 ms                                                                | 32.0 ms: 1.00x faster                                                    |
| genshi_xml     | 64.1 ms                                                                | 65.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2+-7015485 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| scimark_lu                 | 187 ms                                                                 | 156 ms: 1.20x faster                                                     |
| gc_traversal               | 3.54 ms                                                                | 3.21 ms: 1.10x faster                                                    |
| nbody                      | 138 ms                                                                 | 131 ms: 1.06x faster                                                     |
| scimark_sor                | 237 ms                                                                 | 225 ms: 1.05x faster                                                     |
| regex_dna                  | 193 ms                                                                 | 185 ms: 1.04x faster                                                     |
| deltablue                  | 8.33 ms                                                                | 8.08 ms: 1.03x faster                                                    |
| create_gc_cycles           | 1.86 ms                                                                | 1.80 ms: 1.03x faster                                                    |
| float                      | 143 ms                                                                 | 139 ms: 1.03x faster                                                     |
| coroutines                 | 25.0 ms                                                                | 24.4 ms: 1.03x faster                                                    |
| xml_etree_process          | 80.2 ms                                                                | 78.2 ms: 1.03x faster                                                    |
| typing_runtime_protocols   | 205 us                                                                 | 200 us: 1.03x faster                                                     |
| thrift                     | 1.19 ms                                                                | 1.16 ms: 1.02x faster                                                    |
| pprint_pformat             | 2.05 sec                                                               | 2.01 sec: 1.02x faster                                                   |
| dulwich_log                | 97.0 ms                                                                | 95.1 ms: 1.02x faster                                                    |
| subparsers                 | 31.6 ms                                                                | 31.0 ms: 1.02x faster                                                    |
| telco                      | 8.87 ms                                                                | 8.71 ms: 1.02x faster                                                    |
| regex_compile              | 181 ms                                                                 | 178 ms: 1.02x faster                                                     |
| xml_etree_generate         | 98.8 ms                                                                | 97.5 ms: 1.01x faster                                                    |
| sqlglot_parse              | 2.62 ms                                                                | 2.59 ms: 1.01x faster                                                    |
| pprint_safe_repr           | 986 ms                                                                 | 974 ms: 1.01x faster                                                     |
| json_loads                 | 28.9 us                                                                | 28.6 us: 1.01x faster                                                    |
| unpickle_pure_python       | 339 us                                                                 | 335 us: 1.01x faster                                                     |
| many_optionals             | 1.31 ms                                                                | 1.29 ms: 1.01x faster                                                    |
| sqlglot_transpile          | 3.03 ms                                                                | 3.00 ms: 1.01x faster                                                    |
| bpe_tokeniser              | 5.06 sec                                                               | 5.00 sec: 1.01x faster                                                   |
| logging_silent             | 190 ns                                                                 | 188 ns: 1.01x faster                                                     |
| json                       | 5.12 ms                                                                | 5.06 ms: 1.01x faster                                                    |
| hexiom                     | 9.91 ms                                                                | 9.81 ms: 1.01x faster                                                    |
| raytrace                   | 560 ms                                                                 | 555 ms: 1.01x faster                                                     |
| sympy_integrate            | 29.7 ms                                                                | 29.4 ms: 1.01x faster                                                    |
| sqlite_synth               | 2.30 us                                                                | 2.28 us: 1.01x faster                                                    |
| html5lib                   | 97.6 ms                                                                | 96.9 ms: 1.01x faster                                                    |
| sympy_str                  | 481 ms                                                                 | 478 ms: 1.01x faster                                                     |
| go                         | 276 ms                                                                 | 274 ms: 1.01x faster                                                     |
| async_tree_io_tg           | 838 ms                                                                 | 833 ms: 1.01x faster                                                     |
| sympy_expand               | 963 ms                                                                 | 958 ms: 1.01x faster                                                     |
| sympy_sum                  | 352 ms                                                                 | 350 ms: 1.01x faster                                                     |
| mdp                        | 2.79 sec                                                               | 2.78 sec: 1.00x faster                                                   |
| crypto_pyaes               | 93.3 ms                                                                | 92.9 ms: 1.00x faster                                                    |
| sphinx                     | 1.19 sec                                                               | 1.19 sec: 1.00x faster                                                   |
| genshi_text                | 32.1 ms                                                                | 32.0 ms: 1.00x faster                                                    |
| deepcopy                   | 332 us                                                                 | 330 us: 1.00x faster                                                     |
| bench_thread_pool          | 3.43 ms                                                                | 3.42 ms: 1.00x faster                                                    |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| python_startup             | 17.5 ms                                                                | 17.5 ms: 1.00x faster                                                    |
| 2to3                       | 369 ms                                                                 | 368 ms: 1.00x faster                                                     |
| tomli_loads                | 2.66 sec                                                               | 2.67 sec: 1.00x slower                                                   |
| deepcopy_memo              | 40.1 us                                                                | 40.2 us: 1.00x slower                                                    |
| pidigits                   | 181 ms                                                                 | 181 ms: 1.00x slower                                                     |
| xml_etree_parse            | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| async_generators           | 451 ms                                                                 | 454 ms: 1.01x slower                                                     |
| nqueens                    | 97.2 ms                                                                | 97.8 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 621 ms                                                                 | 625 ms: 1.01x slower                                                     |
| scimark_sparse_mat_mult    | 5.75 ms                                                                | 5.80 ms: 1.01x slower                                                    |
| regex_effbot               | 2.81 ms                                                                | 2.83 ms: 1.01x slower                                                    |
| chaos                      | 105 ms                                                                 | 105 ms: 1.01x slower                                                     |
| pyflate                    | 692 ms                                                                 | 699 ms: 1.01x slower                                                     |
| connected_components       | 498 ms                                                                 | 504 ms: 1.01x slower                                                     |
| pathlib                    | 20.3 ms                                                                | 20.5 ms: 1.01x slower                                                    |
| logging_format             | 11.9 us                                                                | 12.0 us: 1.01x slower                                                    |
| genshi_xml                 | 64.1 ms                                                                | 65.1 ms: 1.02x slower                                                    |
| logging_simple             | 10.7 us                                                                | 10.9 us: 1.02x slower                                                    |
| regex_v8                   | 24.7 ms                                                                | 25.1 ms: 1.02x slower                                                    |
| generators                 | 38.3 ms                                                                | 39.0 ms: 1.02x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (32): sqlalchemy_imperative, sqlglot_optimize, sqlglot_normalize, async_tree_cpu_io_mixed, xml_etree_iterparse, scimark_fft, scimark_monte_carlo, pickle_pure_python, asyncio_websockets, meteor_contest, mako, pylint, spectral_norm, k_core, async_tree_memoization, deepcopy_reduce, bench_mp_pool, comprehensions, async_tree_io, sqlalchemy_declarative, richards, coverage, docutils, fannkuch, async_tree_none, async_tree_memoization_tg, pycparser, json_dumps, django_template, shortest_path, richards_super, async_tree_none_tg

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 99.45% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x