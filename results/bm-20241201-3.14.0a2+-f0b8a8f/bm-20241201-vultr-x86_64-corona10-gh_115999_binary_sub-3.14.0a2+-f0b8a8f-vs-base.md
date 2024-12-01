# Results vs. base

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: f0b8a8f
- commit date: 2024-12-01
- overall geometric mean: 1.001x faster
- HPT reliability: 83.78%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 258 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 665 ms                                                                 | 567 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed    | 667 ms                                                                 | 569 ms: 1.17x faster                                                     |
| async_tree_io              | 856 ms                                                                 | 839 ms: 1.02x faster                                                     |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                                     |
| coroutines                 | 22.4 ms                                                                | 23.2 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (6): async_tree_io_tg, async_tree_none, async_tree_memoization_tg, async_tree_memoization, asyncio_websockets, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 220 ms                                                                 | 187 ms: 1.18x faster                                                     |
| float          | 81.5 ms                                                                | 80.9 ms: 1.01x faster                                                    |
| nbody          | 94.0 ms                                                                | 96.1 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.69 ms: 1.04x faster                                                    |
| regex_dna      | 180 ms                                                                 | 174 ms: 1.03x faster                                                     |
| regex_v8       | 23.4 ms                                                                | 23.0 ms: 1.02x faster                                                    |
| regex_compile  | 132 ms                                                                 | 137 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_generate   | 86.3 ms                                                                | 86.9 ms: 1.01x slower                                                    |
| xml_etree_parse      | 136 ms                                                                 | 138 ms: 1.01x slower                                                     |
| json_dumps           | 11.4 ms                                                                | 11.5 ms: 1.01x slower                                                    |
| json_loads           | 24.9 us                                                                | 25.3 us: 1.02x slower                                                    |
| unpickle_pure_python | 217 us                                                                 | 221 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (4): tomli_loads, xml_etree_iterparse, xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| python_startup_no_site | 7.37 ms                                                                | 7.40 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 36.0 ms                                                                | 35.6 ms: 1.01x faster                                                    |
| genshi_xml      | 50.5 ms                                                                | 50.1 ms: 1.01x faster                                                    |
| mako            | 11.8 ms                                                                | 12.0 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2+-58e334e | bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-f0b8a8f |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 220 ms                                                                 | 187 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg | 665 ms                                                                 | 567 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed    | 667 ms                                                                 | 569 ms: 1.17x faster                                                     |
| regex_effbot               | 2.78 ms                                                                | 2.69 ms: 1.04x faster                                                    |
| regex_dna                  | 180 ms                                                                 | 174 ms: 1.03x faster                                                     |
| fannkuch                   | 384 ms                                                                 | 373 ms: 1.03x faster                                                     |
| async_tree_io              | 856 ms                                                                 | 839 ms: 1.02x faster                                                     |
| spectral_norm              | 116 ms                                                                 | 113 ms: 1.02x faster                                                     |
| regex_v8                   | 23.4 ms                                                                | 23.0 ms: 1.02x faster                                                    |
| django_template            | 36.0 ms                                                                | 35.6 ms: 1.01x faster                                                    |
| genshi_xml                 | 50.5 ms                                                                | 50.1 ms: 1.01x faster                                                    |
| float                      | 81.5 ms                                                                | 80.9 ms: 1.01x faster                                                    |
| scimark_fft                | 341 ms                                                                 | 338 ms: 1.01x faster                                                     |
| nqueens                    | 80.1 ms                                                                | 79.6 ms: 1.01x faster                                                    |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                                     |
| pyflate                    | 449 ms                                                                 | 447 ms: 1.00x faster                                                     |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| pylint                     | 269 ms                                                                 | 270 ms: 1.00x slower                                                     |
| many_optionals             | 1.02 ms                                                                | 1.02 ms: 1.00x slower                                                    |
| sqlalchemy_declarative     | 126 ms                                                                 | 127 ms: 1.00x slower                                                     |
| python_startup_no_site     | 7.37 ms                                                                | 7.40 ms: 1.00x slower                                                    |
| comprehensions             | 17.4 us                                                                | 17.5 us: 1.01x slower                                                    |
| sqlglot_normalize          | 107 ms                                                                 | 108 ms: 1.01x slower                                                     |
| mdp                        | 2.35 sec                                                               | 2.36 sec: 1.01x slower                                                   |
| 2to3                       | 256 ms                                                                 | 258 ms: 1.01x slower                                                     |
| pathlib                    | 18.4 ms                                                                | 18.6 ms: 1.01x slower                                                    |
| sqlglot_optimize           | 53.7 ms                                                                | 54.0 ms: 1.01x slower                                                    |
| xml_etree_generate         | 86.3 ms                                                                | 86.9 ms: 1.01x slower                                                    |
| crypto_pyaes               | 67.7 ms                                                                | 68.2 ms: 1.01x slower                                                    |
| telco                      | 7.27 ms                                                                | 7.33 ms: 1.01x slower                                                    |
| richards                   | 47.4 ms                                                                | 47.8 ms: 1.01x slower                                                    |
| sqlglot_transpile          | 1.60 ms                                                                | 1.61 ms: 1.01x slower                                                    |
| deepcopy_memo              | 30.3 us                                                                | 30.6 us: 1.01x slower                                                    |
| xml_etree_parse            | 136 ms                                                                 | 138 ms: 1.01x slower                                                     |
| chaos                      | 59.2 ms                                                                | 59.8 ms: 1.01x slower                                                    |
| scimark_lu                 | 115 ms                                                                 | 116 ms: 1.01x slower                                                     |
| sqlglot_parse              | 1.30 ms                                                                | 1.32 ms: 1.01x slower                                                    |
| pprint_pformat             | 1.47 sec                                                               | 1.48 sec: 1.01x slower                                                   |
| richards_super             | 53.9 ms                                                                | 54.5 ms: 1.01x slower                                                    |
| hexiom                     | 6.07 ms                                                                | 6.14 ms: 1.01x slower                                                    |
| dulwich_log                | 75.3 ms                                                                | 76.2 ms: 1.01x slower                                                    |
| json_dumps                 | 11.4 ms                                                                | 11.5 ms: 1.01x slower                                                    |
| meteor_contest             | 99.7 ms                                                                | 101 ms: 1.01x slower                                                     |
| gc_traversal               | 3.95 ms                                                                | 4.01 ms: 1.01x slower                                                    |
| scimark_sor                | 133 ms                                                                 | 135 ms: 1.02x slower                                                     |
| logging_simple             | 6.19 us                                                                | 6.29 us: 1.02x slower                                                    |
| json_loads                 | 24.9 us                                                                | 25.3 us: 1.02x slower                                                    |
| unpickle_pure_python       | 217 us                                                                 | 221 us: 1.02x slower                                                     |
| go                         | 122 ms                                                                 | 124 ms: 1.02x slower                                                     |
| json                       | 4.48 ms                                                                | 4.56 ms: 1.02x slower                                                    |
| mako                       | 11.8 ms                                                                | 12.0 ms: 1.02x slower                                                    |
| nbody                      | 94.0 ms                                                                | 96.1 ms: 1.02x slower                                                    |
| scimark_monte_carlo        | 65.1 ms                                                                | 66.6 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.20 us                                                                | 2.25 us: 1.02x slower                                                    |
| logging_silent             | 108 ns                                                                 | 111 ns: 1.03x slower                                                     |
| raytrace                   | 264 ms                                                                 | 271 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult    | 4.49 ms                                                                | 4.61 ms: 1.03x slower                                                    |
| logging_format             | 6.86 us                                                                | 7.07 us: 1.03x slower                                                    |
| deltablue                  | 3.31 ms                                                                | 3.42 ms: 1.03x slower                                                    |
| regex_compile              | 132 ms                                                                 | 137 ms: 1.03x slower                                                     |
| coroutines                 | 22.4 ms                                                                | 23.2 ms: 1.04x slower                                                    |
| generators                 | 29.0 ms                                                                | 31.0 ms: 1.07x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (33): async_tree_io_tg, tomli_loads, async_tree_none, async_tree_memoization_tg, async_tree_memoization, typing_runtime_protocols, subparsers, sphinx, sympy_str, deepcopy, bench_thread_pool, docutils, sympy_integrate, connected_components, coverage, thrift, sympy_sum, deepcopy_reduce, asyncio_websockets, bench_mp_pool, async_tree_none_tg, xml_etree_iterparse, xml_etree_process, pickle_pure_python, bpe_tokeniser, pycparser, sympy_expand, pprint_safe_repr, shortest_path, genshi_text, create_gc_cycles, sqlalchemy_imperative, k_core

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 83.78% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x