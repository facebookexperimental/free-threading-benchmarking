# Results vs. base

- fork: python
- ref: bedaea05987738c4c6b9
- machine: darwin-arm64
- commit hash: bedaea0
- commit date: 2025-10-19
- overall geometric mean: 1.005x faster
- HPT reliability: 86.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251019-3.15.0a1+-bedaea0/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json | results/bm-20251019-3.15.0a1+-bedaea0-JIT/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                                                                              | 116 ms: 1.03x slower                                                                                                    |
| docutils       | 1.04 sec                                                                                                            | 1.04 sec: 1.01x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                               | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20251019-3.15.0a1+-bedaea0/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json | results/bm-20251019-3.15.0a1+-bedaea0-JIT/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json |
|----------------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| coroutines                       | 10.0 ms                                                                                                             | 9.92 ms: 1.01x faster                                                                                                   |
| async_tree_none_tg               | 104 ms                                                                                                              | 103 ms: 1.01x faster                                                                                                    |
| async_tree_io_tg                 | 249 ms                                                                                                              | 247 ms: 1.01x faster                                                                                                    |
| asyncio_websockets               | 186 ms                                                                                                              | 187 ms: 1.01x slower                                                                                                    |
| async_tree_eager_memoization     | 110 ms                                                                                                              | 110 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed_tg | 245 ms                                                                                                              | 247 ms: 1.01x slower                                                                                                    |
| async_tree_eager                 | 41.2 ms                                                                                                             | 41.6 ms: 1.01x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg       | 258 ms                                                                                                              | 261 ms: 1.01x slower                                                                                                    |
| asyncio_tcp_ssl                  | 609 ms                                                                                                              | 615 ms: 1.01x slower                                                                                                    |
| async_tree_cpu_io_mixed          | 260 ms                                                                                                              | 263 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                                                              | 222 ms: 1.01x slower                                                                                                    |
| async_generators                 | 174 ms                                                                                                              | 184 ms: 1.06x slower                                                                                                    |
| Geometric mean                   | (ref)                                                                                                               | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (9): async_tree_io, async_tree_memoization_tg, async_tree_eager_tg, async_tree_none, async_tree_memoization, async_tree_eager_io, async_tree_eager_memoization_tg, async_tree_eager_io_tg, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251019-3.15.0a1+-bedaea0/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json | results/bm-20251019-3.15.0a1+-bedaea0-JIT/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 29.9 ms                                                                                                             | 29.6 ms: 1.01x faster                                                                                                   |
| pidigits       | 162 ms                                                                                                              | 161 ms: 1.01x faster                                                                                                    |
| nbody          | 49.1 ms                                                                                                             | 56.7 ms: 1.16x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                               | 1.04x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251019-3.15.0a1+-bedaea0/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json | results/bm-20251019-3.15.0a1+-bedaea0-JIT/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 48.9 ms                                                                                                             | 47.6 ms: 1.03x faster                                                                                                   |
| regex_v8       | 9.68 ms                                                                                                             | 9.66 ms: 1.00x faster                                                                                                   |
| Geometric mean | (ref)                                                                                                               | 1.01x faster                                                                                                            |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251019-3.15.0a1+-bedaea0/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json | results/bm-20251019-3.15.0a1+-bedaea0-JIT/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json |
|----------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 903 ms                                                                                                              | 829 ms: 1.09x faster                                                                                                    |
| unpickle_pure_python | 100 us                                                                                                              | 92.1 us: 1.09x faster                                                                                                   |
| xml_etree_process    | 25.4 ms                                                                                                             | 23.9 ms: 1.06x faster                                                                                                   |
| pickle_pure_python   | 143 us                                                                                                              | 138 us: 1.04x faster                                                                                                    |
| xml_etree_generate   | 35.5 ms                                                                                                             | 34.1 ms: 1.04x faster                                                                                                   |
| json_dumps           | 3.86 ms                                                                                                             | 3.78 ms: 1.02x faster                                                                                                   |
| pickle               | 6.05 us                                                                                                             | 5.94 us: 1.02x faster                                                                                                   |
| pickle_dict          | 13.1 us                                                                                                             | 12.9 us: 1.02x faster                                                                                                   |
| pickle_list          | 2.14 us                                                                                                             | 2.12 us: 1.01x faster                                                                                                   |
| unpickle             | 6.20 us                                                                                                             | 6.30 us: 1.02x slower                                                                                                   |
| unpickle_list        | 1.98 us                                                                                                             | 2.01 us: 1.02x slower                                                                                                   |
| json_loads           | 10.9 us                                                                                                             | 11.1 us: 1.02x slower                                                                                                   |
| xml_etree_iterparse  | 43.0 ms                                                                                                             | 44.1 ms: 1.03x slower                                                                                                   |
| xml_etree_parse      | 60.9 ms                                                                                                             | 63.3 ms: 1.04x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                               | 1.02x faster                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251019-3.15.0a1+-bedaea0/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json | results/bm-20251019-3.15.0a1+-bedaea0-JIT/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json |
|------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.86 ms                                                                                                             | 8.86 ms: 1.00x slower                                                                                                   |
| python_startup_no_site | 6.34 ms                                                                                                             | 6.35 ms: 1.00x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                               | 1.00x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20251019-3.15.0a1+-bedaea0/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json | results/bm-20251019-3.15.0a1+-bedaea0-JIT/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| mako           | 4.78 ms                                                                                                             | 4.38 ms: 1.09x faster                                                                                                   |
| genshi_text    | 9.97 ms                                                                                                             | 9.87 ms: 1.01x faster                                                                                                   |
| Geometric mean | (ref)                                                                                                               | 1.03x faster                                                                                                            |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                        | results/bm-20251019-3.15.0a1+-bedaea0/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json | results/bm-20251019-3.15.0a1+-bedaea0-JIT/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json |
|----------------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pprint_pformat                   | 659 ms                                                                                                              | 578 ms: 1.14x faster                                                                                                    |
| pprint_safe_repr                 | 327 ms                                                                                                              | 288 ms: 1.14x faster                                                                                                    |
| mako                             | 4.78 ms                                                                                                             | 4.38 ms: 1.09x faster                                                                                                   |
| tomli_loads                      | 903 ms                                                                                                              | 829 ms: 1.09x faster                                                                                                    |
| unpickle_pure_python             | 100 us                                                                                                              | 92.1 us: 1.09x faster                                                                                                   |
| xml_etree_process                | 25.4 ms                                                                                                             | 23.9 ms: 1.06x faster                                                                                                   |
| telco                            | 2.87 ms                                                                                                             | 2.70 ms: 1.06x faster                                                                                                   |
| scimark_fft                      | 128 ms                                                                                                              | 122 ms: 1.06x faster                                                                                                    |
| logging_silent                   | 42.4 ns                                                                                                             | 40.3 ns: 1.05x faster                                                                                                   |
| pickle_pure_python               | 143 us                                                                                                              | 138 us: 1.04x faster                                                                                                    |
| xml_etree_generate               | 35.5 ms                                                                                                             | 34.1 ms: 1.04x faster                                                                                                   |
| scimark_sor                      | 51.3 ms                                                                                                             | 49.3 ms: 1.04x faster                                                                                                   |
| fannkuch                         | 180 ms                                                                                                              | 173 ms: 1.04x faster                                                                                                    |
| generators                       | 17.9 ms                                                                                                             | 17.3 ms: 1.03x faster                                                                                                   |
| unpack_sequence                  | 32.0 ns                                                                                                             | 31.1 ns: 1.03x faster                                                                                                   |
| richards_super                   | 24.5 ms                                                                                                             | 23.8 ms: 1.03x faster                                                                                                   |
| richards                         | 21.6 ms                                                                                                             | 21.0 ms: 1.03x faster                                                                                                   |
| regex_compile                    | 48.9 ms                                                                                                             | 47.6 ms: 1.03x faster                                                                                                   |
| sqlglot_v2_parse                 | 555 us                                                                                                              | 542 us: 1.03x faster                                                                                                    |
| scimark_lu                       | 49.0 ms                                                                                                             | 47.8 ms: 1.02x faster                                                                                                   |
| raytrace                         | 119 ms                                                                                                              | 116 ms: 1.02x faster                                                                                                    |
| create_gc_cycles                 | 934 us                                                                                                              | 912 us: 1.02x faster                                                                                                    |
| sqlglot_v2_normalize             | 47.2 ms                                                                                                             | 46.1 ms: 1.02x faster                                                                                                   |
| logging_format                   | 2.59 us                                                                                                             | 2.53 us: 1.02x faster                                                                                                   |
| logging_simple                   | 2.36 us                                                                                                             | 2.31 us: 1.02x faster                                                                                                   |
| json_dumps                       | 3.86 ms                                                                                                             | 3.78 ms: 1.02x faster                                                                                                   |
| pyflate                          | 190 ms                                                                                                              | 187 ms: 1.02x faster                                                                                                    |
| sqlglot_v2_transpile             | 679 us                                                                                                              | 667 us: 1.02x faster                                                                                                    |
| pickle                           | 6.05 us                                                                                                             | 5.94 us: 1.02x faster                                                                                                   |
| scimark_monte_carlo              | 29.7 ms                                                                                                             | 29.1 ms: 1.02x faster                                                                                                   |
| pickle_dict                      | 13.1 us                                                                                                             | 12.9 us: 1.02x faster                                                                                                   |
| spectral_norm                    | 44.1 ms                                                                                                             | 43.4 ms: 1.02x faster                                                                                                   |
| sqlite_synth                     | 946 ns                                                                                                              | 932 ns: 1.02x faster                                                                                                    |
| coroutines                       | 10.0 ms                                                                                                             | 9.92 ms: 1.01x faster                                                                                                   |
| sqlglot_v2_optimize              | 23.1 ms                                                                                                             | 22.8 ms: 1.01x faster                                                                                                   |
| chaos                            | 26.1 ms                                                                                                             | 25.8 ms: 1.01x faster                                                                                                   |
| genshi_text                      | 9.97 ms                                                                                                             | 9.87 ms: 1.01x faster                                                                                                   |
| async_tree_none_tg               | 104 ms                                                                                                              | 103 ms: 1.01x faster                                                                                                    |
| sympy_sum                        | 55.7 ms                                                                                                             | 55.2 ms: 1.01x faster                                                                                                   |
| float                            | 29.9 ms                                                                                                             | 29.6 ms: 1.01x faster                                                                                                   |
| async_tree_io_tg                 | 249 ms                                                                                                              | 247 ms: 1.01x faster                                                                                                    |
| pidigits                         | 162 ms                                                                                                              | 161 ms: 1.01x faster                                                                                                    |
| pickle_list                      | 2.14 us                                                                                                             | 2.12 us: 1.01x faster                                                                                                   |
| hexiom                           | 2.85 ms                                                                                                             | 2.84 ms: 1.00x faster                                                                                                   |
| regex_v8                         | 9.68 ms                                                                                                             | 9.66 ms: 1.00x faster                                                                                                   |
| python_startup                   | 8.86 ms                                                                                                             | 8.86 ms: 1.00x slower                                                                                                   |
| python_startup_no_site           | 6.34 ms                                                                                                             | 6.35 ms: 1.00x slower                                                                                                   |
| sympy_str                        | 100 ms                                                                                                              | 100 ms: 1.00x slower                                                                                                    |
| asyncio_websockets               | 186 ms                                                                                                              | 187 ms: 1.01x slower                                                                                                    |
| docutils                         | 1.04 sec                                                                                                            | 1.04 sec: 1.01x slower                                                                                                  |
| bench_mp_pool                    | 42.4 ms                                                                                                             | 42.6 ms: 1.01x slower                                                                                                   |
| sympy_expand                     | 169 ms                                                                                                              | 170 ms: 1.01x slower                                                                                                    |
| mdp                              | 542 ms                                                                                                              | 546 ms: 1.01x slower                                                                                                    |
| async_tree_eager_memoization     | 110 ms                                                                                                              | 110 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed_tg | 245 ms                                                                                                              | 247 ms: 1.01x slower                                                                                                    |
| subparsers                       | 17.6 ms                                                                                                             | 17.8 ms: 1.01x slower                                                                                                   |
| async_tree_eager                 | 41.2 ms                                                                                                             | 41.6 ms: 1.01x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg       | 258 ms                                                                                                              | 261 ms: 1.01x slower                                                                                                    |
| deepcopy_reduce                  | 1.14 us                                                                                                             | 1.15 us: 1.01x slower                                                                                                   |
| asyncio_tcp_ssl                  | 609 ms                                                                                                              | 615 ms: 1.01x slower                                                                                                    |
| async_tree_cpu_io_mixed          | 260 ms                                                                                                              | 263 ms: 1.01x slower                                                                                                    |
| crypto_pyaes                     | 37.2 ms                                                                                                             | 37.7 ms: 1.01x slower                                                                                                   |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                                                              | 222 ms: 1.01x slower                                                                                                    |
| bpe_tokeniser                    | 1.96 sec                                                                                                            | 1.99 sec: 1.01x slower                                                                                                  |
| unpickle                         | 6.20 us                                                                                                             | 6.30 us: 1.02x slower                                                                                                   |
| unpickle_list                    | 1.98 us                                                                                                             | 2.01 us: 1.02x slower                                                                                                   |
| sympy_integrate                  | 7.38 ms                                                                                                             | 7.51 ms: 1.02x slower                                                                                                   |
| typing_runtime_protocols         | 63.3 us                                                                                                             | 64.6 us: 1.02x slower                                                                                                   |
| json_loads                       | 10.9 us                                                                                                             | 11.1 us: 1.02x slower                                                                                                   |
| xml_etree_iterparse              | 43.0 ms                                                                                                             | 44.1 ms: 1.03x slower                                                                                                   |
| k_core                           | 989 ms                                                                                                              | 1.02 sec: 1.03x slower                                                                                                  |
| nqueens                          | 37.8 ms                                                                                                             | 39.0 ms: 1.03x slower                                                                                                   |
| 2to3                             | 112 ms                                                                                                              | 116 ms: 1.03x slower                                                                                                    |
| many_optionals                   | 365 us                                                                                                              | 378 us: 1.04x slower                                                                                                    |
| xml_etree_parse                  | 60.9 ms                                                                                                             | 63.3 ms: 1.04x slower                                                                                                   |
| async_generators                 | 174 ms                                                                                                              | 184 ms: 1.06x slower                                                                                                    |
| shortest_path                    | 224 ms                                                                                                              | 241 ms: 1.08x slower                                                                                                    |
| connected_components             | 206 ms                                                                                                              | 225 ms: 1.09x slower                                                                                                    |
| scimark_sparse_mat_mult          | 1.90 ms                                                                                                             | 2.08 ms: 1.09x slower                                                                                                   |
| nbody                            | 49.1 ms                                                                                                             | 56.7 ms: 1.16x slower                                                                                                   |
| Geometric mean                   | (ref)                                                                                                               | 1.01x faster                                                                                                            |

Benchmark hidden because not significant (31): sphinx, genshi_xml, html5lib, async_tree_io, gc_traversal, async_tree_memoization_tg, meteor_contest, pathlib, go, comprehensions, deltablue, async_tree_eager_tg, dask, async_tree_none, deepcopy_memo, pylint, regex_dna, async_tree_memoization, dulwich_log, deepcopy, async_tree_eager_io, django_template, bench_thread_pool, regex_effbot, thrift, pycparser, json, coverage, async_tree_eager_memoization_tg, async_tree_eager_io_tg, asyncio_tcp

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 86.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x