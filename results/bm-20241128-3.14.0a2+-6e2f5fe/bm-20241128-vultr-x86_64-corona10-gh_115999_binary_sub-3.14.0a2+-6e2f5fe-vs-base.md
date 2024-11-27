# Results vs. base

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: 6e2f5fe
- commit date: 2024-11-28
- overall geometric mean: 1.003x faster
- HPT reliability: 74.95%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 257 ms: 1.00x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.64 sec: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines       | 22.4 ms                                                                | 22.1 ms: 1.01x faster                                                    |
| async_generators | 375 ms                                                                 | 373 ms: 1.01x faster                                                     |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (9): async_tree_io_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none, async_tree_memoization, async_tree_none_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 81.5 ms                                                                | 80.9 ms: 1.01x faster                                                    |
| pidigits       | 220 ms                                                                 | 223 ms: 1.01x slower                                                     |
| nbody          | 94.0 ms                                                                | 95.4 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.66 ms: 1.05x faster                                                    |
| regex_dna      | 180 ms                                                                 | 174 ms: 1.03x faster                                                     |
| regex_v8       | 23.4 ms                                                                | 23.0 ms: 1.02x faster                                                    |
| regex_compile  | 132 ms                                                                 | 130 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_pure_python | 217 us                                                                 | 215 us: 1.01x faster                                                     |
| xml_etree_process    | 61.0 ms                                                                | 60.2 ms: 1.01x faster                                                    |
| xml_etree_generate   | 86.3 ms                                                                | 85.2 ms: 1.01x faster                                                    |
| xml_etree_iterparse  | 98.5 ms                                                                | 97.7 ms: 1.01x faster                                                    |
| pickle_pure_python   | 320 us                                                                 | 318 us: 1.01x faster                                                     |
| xml_etree_parse      | 136 ms                                                                 | 139 ms: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (3): tomli_loads, json_dumps, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| python_startup_no_site | 7.37 ms                                                                | 7.43 ms: 1.01x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 11.8 ms                                                                | 11.5 ms: 1.03x faster                                                    |
| django_template | 36.0 ms                                                                | 35.6 ms: 1.01x faster                                                    |
| genshi_text     | 22.3 ms                                                                | 22.2 ms: 1.00x faster                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot             | 2.78 ms                                                                | 2.66 ms: 1.05x faster                                                    |
| richards                 | 47.4 ms                                                                | 45.8 ms: 1.04x faster                                                    |
| regex_dna                | 180 ms                                                                 | 174 ms: 1.03x faster                                                     |
| richards_super           | 53.9 ms                                                                | 52.4 ms: 1.03x faster                                                    |
| mako                     | 11.8 ms                                                                | 11.5 ms: 1.03x faster                                                    |
| spectral_norm            | 116 ms                                                                 | 114 ms: 1.02x faster                                                     |
| regex_v8                 | 23.4 ms                                                                | 23.0 ms: 1.02x faster                                                    |
| nqueens                  | 80.1 ms                                                                | 78.7 ms: 1.02x faster                                                    |
| deltablue                | 3.31 ms                                                                | 3.26 ms: 1.02x faster                                                    |
| regex_compile            | 132 ms                                                                 | 130 ms: 1.01x faster                                                     |
| unpickle_pure_python     | 217 us                                                                 | 215 us: 1.01x faster                                                     |
| xml_etree_process        | 61.0 ms                                                                | 60.2 ms: 1.01x faster                                                    |
| telco                    | 7.27 ms                                                                | 7.18 ms: 1.01x faster                                                    |
| hexiom                   | 6.07 ms                                                                | 5.99 ms: 1.01x faster                                                    |
| xml_etree_generate       | 86.3 ms                                                                | 85.2 ms: 1.01x faster                                                    |
| subparsers               | 22.3 ms                                                                | 22.1 ms: 1.01x faster                                                    |
| django_template          | 36.0 ms                                                                | 35.6 ms: 1.01x faster                                                    |
| go                       | 122 ms                                                                 | 121 ms: 1.01x faster                                                     |
| typing_runtime_protocols | 160 us                                                                 | 158 us: 1.01x faster                                                     |
| coroutines               | 22.4 ms                                                                | 22.1 ms: 1.01x faster                                                    |
| xml_etree_iterparse      | 98.5 ms                                                                | 97.7 ms: 1.01x faster                                                    |
| pickle_pure_python       | 320 us                                                                 | 318 us: 1.01x faster                                                     |
| scimark_fft              | 341 ms                                                                 | 338 ms: 1.01x faster                                                     |
| async_generators         | 375 ms                                                                 | 373 ms: 1.01x faster                                                     |
| float                    | 81.5 ms                                                                | 80.9 ms: 1.01x faster                                                    |
| pprint_safe_repr         | 723 ms                                                                 | 719 ms: 1.01x faster                                                     |
| pathlib                  | 18.4 ms                                                                | 18.3 ms: 1.01x faster                                                    |
| sympy_integrate          | 20.0 ms                                                                | 19.9 ms: 1.01x faster                                                    |
| genshi_text              | 22.3 ms                                                                | 22.2 ms: 1.00x faster                                                    |
| deepcopy_memo            | 30.3 us                                                                | 30.2 us: 1.00x faster                                                    |
| docutils                 | 2.63 sec                                                               | 2.64 sec: 1.00x slower                                                   |
| 2to3                     | 256 ms                                                                 | 257 ms: 1.00x slower                                                     |
| pylint                   | 269 ms                                                                 | 270 ms: 1.00x slower                                                     |
| sympy_sum                | 153 ms                                                                 | 154 ms: 1.00x slower                                                     |
| chaos                    | 59.2 ms                                                                | 59.5 ms: 1.00x slower                                                    |
| python_startup           | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| bpe_tokeniser            | 4.43 sec                                                               | 4.45 sec: 1.01x slower                                                   |
| raytrace                 | 264 ms                                                                 | 265 ms: 1.01x slower                                                     |
| logging_silent           | 108 ns                                                                 | 108 ns: 1.01x slower                                                     |
| sqlalchemy_declarative   | 126 ms                                                                 | 127 ms: 1.01x slower                                                     |
| many_optionals           | 1.02 ms                                                                | 1.03 ms: 1.01x slower                                                    |
| python_startup_no_site   | 7.37 ms                                                                | 7.43 ms: 1.01x slower                                                    |
| logging_format           | 6.86 us                                                                | 6.92 us: 1.01x slower                                                    |
| scimark_sor              | 133 ms                                                                 | 135 ms: 1.01x slower                                                     |
| sympy_expand             | 462 ms                                                                 | 466 ms: 1.01x slower                                                     |
| crypto_pyaes             | 67.7 ms                                                                | 68.5 ms: 1.01x slower                                                    |
| pidigits                 | 220 ms                                                                 | 223 ms: 1.01x slower                                                     |
| dulwich_log              | 75.3 ms                                                                | 76.4 ms: 1.01x slower                                                    |
| nbody                    | 94.0 ms                                                                | 95.4 ms: 1.01x slower                                                    |
| create_gc_cycles         | 1.93 ms                                                                | 1.96 ms: 1.02x slower                                                    |
| xml_etree_parse          | 136 ms                                                                 | 139 ms: 1.02x slower                                                     |
| scimark_monte_carlo      | 65.1 ms                                                                | 66.4 ms: 1.02x slower                                                    |
| json                     | 4.48 ms                                                                | 4.56 ms: 1.02x slower                                                    |
| fannkuch                 | 384 ms                                                                 | 391 ms: 1.02x slower                                                     |
| deepcopy_reduce          | 2.61 us                                                                | 2.68 us: 1.03x slower                                                    |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (40): async_tree_io_tg, tomli_loads, connected_components, bench_mp_pool, sphinx, shortest_path, thrift, comprehensions, sqlglot_parse, pprint_pformat, mdp, sqlglot_optimize, asyncio_websockets, json_dumps, bench_thread_pool, async_tree_cpu_io_mixed_tg, deepcopy, pyflate, logging_simple, gc_traversal, sqlglot_normalize, pycparser, sqlglot_transpile, async_tree_cpu_io_mixed, scimark_lu, sympy_str, async_tree_memoization_tg, async_tree_none, generators, sqlite_synth, sqlalchemy_imperative, json_loads, genshi_xml, meteor_contest, async_tree_memoization, coverage, async_tree_none_tg, async_tree_io, scimark_sparse_mat_mult, k_core

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 74.95% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x