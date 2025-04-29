# Results vs. base

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.000x slower
- HPT reliability: 97.70%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                                 | 279 ms: 1.01x faster                                                              |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                      |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 508 ms                                                                 | 503 ms: 1.01x faster                                                              |
| async_generators        | 366 ms                                                                 | 368 ms: 1.01x slower                                                              |
| coroutines              | 22.4 ms                                                                | 23.5 ms: 1.05x slower                                                             |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                                      |

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none_tg, async_tree_none, async_tree_memoization_tg, async_tree_io, asyncio_websockets, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 67.7 ms                                                                | 66.8 ms: 1.01x faster                                                             |
| nbody          | 109 ms                                                                 | 110 ms: 1.00x slower                                                              |
| pidigits       | 190 ms                                                                 | 199 ms: 1.05x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_dna      | 172 ms                                                                 | 177 ms: 1.03x slower                                                              |
| regex_effbot   | 2.67 ms                                                                | 2.78 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                      |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_process    | 67.0 ms                                                                | 66.1 ms: 1.01x faster                                                             |
| json_dumps           | 12.9 ms                                                                | 12.7 ms: 1.01x faster                                                             |
| xml_etree_generate   | 93.3 ms                                                                | 92.7 ms: 1.01x faster                                                             |
| unpickle_pure_python | 227 us                                                                 | 226 us: 1.01x faster                                                              |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                      |

Benchmark hidden because not significant (5): xml_etree_parse, pickle_pure_python, tomli_loads, xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 15.6 ms                                                                | 15.4 ms: 1.01x faster                                                             |
| python_startup_no_site | 9.29 ms                                                                | 9.19 ms: 1.01x faster                                                             |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako            | 15.5 ms                                                                | 15.4 ms: 1.01x faster                                                             |
| django_template | 40.1 ms                                                                | 39.7 ms: 1.01x faster                                                             |
| genshi_text     | 26.1 ms                                                                | 26.0 ms: 1.00x faster                                                             |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                                      |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|--------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| deltablue                | 3.71 ms                                                                | 3.53 ms: 1.05x faster                                                             |
| pyflate                  | 473 ms                                                                 | 455 ms: 1.04x faster                                                              |
| pathlib                  | 19.6 ms                                                                | 19.2 ms: 1.02x faster                                                             |
| bench_mp_pool            | 95.8 ms                                                                | 94.1 ms: 1.02x faster                                                             |
| richards                 | 50.2 ms                                                                | 49.5 ms: 1.01x faster                                                             |
| python_startup           | 15.6 ms                                                                | 15.4 ms: 1.01x faster                                                             |
| scimark_sor              | 119 ms                                                                 | 118 ms: 1.01x faster                                                              |
| float                    | 67.7 ms                                                                | 66.8 ms: 1.01x faster                                                             |
| xml_etree_process        | 67.0 ms                                                                | 66.1 ms: 1.01x faster                                                             |
| chaos                    | 61.3 ms                                                                | 60.6 ms: 1.01x faster                                                             |
| 2to3                     | 282 ms                                                                 | 279 ms: 1.01x faster                                                              |
| python_startup_no_site   | 9.29 ms                                                                | 9.19 ms: 1.01x faster                                                             |
| async_tree_cpu_io_mixed  | 508 ms                                                                 | 503 ms: 1.01x faster                                                              |
| scimark_fft              | 341 ms                                                                 | 338 ms: 1.01x faster                                                              |
| meteor_contest           | 129 ms                                                                 | 127 ms: 1.01x faster                                                              |
| json_dumps               | 12.9 ms                                                                | 12.7 ms: 1.01x faster                                                             |
| pycparser                | 1.14 sec                                                               | 1.13 sec: 1.01x faster                                                            |
| mako                     | 15.5 ms                                                                | 15.4 ms: 1.01x faster                                                             |
| django_template          | 40.1 ms                                                                | 39.7 ms: 1.01x faster                                                             |
| many_optionals           | 1.11 ms                                                                | 1.10 ms: 1.01x faster                                                             |
| raytrace                 | 290 ms                                                                 | 288 ms: 1.01x faster                                                              |
| xml_etree_generate       | 93.3 ms                                                                | 92.7 ms: 1.01x faster                                                             |
| coverage                 | 110 ms                                                                 | 109 ms: 1.01x faster                                                              |
| richards_super           | 57.7 ms                                                                | 57.4 ms: 1.01x faster                                                             |
| dulwich_log              | 70.9 ms                                                                | 70.5 ms: 1.01x faster                                                             |
| unpickle_pure_python     | 227 us                                                                 | 226 us: 1.01x faster                                                              |
| sqlglot_v2_parse         | 1.46 ms                                                                | 1.46 ms: 1.01x faster                                                             |
| sqlalchemy_declarative   | 153 ms                                                                 | 153 ms: 1.00x faster                                                              |
| genshi_text              | 26.1 ms                                                                | 26.0 ms: 1.00x faster                                                             |
| nqueens                  | 85.7 ms                                                                | 85.4 ms: 1.00x faster                                                             |
| deepcopy_memo            | 34.7 us                                                                | 34.5 us: 1.00x faster                                                             |
| k_core                   | 2.24 sec                                                               | 2.23 sec: 1.00x faster                                                            |
| bench_thread_pool        | 3.13 ms                                                                | 3.13 ms: 1.00x slower                                                             |
| nbody                    | 109 ms                                                                 | 110 ms: 1.00x slower                                                              |
| gc_traversal             | 1.78 ms                                                                | 1.78 ms: 1.00x slower                                                             |
| deepcopy_reduce          | 2.98 us                                                                | 2.99 us: 1.00x slower                                                             |
| sympy_str                | 313 ms                                                                 | 315 ms: 1.01x slower                                                              |
| sympy_expand             | 526 ms                                                                 | 530 ms: 1.01x slower                                                              |
| async_generators         | 366 ms                                                                 | 368 ms: 1.01x slower                                                              |
| create_gc_cycles         | 1.35 ms                                                                | 1.36 ms: 1.01x slower                                                             |
| deepcopy                 | 289 us                                                                 | 291 us: 1.01x slower                                                              |
| pprint_safe_repr         | 767 ms                                                                 | 774 ms: 1.01x slower                                                              |
| hexiom                   | 6.65 ms                                                                | 6.71 ms: 1.01x slower                                                             |
| logging_silent           | 104 ns                                                                 | 105 ns: 1.01x slower                                                              |
| typing_runtime_protocols | 189 us                                                                 | 191 us: 1.01x slower                                                              |
| connected_components     | 475 ms                                                                 | 482 ms: 1.01x slower                                                              |
| comprehensions           | 19.1 us                                                                | 19.4 us: 1.02x slower                                                             |
| pprint_pformat           | 1.58 sec                                                               | 1.60 sec: 1.02x slower                                                            |
| generators               | 30.1 ms                                                                | 30.8 ms: 1.02x slower                                                             |
| spectral_norm            | 101 ms                                                                 | 104 ms: 1.03x slower                                                              |
| logging_simple           | 6.96 us                                                                | 7.14 us: 1.03x slower                                                             |
| regex_dna                | 172 ms                                                                 | 177 ms: 1.03x slower                                                              |
| regex_effbot             | 2.67 ms                                                                | 2.78 ms: 1.04x slower                                                             |
| logging_format           | 7.75 us                                                                | 8.07 us: 1.04x slower                                                             |
| pidigits                 | 190 ms                                                                 | 199 ms: 1.05x slower                                                              |
| coroutines               | 22.4 ms                                                                | 23.5 ms: 1.05x slower                                                             |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                                      |

Benchmark hidden because not significant (39): html5lib, async_tree_cpu_io_mixed_tg, sqlglot_v2_optimize, async_tree_memoization, sqlglot_v2_normalize, async_tree_none_tg, async_tree_none, genshi_xml, mdp, async_tree_memoization_tg, scimark_monte_carlo, xml_etree_parse, regex_compile, fannkuch, crypto_pyaes, pylint, async_tree_io, sqlglot_v2_transpile, sphinx, sqlalchemy_imperative, pickle_pure_python, asyncio_websockets, sympy_integrate, go, subparsers, docutils, bpe_tokeniser, sympy_sum, regex_v8, scimark_lu, async_tree_io_tg, tomli_loads, shortest_path, scimark_sparse_mat_mult, json, xml_etree_iterparse, sqlite_synth, telco, json_loads

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 97.70% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x