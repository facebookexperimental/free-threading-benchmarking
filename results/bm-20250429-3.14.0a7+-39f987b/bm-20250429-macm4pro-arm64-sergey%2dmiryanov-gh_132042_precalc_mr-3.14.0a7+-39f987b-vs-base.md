# Results vs. base

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: darwin-arm64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.008x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                                   | 111 ms: 1.03x faster                                                                |
| docutils       | 1.07 sec                                                                 | 1.05 sec: 1.01x faster                                                              |
| html5lib       | 24.6 ms                                                                  | 24.2 ms: 1.01x faster                                                               |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                        |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|---------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_eager                | 43.0 ms                                                                  | 41.5 ms: 1.04x faster                                                               |
| async_tree_cpu_io_mixed         | 276 ms                                                                   | 268 ms: 1.03x faster                                                                |
| async_tree_eager_io_tg          | 258 ms                                                                   | 251 ms: 1.03x faster                                                                |
| async_generators                | 175 ms                                                                   | 171 ms: 1.02x faster                                                                |
| async_tree_none                 | 115 ms                                                                   | 113 ms: 1.02x faster                                                                |
| async_tree_io                   | 255 ms                                                                   | 250 ms: 1.02x faster                                                                |
| async_tree_eager_io             | 250 ms                                                                   | 246 ms: 1.02x faster                                                                |
| async_tree_none_tg              | 107 ms                                                                   | 105 ms: 1.02x faster                                                                |
| coroutines                      | 10.3 ms                                                                  | 10.1 ms: 1.01x faster                                                               |
| async_tree_eager_cpu_io_mixed   | 226 ms                                                                   | 223 ms: 1.01x faster                                                                |
| async_tree_eager_memoization    | 112 ms                                                                   | 111 ms: 1.01x faster                                                                |
| async_tree_memoization_tg       | 149 ms                                                                   | 147 ms: 1.01x faster                                                                |
| async_tree_eager_memoization_tg | 135 ms                                                                   | 133 ms: 1.01x faster                                                                |
| async_tree_io_tg                | 252 ms                                                                   | 249 ms: 1.01x faster                                                                |
| async_tree_memoization          | 149 ms                                                                   | 148 ms: 1.01x faster                                                                |
| asyncio_websockets              | 194 ms                                                                   | 193 ms: 1.01x faster                                                                |
| Geometric mean                  | (ref)                                                                    | 1.02x faster                                                                        |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_eager_tg, async_tree_eager_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| pidigits       | 170 ms                                                                   | 169 ms: 1.01x faster                                                                |
| float          | 29.1 ms                                                                  | 29.2 ms: 1.00x slower                                                               |
| nbody          | 49.3 ms                                                                  | 51.3 ms: 1.04x slower                                                               |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_compile  | 49.0 ms                                                                  | 48.2 ms: 1.02x faster                                                               |
| regex_v8       | 10.4 ms                                                                  | 10.3 ms: 1.00x faster                                                               |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                        |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|---------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| tomli_loads         | 933 ms                                                                   | 918 ms: 1.02x faster                                                                |
| json_loads          | 11.7 us                                                                  | 11.6 us: 1.01x faster                                                               |
| pickle_pure_python  | 146 us                                                                   | 145 us: 1.01x faster                                                                |
| xml_etree_generate  | 36.3 ms                                                                  | 36.1 ms: 1.01x faster                                                               |
| xml_etree_parse     | 62.6 ms                                                                  | 63.0 ms: 1.01x slower                                                               |
| xml_etree_iterparse | 44.2 ms                                                                  | 44.6 ms: 1.01x slower                                                               |
| Geometric mean      | (ref)                                                                    | 1.00x faster                                                                        |

Benchmark hidden because not significant (3): xml_etree_process, json_dumps, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup         | 9.16 ms                                                                  | 8.92 ms: 1.03x faster                                                               |
| python_startup_no_site | 6.26 ms                                                                  | 6.16 ms: 1.02x faster                                                               |
| Geometric mean         | (ref)                                                                    | 1.02x faster                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| django_template | 15.3 ms                                                                  | 15.0 ms: 1.02x faster                                                               |
| mako            | 4.97 ms                                                                  | 4.91 ms: 1.01x faster                                                               |
| genshi_text     | 10.0 ms                                                                  | 9.96 ms: 1.00x faster                                                               |
| genshi_xml      | 21.6 ms                                                                  | 21.9 ms: 1.01x slower                                                               |
| Geometric mean  | (ref)                                                                    | 1.01x faster                                                                        |

All benchmarks:
===============

| Benchmark                       | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|---------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| go                              | 59.1 ms                                                                  | 56.4 ms: 1.05x faster                                                               |
| deltablue                       | 1.56 ms                                                                  | 1.49 ms: 1.05x faster                                                               |
| create_gc_cycles                | 949 us                                                                   | 915 us: 1.04x faster                                                                |
| async_tree_eager                | 43.0 ms                                                                  | 41.5 ms: 1.04x faster                                                               |
| comprehensions                  | 7.78 us                                                                  | 7.51 us: 1.04x faster                                                               |
| bench_mp_pool                   | 41.7 ms                                                                  | 40.3 ms: 1.04x faster                                                               |
| 2to3                            | 114 ms                                                                   | 111 ms: 1.03x faster                                                                |
| async_tree_cpu_io_mixed         | 276 ms                                                                   | 268 ms: 1.03x faster                                                                |
| deepcopy_memo                   | 12.8 us                                                                  | 12.4 us: 1.03x faster                                                               |
| pprint_safe_repr                | 342 ms                                                                   | 331 ms: 1.03x faster                                                                |
| async_tree_eager_io_tg          | 258 ms                                                                   | 251 ms: 1.03x faster                                                                |
| python_startup                  | 9.16 ms                                                                  | 8.92 ms: 1.03x faster                                                               |
| hexiom                          | 2.85 ms                                                                  | 2.78 ms: 1.03x faster                                                               |
| pyflate                         | 201 ms                                                                   | 196 ms: 1.03x faster                                                                |
| async_generators                | 175 ms                                                                   | 171 ms: 1.02x faster                                                                |
| raytrace                        | 121 ms                                                                   | 118 ms: 1.02x faster                                                                |
| gc_traversal                    | 2.13 ms                                                                  | 2.08 ms: 1.02x faster                                                               |
| many_optionals                  | 241 us                                                                   | 236 us: 1.02x faster                                                                |
| async_tree_none                 | 115 ms                                                                   | 113 ms: 1.02x faster                                                                |
| django_template                 | 15.3 ms                                                                  | 15.0 ms: 1.02x faster                                                               |
| pprint_pformat                  | 691 ms                                                                   | 679 ms: 1.02x faster                                                                |
| async_tree_io                   | 255 ms                                                                   | 250 ms: 1.02x faster                                                                |
| python_startup_no_site          | 6.26 ms                                                                  | 6.16 ms: 1.02x faster                                                               |
| tomli_loads                     | 933 ms                                                                   | 918 ms: 1.02x faster                                                                |
| deepcopy                        | 110 us                                                                   | 108 us: 1.02x faster                                                                |
| regex_compile                   | 49.0 ms                                                                  | 48.2 ms: 1.02x faster                                                               |
| async_tree_eager_io             | 250 ms                                                                   | 246 ms: 1.02x faster                                                                |
| async_tree_none_tg              | 107 ms                                                                   | 105 ms: 1.02x faster                                                                |
| dulwich_log                     | 18.1 ms                                                                  | 17.8 ms: 1.02x faster                                                               |
| html5lib                        | 24.6 ms                                                                  | 24.2 ms: 1.01x faster                                                               |
| docutils                        | 1.07 sec                                                                 | 1.05 sec: 1.01x faster                                                              |
| coroutines                      | 10.3 ms                                                                  | 10.1 ms: 1.01x faster                                                               |
| async_tree_eager_cpu_io_mixed   | 226 ms                                                                   | 223 ms: 1.01x faster                                                                |
| async_tree_eager_memoization    | 112 ms                                                                   | 111 ms: 1.01x faster                                                                |
| chaos                           | 26.8 ms                                                                  | 26.4 ms: 1.01x faster                                                               |
| mako                            | 4.97 ms                                                                  | 4.91 ms: 1.01x faster                                                               |
| json_loads                      | 11.7 us                                                                  | 11.6 us: 1.01x faster                                                               |
| async_tree_memoization_tg       | 149 ms                                                                   | 147 ms: 1.01x faster                                                                |
| async_tree_eager_memoization_tg | 135 ms                                                                   | 133 ms: 1.01x faster                                                                |
| sqlglot_v2_optimize             | 22.9 ms                                                                  | 22.6 ms: 1.01x faster                                                               |
| async_tree_io_tg                | 252 ms                                                                   | 249 ms: 1.01x faster                                                                |
| logging_silent                  | 41.2 ns                                                                  | 40.8 ns: 1.01x faster                                                               |
| scimark_monte_carlo             | 29.5 ms                                                                  | 29.2 ms: 1.01x faster                                                               |
| generators                      | 17.9 ms                                                                  | 17.8 ms: 1.01x faster                                                               |
| deepcopy_reduce                 | 1.11 us                                                                  | 1.10 us: 1.01x faster                                                               |
| pickle_pure_python              | 146 us                                                                   | 145 us: 1.01x faster                                                                |
| sqlglot_v2_normalize            | 46.9 ms                                                                  | 46.5 ms: 1.01x faster                                                               |
| async_tree_memoization          | 149 ms                                                                   | 148 ms: 1.01x faster                                                                |
| subparsers                      | 8.92 ms                                                                  | 8.84 ms: 1.01x faster                                                               |
| pidigits                        | 170 ms                                                                   | 169 ms: 1.01x faster                                                                |
| sqlglot_v2_parse                | 550 us                                                                   | 545 us: 1.01x faster                                                                |
| sqlglot_v2_transpile            | 673 us                                                                   | 668 us: 1.01x faster                                                                |
| asyncio_websockets              | 194 ms                                                                   | 193 ms: 1.01x faster                                                                |
| connected_components            | 201 ms                                                                   | 199 ms: 1.01x faster                                                                |
| shortest_path                   | 217 ms                                                                   | 216 ms: 1.01x faster                                                                |
| sympy_str                       | 99.0 ms                                                                  | 98.4 ms: 1.01x faster                                                               |
| pathlib                         | 11.2 ms                                                                  | 11.1 ms: 1.01x faster                                                               |
| xml_etree_generate              | 36.3 ms                                                                  | 36.1 ms: 1.01x faster                                                               |
| richards                        | 22.1 ms                                                                  | 22.0 ms: 1.00x faster                                                               |
| genshi_text                     | 10.0 ms                                                                  | 9.96 ms: 1.00x faster                                                               |
| sympy_sum                       | 56.2 ms                                                                  | 56.0 ms: 1.00x faster                                                               |
| regex_v8                        | 10.4 ms                                                                  | 10.3 ms: 1.00x faster                                                               |
| sqlalchemy_declarative          | 46.1 ms                                                                  | 46.0 ms: 1.00x faster                                                               |
| bpe_tokeniser                   | 1.94 sec                                                                 | 1.94 sec: 1.00x slower                                                              |
| float                           | 29.1 ms                                                                  | 29.2 ms: 1.00x slower                                                               |
| sqlalchemy_imperative           | 5.44 ms                                                                  | 5.47 ms: 1.01x slower                                                               |
| xml_etree_parse                 | 62.6 ms                                                                  | 63.0 ms: 1.01x slower                                                               |
| sympy_integrate                 | 7.48 ms                                                                  | 7.53 ms: 1.01x slower                                                               |
| scimark_lu                      | 48.3 ms                                                                  | 48.6 ms: 1.01x slower                                                               |
| nqueens                         | 37.7 ms                                                                  | 38.0 ms: 1.01x slower                                                               |
| scimark_fft                     | 130 ms                                                                   | 131 ms: 1.01x slower                                                                |
| xml_etree_iterparse             | 44.2 ms                                                                  | 44.6 ms: 1.01x slower                                                               |
| json                            | 1.98 ms                                                                  | 2.00 ms: 1.01x slower                                                               |
| fannkuch                        | 178 ms                                                                   | 180 ms: 1.01x slower                                                                |
| scimark_sparse_mat_mult         | 1.95 ms                                                                  | 1.97 ms: 1.01x slower                                                               |
| genshi_xml                      | 21.6 ms                                                                  | 21.9 ms: 1.01x slower                                                               |
| mdp                             | 517 ms                                                                   | 527 ms: 1.02x slower                                                                |
| crypto_pyaes                    | 37.6 ms                                                                  | 38.3 ms: 1.02x slower                                                               |
| scimark_sor                     | 50.7 ms                                                                  | 51.9 ms: 1.02x slower                                                               |
| coverage                        | 33.2 ms                                                                  | 34.3 ms: 1.03x slower                                                               |
| nbody                           | 49.3 ms                                                                  | 51.3 ms: 1.04x slower                                                               |
| spectral_norm                   | 45.2 ms                                                                  | 47.3 ms: 1.05x slower                                                               |
| Geometric mean                  | (ref)                                                                    | 1.01x faster                                                                        |

Benchmark hidden because not significant (21): async_tree_cpu_io_mixed_tg, async_tree_eager_tg, sqlite_synth, pylint, richards_super, logging_simple, regex_effbot, typing_runtime_protocols, bench_thread_pool, xml_etree_process, async_tree_eager_cpu_io_mixed_tg, sphinx, sympy_expand, meteor_contest, logging_format, json_dumps, regex_dna, unpickle_pure_python, telco, pycparser, k_core

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x