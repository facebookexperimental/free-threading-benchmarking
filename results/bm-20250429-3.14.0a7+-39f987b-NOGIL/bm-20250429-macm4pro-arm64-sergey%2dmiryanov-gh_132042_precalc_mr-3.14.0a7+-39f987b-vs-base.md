# Results vs. base

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: darwin-arm64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.000x faster
- HPT reliability: 90.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 124 ms                                                                   | 123 ms: 1.01x faster                                                                |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                        |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed    | 227 ms                                                                   | 223 ms: 1.02x faster                                                                |
| async_tree_cpu_io_mixed_tg       | 237 ms                                                                   | 233 ms: 1.02x faster                                                                |
| async_tree_eager_cpu_io_mixed_tg | 229 ms                                                                   | 225 ms: 1.02x faster                                                                |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 242 ms: 1.01x faster                                                                |
| async_tree_eager_io              | 207 ms                                                                   | 206 ms: 1.01x faster                                                                |
| async_tree_eager_io_tg           | 196 ms                                                                   | 195 ms: 1.00x faster                                                                |
| async_tree_eager                 | 50.7 ms                                                                  | 50.5 ms: 1.00x faster                                                               |
| async_tree_io_tg                 | 197 ms                                                                   | 196 ms: 1.00x faster                                                                |
| async_tree_eager_memoization_tg  | 113 ms                                                                   | 113 ms: 1.00x faster                                                                |
| async_tree_none                  | 101 ms                                                                   | 102 ms: 1.01x slower                                                                |
| Geometric mean                   | (ref)                                                                    | 1.00x faster                                                                        |

Benchmark hidden because not significant (9): coroutines, async_tree_none_tg, async_tree_memoization, async_tree_eager_tg, async_generators, async_tree_eager_memoization, async_tree_io, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| nbody          | 55.9 ms                                                                  | 56.2 ms: 1.00x slower                                                               |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                        |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_v8       | 9.94 ms                                                                  | 10.0 ms: 1.01x slower                                                               |
| regex_dna      | 103 ms                                                                   | 104 ms: 1.01x slower                                                                |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                        |

Benchmark hidden because not significant (2): regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|---------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| xml_etree_iterparse | 37.8 ms                                                                  | 36.3 ms: 1.04x faster                                                               |
| xml_etree_process   | 26.8 ms                                                                  | 26.7 ms: 1.00x faster                                                               |
| xml_etree_generate  | 37.2 ms                                                                  | 37.0 ms: 1.00x faster                                                               |
| xml_etree_parse     | 56.4 ms                                                                  | 56.8 ms: 1.01x slower                                                               |
| json_loads          | 12.4 us                                                                  | 12.5 us: 1.01x slower                                                               |
| tomli_loads         | 974 ms                                                                   | 989 ms: 1.02x slower                                                                |
| Geometric mean      | (ref)                                                                    | 1.00x faster                                                                        |

Benchmark hidden because not significant (3): json_dumps, unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup         | 9.65 ms                                                                  | 9.48 ms: 1.02x faster                                                               |
| python_startup_no_site | 6.98 ms                                                                  | 6.92 ms: 1.01x faster                                                               |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| django_template | 16.5 ms                                                                  | 16.4 ms: 1.01x faster                                                               |
| mako            | 5.58 ms                                                                  | 5.59 ms: 1.00x slower                                                               |
| genshi_text     | 11.4 ms                                                                  | 11.5 ms: 1.01x slower                                                               |
| Geometric mean  | (ref)                                                                    | 1.00x slower                                                                        |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| xml_etree_iterparse              | 37.8 ms                                                                  | 36.3 ms: 1.04x faster                                                               |
| bench_mp_pool                    | 43.0 ms                                                                  | 41.9 ms: 1.03x faster                                                               |
| logging_silent                   | 45.2 ns                                                                  | 44.2 ns: 1.02x faster                                                               |
| python_startup                   | 9.65 ms                                                                  | 9.48 ms: 1.02x faster                                                               |
| async_tree_eager_cpu_io_mixed    | 227 ms                                                                   | 223 ms: 1.02x faster                                                                |
| async_tree_cpu_io_mixed_tg       | 237 ms                                                                   | 233 ms: 1.02x faster                                                                |
| async_tree_eager_cpu_io_mixed_tg | 229 ms                                                                   | 225 ms: 1.02x faster                                                                |
| async_tree_cpu_io_mixed          | 246 ms                                                                   | 242 ms: 1.01x faster                                                                |
| scimark_lu                       | 56.0 ms                                                                  | 55.5 ms: 1.01x faster                                                               |
| python_startup_no_site           | 6.98 ms                                                                  | 6.92 ms: 1.01x faster                                                               |
| 2to3                             | 124 ms                                                                   | 123 ms: 1.01x faster                                                                |
| fannkuch                         | 192 ms                                                                   | 190 ms: 1.01x faster                                                                |
| k_core                           | 1.00 sec                                                                 | 994 ms: 1.01x faster                                                                |
| sqlglot_v2_parse                 | 601 us                                                                   | 597 us: 1.01x faster                                                                |
| django_template                  | 16.5 ms                                                                  | 16.4 ms: 1.01x faster                                                               |
| pprint_pformat                   | 738 ms                                                                   | 733 ms: 1.01x faster                                                                |
| sqlglot_v2_transpile             | 733 us                                                                   | 729 us: 1.01x faster                                                                |
| async_tree_eager_io              | 207 ms                                                                   | 206 ms: 1.01x faster                                                                |
| sqlglot_v2_optimize              | 24.3 ms                                                                  | 24.1 ms: 1.01x faster                                                               |
| async_tree_eager_io_tg           | 196 ms                                                                   | 195 ms: 1.00x faster                                                                |
| bpe_tokeniser                    | 1.97 sec                                                                 | 1.96 sec: 1.00x faster                                                              |
| async_tree_eager                 | 50.7 ms                                                                  | 50.5 ms: 1.00x faster                                                               |
| xml_etree_process                | 26.8 ms                                                                  | 26.7 ms: 1.00x faster                                                               |
| nqueens                          | 41.6 ms                                                                  | 41.4 ms: 1.00x faster                                                               |
| xml_etree_generate               | 37.2 ms                                                                  | 37.0 ms: 1.00x faster                                                               |
| async_tree_io_tg                 | 197 ms                                                                   | 196 ms: 1.00x faster                                                                |
| sqlglot_v2_normalize             | 49.1 ms                                                                  | 49.0 ms: 1.00x faster                                                               |
| mdp                              | 575 ms                                                                   | 573 ms: 1.00x faster                                                                |
| telco                            | 3.24 ms                                                                  | 3.23 ms: 1.00x faster                                                               |
| async_tree_eager_memoization_tg  | 113 ms                                                                   | 113 ms: 1.00x faster                                                                |
| sympy_integrate                  | 8.16 ms                                                                  | 8.14 ms: 1.00x faster                                                               |
| dulwich_log                      | 19.1 ms                                                                  | 19.0 ms: 1.00x faster                                                               |
| chaos                            | 28.7 ms                                                                  | 28.7 ms: 1.00x slower                                                               |
| mako                             | 5.58 ms                                                                  | 5.59 ms: 1.00x slower                                                               |
| scimark_monte_carlo              | 32.9 ms                                                                  | 33.0 ms: 1.00x slower                                                               |
| shortest_path                    | 233 ms                                                                   | 233 ms: 1.00x slower                                                                |
| hexiom                           | 3.18 ms                                                                  | 3.19 ms: 1.00x slower                                                               |
| comprehensions                   | 8.61 us                                                                  | 8.65 us: 1.00x slower                                                               |
| subparsers                       | 9.01 ms                                                                  | 9.05 ms: 1.00x slower                                                               |
| nbody                            | 55.9 ms                                                                  | 56.2 ms: 1.00x slower                                                               |
| sqlalchemy_declarative           | 51.3 ms                                                                  | 51.6 ms: 1.01x slower                                                               |
| pathlib                          | 11.0 ms                                                                  | 11.1 ms: 1.01x slower                                                               |
| regex_v8                         | 9.94 ms                                                                  | 10.0 ms: 1.01x slower                                                               |
| xml_etree_parse                  | 56.4 ms                                                                  | 56.8 ms: 1.01x slower                                                               |
| scimark_sor                      | 54.6 ms                                                                  | 55.0 ms: 1.01x slower                                                               |
| regex_dna                        | 103 ms                                                                   | 104 ms: 1.01x slower                                                                |
| genshi_text                      | 11.4 ms                                                                  | 11.5 ms: 1.01x slower                                                               |
| richards                         | 24.3 ms                                                                  | 24.6 ms: 1.01x slower                                                               |
| typing_runtime_protocols         | 73.4 us                                                                  | 74.3 us: 1.01x slower                                                               |
| sqlite_synth                     | 815 ns                                                                   | 824 ns: 1.01x slower                                                                |
| json_loads                       | 12.4 us                                                                  | 12.5 us: 1.01x slower                                                               |
| async_tree_none                  | 101 ms                                                                   | 102 ms: 1.01x slower                                                                |
| pyflate                          | 201 ms                                                                   | 203 ms: 1.01x slower                                                                |
| tomli_loads                      | 974 ms                                                                   | 989 ms: 1.02x slower                                                                |
| spectral_norm                    | 50.8 ms                                                                  | 51.7 ms: 1.02x slower                                                               |
| richards_super                   | 27.7 ms                                                                  | 28.3 ms: 1.02x slower                                                               |
| coverage                         | 39.9 ms                                                                  | 40.8 ms: 1.02x slower                                                               |
| Geometric mean                   | (ref)                                                                    | 1.00x faster                                                                        |

Benchmark hidden because not significant (46): sympy_expand, regex_compile, json, pycparser, coroutines, deepcopy_reduce, logging_format, deepcopy_memo, async_tree_none_tg, sympy_str, scimark_sparse_mat_mult, sphinx, docutils, float, async_tree_memoization, async_tree_eager_tg, pprint_safe_repr, genshi_xml, raytrace, async_generators, async_tree_eager_memoization, meteor_contest, async_tree_io, html5lib, pylint, json_dumps, crypto_pyaes, logging_simple, go, bench_thread_pool, generators, pidigits, connected_components, asyncio_websockets, gc_traversal, unpickle_pure_python, pickle_pure_python, sympy_sum, many_optionals, sqlalchemy_imperative, create_gc_cycles, regex_effbot, deltablue, scimark_fft, deepcopy, async_tree_memoization_tg

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 90.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x