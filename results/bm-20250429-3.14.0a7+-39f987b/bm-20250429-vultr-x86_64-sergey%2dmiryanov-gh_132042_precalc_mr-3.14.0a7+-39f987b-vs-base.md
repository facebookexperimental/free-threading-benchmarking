# Results vs. base

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.001x slower
- HPT reliability: 61.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 245 ms: 1.01x faster                                                              |
| docutils       | 2.53 sec                                                               | 2.51 sec: 1.01x faster                                                            |
| sphinx         | 977 ms                                                                 | 968 ms: 1.01x faster                                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_generators           | 332 ms                                                                 | 326 ms: 1.02x faster                                                              |
| coroutines                 | 23.5 ms                                                                | 23.1 ms: 1.02x faster                                                             |
| async_tree_memoization     | 307 ms                                                                 | 309 ms: 1.01x slower                                                              |
| async_tree_cpu_io_mixed    | 513 ms                                                                 | 560 ms: 1.09x slower                                                              |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 553 ms: 1.10x slower                                                              |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                                      |

Benchmark hidden because not significant (6): async_tree_none, async_tree_io_tg, asyncio_websockets, async_tree_none_tg, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| nbody          | 86.7 ms                                                                | 89.7 ms: 1.03x slower                                                             |
| pidigits       | 190 ms                                                                 | 226 ms: 1.19x slower                                                              |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                                      |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_dna      | 183 ms                                                                 | 172 ms: 1.06x faster                                                              |
| regex_effbot   | 2.80 ms                                                                | 2.70 ms: 1.04x faster                                                             |
| regex_v8       | 22.1 ms                                                                | 21.5 ms: 1.03x faster                                                             |
| regex_compile  | 123 ms                                                                 | 122 ms: 1.00x faster                                                              |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 11.5 ms                                                                | 11.3 ms: 1.01x faster                                                             |
| xml_etree_parse      | 131 ms                                                                 | 131 ms: 1.01x faster                                                              |
| pickle_pure_python   | 303 us                                                                 | 302 us: 1.00x faster                                                              |
| unpickle_pure_python | 209 us                                                                 | 210 us: 1.00x slower                                                              |
| tomli_loads          | 1.85 sec                                                               | 1.87 sec: 1.01x slower                                                            |
| json_loads           | 27.6 us                                                                | 28.2 us: 1.02x slower                                                             |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                                      |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                | 14.6 ms: 1.02x faster                                                             |
| python_startup_no_site | 7.29 ms                                                                | 7.17 ms: 1.02x faster                                                             |
| Geometric mean         | (ref)                                                                  | 1.02x faster                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako           | 12.0 ms                                                                | 11.8 ms: 1.02x faster                                                             |
| genshi_xml     | 48.2 ms                                                                | 47.7 ms: 1.01x faster                                                             |
| genshi_text    | 20.7 ms                                                                | 20.9 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                      |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-vultr-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| scimark_sparse_mat_mult    | 4.63 ms                                                                | 4.31 ms: 1.07x faster                                                             |
| regex_dna                  | 183 ms                                                                 | 172 ms: 1.06x faster                                                              |
| regex_effbot               | 2.80 ms                                                                | 2.70 ms: 1.04x faster                                                             |
| regex_v8                   | 22.1 ms                                                                | 21.5 ms: 1.03x faster                                                             |
| meteor_contest             | 101 ms                                                                 | 98.2 ms: 1.03x faster                                                             |
| generators                 | 28.0 ms                                                                | 27.3 ms: 1.02x faster                                                             |
| scimark_fft                | 319 ms                                                                 | 312 ms: 1.02x faster                                                              |
| crypto_pyaes               | 68.9 ms                                                                | 67.4 ms: 1.02x faster                                                             |
| hexiom                     | 5.76 ms                                                                | 5.64 ms: 1.02x faster                                                             |
| async_generators           | 332 ms                                                                 | 326 ms: 1.02x faster                                                              |
| bench_mp_pool              | 88.4 ms                                                                | 86.7 ms: 1.02x faster                                                             |
| mako                       | 12.0 ms                                                                | 11.8 ms: 1.02x faster                                                             |
| python_startup             | 14.9 ms                                                                | 14.6 ms: 1.02x faster                                                             |
| python_startup_no_site     | 7.29 ms                                                                | 7.17 ms: 1.02x faster                                                             |
| coroutines                 | 23.5 ms                                                                | 23.1 ms: 1.02x faster                                                             |
| gc_traversal               | 4.57 ms                                                                | 4.50 ms: 1.02x faster                                                             |
| json_dumps                 | 11.5 ms                                                                | 11.3 ms: 1.01x faster                                                             |
| pycparser                  | 1.10 sec                                                               | 1.09 sec: 1.01x faster                                                            |
| 2to3                       | 248 ms                                                                 | 245 ms: 1.01x faster                                                              |
| comprehensions             | 16.7 us                                                                | 16.4 us: 1.01x faster                                                             |
| genshi_xml                 | 48.2 ms                                                                | 47.7 ms: 1.01x faster                                                             |
| deltablue                  | 3.24 ms                                                                | 3.21 ms: 1.01x faster                                                             |
| deepcopy_reduce            | 2.60 us                                                                | 2.58 us: 1.01x faster                                                             |
| sphinx                     | 977 ms                                                                 | 968 ms: 1.01x faster                                                              |
| sqlalchemy_declarative     | 130 ms                                                                 | 129 ms: 1.01x faster                                                              |
| deepcopy_memo              | 28.8 us                                                                | 28.6 us: 1.01x faster                                                             |
| scimark_lu                 | 111 ms                                                                 | 110 ms: 1.01x faster                                                              |
| docutils                   | 2.53 sec                                                               | 2.51 sec: 1.01x faster                                                            |
| sqlglot_v2_optimize        | 49.9 ms                                                                | 49.6 ms: 1.01x faster                                                             |
| xml_etree_parse            | 131 ms                                                                 | 131 ms: 1.01x faster                                                              |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.50 ms: 1.01x faster                                                             |
| pickle_pure_python         | 303 us                                                                 | 302 us: 1.00x faster                                                              |
| regex_compile              | 123 ms                                                                 | 122 ms: 1.00x faster                                                              |
| pprint_pformat             | 1.41 sec                                                               | 1.40 sec: 1.00x faster                                                            |
| bpe_tokeniser              | 4.12 sec                                                               | 4.11 sec: 1.00x faster                                                            |
| raytrace                   | 246 ms                                                                 | 247 ms: 1.00x slower                                                              |
| go                         | 108 ms                                                                 | 109 ms: 1.00x slower                                                              |
| bench_thread_pool          | 1.04 ms                                                                | 1.05 ms: 1.00x slower                                                             |
| unpickle_pure_python       | 209 us                                                                 | 210 us: 1.00x slower                                                              |
| coverage                   | 81.1 ms                                                                | 81.5 ms: 1.00x slower                                                             |
| sympy_sum                  | 151 ms                                                                 | 152 ms: 1.01x slower                                                              |
| sqlalchemy_imperative      | 19.7 ms                                                                | 19.8 ms: 1.01x slower                                                             |
| richards                   | 40.4 ms                                                                | 40.7 ms: 1.01x slower                                                             |
| chaos                      | 53.3 ms                                                                | 53.7 ms: 1.01x slower                                                             |
| richards_super             | 46.1 ms                                                                | 46.5 ms: 1.01x slower                                                             |
| mdp                        | 1.13 sec                                                               | 1.14 sec: 1.01x slower                                                            |
| async_tree_memoization     | 307 ms                                                                 | 309 ms: 1.01x slower                                                              |
| genshi_text                | 20.7 ms                                                                | 20.9 ms: 1.01x slower                                                             |
| nqueens                    | 76.4 ms                                                                | 77.0 ms: 1.01x slower                                                             |
| spectral_norm              | 95.4 ms                                                                | 96.2 ms: 1.01x slower                                                             |
| tomli_loads                | 1.85 sec                                                               | 1.87 sec: 1.01x slower                                                            |
| fannkuch                   | 380 ms                                                                 | 383 ms: 1.01x slower                                                              |
| shortest_path              | 434 ms                                                                 | 438 ms: 1.01x slower                                                              |
| pathlib                    | 19.2 ms                                                                | 19.4 ms: 1.01x slower                                                             |
| pyflate                    | 405 ms                                                                 | 410 ms: 1.01x slower                                                              |
| scimark_sor                | 109 ms                                                                 | 110 ms: 1.01x slower                                                              |
| logging_format             | 6.54 us                                                                | 6.62 us: 1.01x slower                                                             |
| subparsers                 | 21.9 ms                                                                | 22.3 ms: 1.02x slower                                                             |
| json                       | 4.96 ms                                                                | 5.07 ms: 1.02x slower                                                             |
| logging_simple             | 5.85 us                                                                | 5.98 us: 1.02x slower                                                             |
| json_loads                 | 27.6 us                                                                | 28.2 us: 1.02x slower                                                             |
| typing_runtime_protocols   | 154 us                                                                 | 158 us: 1.02x slower                                                              |
| nbody                      | 86.7 ms                                                                | 89.7 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed    | 513 ms                                                                 | 560 ms: 1.09x slower                                                              |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                 | 553 ms: 1.10x slower                                                              |
| pidigits                   | 190 ms                                                                 | 226 ms: 1.19x slower                                                              |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                                      |

Benchmark hidden because not significant (28): scimark_monte_carlo, k_core, sqlite_synth, connected_components, xml_etree_iterparse, telco, sqlglot_v2_parse, xml_etree_process, sympy_str, pprint_safe_repr, pylint, sympy_expand, async_tree_none, sympy_integrate, sqlglot_v2_normalize, create_gc_cycles, xml_etree_generate, async_tree_io_tg, asyncio_websockets, deepcopy, dulwich_log, float, django_template, many_optionals, async_tree_none_tg, logging_silent, async_tree_io, async_tree_memoization_tg

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 61.63% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x