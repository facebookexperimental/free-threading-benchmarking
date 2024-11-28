# Results vs. base

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: 6e2f5fe
- commit date: 2024-11-28
- overall geometric mean: 1.007x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 382 ms                                                                 | 377 ms: 1.01x faster                                                     |
| docutils       | 3.22 sec                                                               | 3.19 sec: 1.01x faster                                                   |
| html5lib       | 103 ms                                                                 | 101 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 637 ms                                                                 | 627 ms: 1.02x faster                                                     |
| async_generators           | 472 ms                                                                 | 469 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed    | 661 ms                                                                 | 657 ms: 1.01x faster                                                     |
| async_tree_none            | 402 ms                                                                 | 400 ms: 1.01x faster                                                     |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                                     |
| coroutines                 | 27.8 ms                                                                | 28.2 ms: 1.01x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_io_tg, async_tree_memoization, async_tree_none_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 143 ms                                                                 | 139 ms: 1.03x faster                                                     |
| float          | 143 ms                                                                 | 144 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.89 ms                                                                | 2.77 ms: 1.04x faster                                                    |
| regex_compile  | 196 ms                                                                 | 194 ms: 1.01x faster                                                     |
| regex_dna      | 181 ms                                                                 | 187 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|--------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads        | 2.93 sec                                                               | 2.75 sec: 1.07x faster                                                   |
| pickle_pure_python | 556 us                                                                 | 549 us: 1.01x faster                                                     |
| xml_etree_generate | 103 ms                                                                 | 102 ms: 1.00x faster                                                     |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (6): xml_etree_parse, json_dumps, unpickle_pure_python, xml_etree_process, xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.5 ms: 1.00x faster                                                    |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 34.3 ms                                                                | 33.6 ms: 1.02x faster                                                    |
| genshi_xml      | 68.3 ms                                                                | 67.2 ms: 1.02x faster                                                    |
| mako            | 19.6 ms                                                                | 19.8 ms: 1.01x slower                                                    |
| django_template | 55.1 ms                                                                | 55.7 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.52 ms                                                                | 3.29 ms: 1.07x faster                                                    |
| tomli_loads                | 2.93 sec                                                               | 2.75 sec: 1.07x faster                                                   |
| crypto_pyaes               | 104 ms                                                                 | 98.6 ms: 1.05x faster                                                    |
| hexiom                     | 11.5 ms                                                                | 11.0 ms: 1.05x faster                                                    |
| regex_effbot               | 2.89 ms                                                                | 2.77 ms: 1.04x faster                                                    |
| scimark_lu                 | 203 ms                                                                 | 195 ms: 1.04x faster                                                     |
| richards_super             | 104 ms                                                                 | 99.7 ms: 1.04x faster                                                    |
| nqueens                    | 107 ms                                                                 | 103 ms: 1.04x faster                                                     |
| raytrace                   | 622 ms                                                                 | 599 ms: 1.04x faster                                                     |
| chaos                      | 116 ms                                                                 | 112 ms: 1.03x faster                                                     |
| nbody                      | 143 ms                                                                 | 139 ms: 1.03x faster                                                     |
| fannkuch                   | 534 ms                                                                 | 521 ms: 1.03x faster                                                     |
| scimark_monte_carlo        | 124 ms                                                                 | 121 ms: 1.03x faster                                                     |
| create_gc_cycles           | 1.86 ms                                                                | 1.82 ms: 1.02x faster                                                    |
| richards                   | 85.6 ms                                                                | 83.6 ms: 1.02x faster                                                    |
| sqlglot_transpile          | 3.11 ms                                                                | 3.04 ms: 1.02x faster                                                    |
| go                         | 287 ms                                                                 | 281 ms: 1.02x faster                                                     |
| html5lib                   | 103 ms                                                                 | 101 ms: 1.02x faster                                                     |
| sqlite_synth               | 2.35 us                                                                | 2.30 us: 1.02x faster                                                    |
| genshi_text                | 34.3 ms                                                                | 33.6 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg | 637 ms                                                                 | 627 ms: 1.02x faster                                                     |
| genshi_xml                 | 68.3 ms                                                                | 67.2 ms: 1.02x faster                                                    |
| 2to3                       | 382 ms                                                                 | 377 ms: 1.01x faster                                                     |
| pickle_pure_python         | 556 us                                                                 | 549 us: 1.01x faster                                                     |
| regex_compile              | 196 ms                                                                 | 194 ms: 1.01x faster                                                     |
| deltablue                  | 8.89 ms                                                                | 8.80 ms: 1.01x faster                                                    |
| docutils                   | 3.22 sec                                                               | 3.19 sec: 1.01x faster                                                   |
| pprint_pformat             | 2.23 sec                                                               | 2.22 sec: 1.01x faster                                                   |
| scimark_sor                | 243 ms                                                                 | 242 ms: 1.01x faster                                                     |
| logging_silent             | 201 ns                                                                 | 200 ns: 1.01x faster                                                     |
| mdp                        | 2.93 sec                                                               | 2.91 sec: 1.01x faster                                                   |
| pprint_safe_repr           | 1.08 sec                                                               | 1.07 sec: 1.01x faster                                                   |
| async_generators           | 472 ms                                                                 | 469 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed    | 661 ms                                                                 | 657 ms: 1.01x faster                                                     |
| async_tree_none            | 402 ms                                                                 | 400 ms: 1.01x faster                                                     |
| many_optionals             | 1.38 ms                                                                | 1.37 ms: 1.01x faster                                                    |
| k_core                     | 2.47 sec                                                               | 2.45 sec: 1.00x faster                                                   |
| sympy_expand               | 986 ms                                                                 | 982 ms: 1.00x faster                                                     |
| xml_etree_generate         | 103 ms                                                                 | 102 ms: 1.00x faster                                                     |
| bpe_tokeniser              | 5.56 sec                                                               | 5.55 sec: 1.00x faster                                                   |
| python_startup             | 17.5 ms                                                                | 17.5 ms: 1.00x faster                                                    |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                    |
| deepcopy_memo              | 45.8 us                                                                | 45.9 us: 1.00x slower                                                    |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                                     |
| scimark_fft                | 400 ms                                                                 | 402 ms: 1.01x slower                                                     |
| float                      | 143 ms                                                                 | 144 ms: 1.01x slower                                                     |
| generators                 | 39.2 ms                                                                | 39.4 ms: 1.01x slower                                                    |
| comprehensions             | 29.0 us                                                                | 29.2 us: 1.01x slower                                                    |
| sqlglot_normalize          | 149 ms                                                                 | 150 ms: 1.01x slower                                                     |
| subparsers                 | 33.2 ms                                                                | 33.4 ms: 1.01x slower                                                    |
| pyflate                    | 736 ms                                                                 | 741 ms: 1.01x slower                                                     |
| deepcopy_reduce            | 3.72 us                                                                | 3.76 us: 1.01x slower                                                    |
| mako                       | 19.6 ms                                                                | 19.8 ms: 1.01x slower                                                    |
| django_template            | 55.1 ms                                                                | 55.7 ms: 1.01x slower                                                    |
| coroutines                 | 27.8 ms                                                                | 28.2 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 213 us                                                                 | 217 us: 1.02x slower                                                     |
| scimark_sparse_mat_mult    | 5.82 ms                                                                | 5.99 ms: 1.03x slower                                                    |
| regex_dna                  | 181 ms                                                                 | 187 ms: 1.04x slower                                                     |
| spectral_norm              | 130 ms                                                                 | 135 ms: 1.04x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (35): xml_etree_parse, coverage, async_tree_memoization_tg, async_tree_io_tg, sqlglot_parse, bench_mp_pool, json_dumps, sympy_integrate, unpickle_pure_python, async_tree_memoization, xml_etree_process, sphinx, xml_etree_iterparse, dulwich_log, connected_components, sympy_sum, pylint, shortest_path, sympy_str, json_loads, telco, pidigits, async_tree_none_tg, logging_format, async_tree_io, json, sqlglot_optimize, thrift, bench_thread_pool, deepcopy, pycparser, pathlib, logging_simple, regex_v8, meteor_contest

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x