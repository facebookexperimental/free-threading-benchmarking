# Results vs. base

- fork: nascheme
- ref: gh_158197_split_dict
- machine: darwin-arm64
- commit hash: 703df80
- commit date: 2026-10-16
- overall geometric mean: 1.004x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 121 ms                                                                      | 119 ms: 1.02x faster                                                          |
| docutils       | 997 ms                                                                      | 991 ms: 1.01x faster                                                          |
| html5lib       | 21.5 ms                                                                     | 21.7 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                       | 1.00x faster                                                                  |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_io                    | 277 ms                                                                      | 270 ms: 1.02x faster                                                          |
| async_tree_none                  | 133 ms                                                                      | 130 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 285 ms                                                                      | 281 ms: 1.02x faster                                                          |
| async_tree_eager_cpu_io_mixed    | 228 ms                                                                      | 224 ms: 1.02x faster                                                          |
| async_tree_eager_io              | 278 ms                                                                      | 273 ms: 1.02x faster                                                          |
| async_generators                 | 183 ms                                                                      | 180 ms: 1.02x faster                                                          |
| async_tree_eager_cpu_io_mixed_tg | 267 ms                                                                      | 263 ms: 1.01x faster                                                          |
| async_tree_eager                 | 45.2 ms                                                                     | 44.6 ms: 1.01x faster                                                         |
| async_tree_eager_io_tg           | 277 ms                                                                      | 273 ms: 1.01x faster                                                          |
| async_tree_io_tg                 | 277 ms                                                                      | 274 ms: 1.01x faster                                                          |
| async_tree_cpu_io_mixed          | 291 ms                                                                      | 287 ms: 1.01x faster                                                          |
| asyncio_websockets               | 183 ms                                                                      | 181 ms: 1.01x faster                                                          |
| async_tree_eager_memoization     | 119 ms                                                                      | 118 ms: 1.01x faster                                                          |
| async_tree_eager_tg              | 107 ms                                                                      | 110 ms: 1.04x slower                                                          |
| Geometric mean                   | (ref)                                                                       | 1.01x faster                                                                  |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_eager_memoization_tg, async_tree_memoization_tg, async_tree_memoization, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 30.6 ms                                                                     | 30.7 ms: 1.00x slower                                                         |
| pidigits       | 159 ms                                                                      | 160 ms: 1.00x slower                                                          |
| nbody          | 53.3 ms                                                                     | 53.9 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 8.86 ms                                                                     | 8.63 ms: 1.03x faster                                                         |
| regex_effbot   | 1.34 ms                                                                     | 1.33 ms: 1.01x faster                                                         |
| regex_compile  | 58.6 ms                                                                     | 58.3 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                                       | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 145 us                                                                      | 142 us: 1.02x faster                                                          |
| json_loads           | 10.7 us                                                                     | 10.5 us: 1.02x faster                                                         |
| json_dumps           | 3.64 ms                                                                     | 3.58 ms: 1.02x faster                                                         |
| xml_etree_generate   | 35.1 ms                                                                     | 35.4 ms: 1.01x slower                                                         |
| xml_etree_process    | 26.6 ms                                                                     | 26.8 ms: 1.01x slower                                                         |
| xml_etree_parse      | 56.9 ms                                                                     | 57.5 ms: 1.01x slower                                                         |
| tomli_loads          | 832 ms                                                                      | 845 ms: 1.02x slower                                                          |
| unpickle_pure_python | 96.1 us                                                                     | 98.1 us: 1.02x slower                                                         |
| xml_etree_iterparse  | 37.3 ms                                                                     | 38.3 ms: 1.03x slower                                                         |
| Geometric mean       | (ref)                                                                       | 1.00x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|------------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                                     | 7.17 ms: 1.00x slower                                                         |
| Geometric mean         | (ref)                                                                       | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|-----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| django_template | 15.6 ms                                                                     | 15.4 ms: 1.01x faster                                                         |
| mako            | 5.59 ms                                                                     | 5.57 ms: 1.00x faster                                                         |
| Geometric mean  | (ref)                                                                       | 1.01x faster                                                                  |

All benchmarks:
===============

| Benchmark                        | bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1+dev-010bebb | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| many_optionals                   | 241 us                                                                      | 235 us: 1.03x faster                                                          |
| regex_v8                         | 8.86 ms                                                                     | 8.63 ms: 1.03x faster                                                         |
| async_tree_io                    | 277 ms                                                                      | 270 ms: 1.02x faster                                                          |
| deepcopy_memo                    | 13.4 us                                                                     | 13.1 us: 1.02x faster                                                         |
| coverage                         | 39.0 ms                                                                     | 38.1 ms: 1.02x faster                                                         |
| subparsers                       | 4.02 ms                                                                     | 3.93 ms: 1.02x faster                                                         |
| 2to3                             | 121 ms                                                                      | 119 ms: 1.02x faster                                                          |
| pickle_pure_python               | 145 us                                                                      | 142 us: 1.02x faster                                                          |
| async_tree_none                  | 133 ms                                                                      | 130 ms: 1.02x faster                                                          |
| logging_silent                   | 43.1 ns                                                                     | 42.3 ns: 1.02x faster                                                         |
| json_loads                       | 10.7 us                                                                     | 10.5 us: 1.02x faster                                                         |
| hexiom                           | 2.88 ms                                                                     | 2.83 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 285 ms                                                                      | 281 ms: 1.02x faster                                                          |
| async_tree_eager_cpu_io_mixed    | 228 ms                                                                      | 224 ms: 1.02x faster                                                          |
| async_tree_eager_io              | 278 ms                                                                      | 273 ms: 1.02x faster                                                          |
| async_generators                 | 183 ms                                                                      | 180 ms: 1.02x faster                                                          |
| json_dumps                       | 3.64 ms                                                                     | 3.58 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 267 ms                                                                      | 263 ms: 1.01x faster                                                          |
| deepcopy_reduce                  | 1.09 us                                                                     | 1.07 us: 1.01x faster                                                         |
| bench_mp_pool                    | 42.0 ms                                                                     | 41.3 ms: 1.01x faster                                                         |
| async_tree_eager                 | 45.2 ms                                                                     | 44.6 ms: 1.01x faster                                                         |
| dulwich_log                      | 18.4 ms                                                                     | 18.1 ms: 1.01x faster                                                         |
| async_tree_eager_io_tg           | 277 ms                                                                      | 273 ms: 1.01x faster                                                          |
| async_tree_io_tg                 | 277 ms                                                                      | 274 ms: 1.01x faster                                                          |
| mdp                              | 551 ms                                                                      | 544 ms: 1.01x faster                                                          |
| async_tree_cpu_io_mixed          | 291 ms                                                                      | 287 ms: 1.01x faster                                                          |
| regex_effbot                     | 1.34 ms                                                                     | 1.33 ms: 1.01x faster                                                         |
| django_template                  | 15.6 ms                                                                     | 15.4 ms: 1.01x faster                                                         |
| json                             | 1.87 ms                                                                     | 1.85 ms: 1.01x faster                                                         |
| pprint_safe_repr                 | 330 ms                                                                      | 326 ms: 1.01x faster                                                          |
| deltablue                        | 1.59 ms                                                                     | 1.57 ms: 1.01x faster                                                         |
| crypto_pyaes                     | 40.4 ms                                                                     | 40.0 ms: 1.01x faster                                                         |
| generators                       | 15.4 ms                                                                     | 15.3 ms: 1.01x faster                                                         |
| bpe_tokeniser                    | 1.89 sec                                                                    | 1.87 sec: 1.01x faster                                                        |
| asyncio_websockets               | 183 ms                                                                      | 181 ms: 1.01x faster                                                          |
| pathlib                          | 10.4 ms                                                                     | 10.3 ms: 1.01x faster                                                         |
| sympy_integrate                  | 7.68 ms                                                                     | 7.62 ms: 1.01x faster                                                         |
| go                               | 55.2 ms                                                                     | 54.8 ms: 1.01x faster                                                         |
| deepcopy                         | 100.0 us                                                                    | 99.3 us: 1.01x faster                                                         |
| async_tree_eager_memoization     | 119 ms                                                                      | 118 ms: 1.01x faster                                                          |
| pprint_pformat                   | 690 ms                                                                      | 686 ms: 1.01x faster                                                          |
| nqueens                          | 37.8 ms                                                                     | 37.6 ms: 1.01x faster                                                         |
| docutils                         | 997 ms                                                                      | 991 ms: 1.01x faster                                                          |
| sympy_expand                     | 177 ms                                                                      | 176 ms: 1.01x faster                                                          |
| sympy_sum                        | 57.6 ms                                                                     | 57.3 ms: 1.01x faster                                                         |
| typing_runtime_protocols         | 53.6 us                                                                     | 53.2 us: 1.01x faster                                                         |
| fannkuch                         | 180 ms                                                                      | 180 ms: 1.01x faster                                                          |
| regex_compile                    | 58.6 ms                                                                     | 58.3 ms: 1.00x faster                                                         |
| telco                            | 3.09 ms                                                                     | 3.07 ms: 1.00x faster                                                         |
| sympy_str                        | 105 ms                                                                      | 104 ms: 1.00x faster                                                          |
| chaos                            | 26.8 ms                                                                     | 26.7 ms: 1.00x faster                                                         |
| mako                             | 5.59 ms                                                                     | 5.57 ms: 1.00x faster                                                         |
| python_startup_no_site           | 7.16 ms                                                                     | 7.17 ms: 1.00x slower                                                         |
| float                            | 30.6 ms                                                                     | 30.7 ms: 1.00x slower                                                         |
| raytrace                         | 120 ms                                                                      | 121 ms: 1.00x slower                                                          |
| pidigits                         | 159 ms                                                                      | 160 ms: 1.00x slower                                                          |
| scimark_monte_carlo              | 31.6 ms                                                                     | 31.8 ms: 1.01x slower                                                         |
| pycparser                        | 450 ms                                                                      | 452 ms: 1.01x slower                                                          |
| create_gc_cycles                 | 459 us                                                                      | 461 us: 1.01x slower                                                          |
| thrift                           | 324 us                                                                      | 326 us: 1.01x slower                                                          |
| scimark_fft                      | 126 ms                                                                      | 127 ms: 1.01x slower                                                          |
| xml_etree_generate               | 35.1 ms                                                                     | 35.4 ms: 1.01x slower                                                         |
| spectral_norm                    | 43.9 ms                                                                     | 44.2 ms: 1.01x slower                                                         |
| xml_etree_process                | 26.6 ms                                                                     | 26.8 ms: 1.01x slower                                                         |
| richards                         | 22.2 ms                                                                     | 22.3 ms: 1.01x slower                                                         |
| html5lib                         | 21.5 ms                                                                     | 21.7 ms: 1.01x slower                                                         |
| richards_super                   | 25.3 ms                                                                     | 25.6 ms: 1.01x slower                                                         |
| xml_etree_parse                  | 56.9 ms                                                                     | 57.5 ms: 1.01x slower                                                         |
| nbody                            | 53.3 ms                                                                     | 53.9 ms: 1.01x slower                                                         |
| tomli_loads                      | 832 ms                                                                      | 845 ms: 1.02x slower                                                          |
| unpickle_pure_python             | 96.1 us                                                                     | 98.1 us: 1.02x slower                                                         |
| scimark_sparse_mat_mult          | 2.06 ms                                                                     | 2.11 ms: 1.02x slower                                                         |
| xml_etree_iterparse              | 37.3 ms                                                                     | 38.3 ms: 1.03x slower                                                         |
| async_tree_eager_tg              | 107 ms                                                                      | 110 ms: 1.04x slower                                                          |
| Geometric mean                   | (ref)                                                                       | 1.00x faster                                                                  |

Benchmark hidden because not significant (26): async_tree_none_tg, async_tree_eager_memoization_tg, async_tree_memoization_tg, async_tree_memoization, gc_traversal, pylint, logging_simple, shortest_path, regex_dna, scimark_sor, sqlglot_v2_normalize, k_core, sphinx, pyflate, scimark_lu, coroutines, sqlglot_v2_transpile, connected_components, python_startup, bench_thread_pool, logging_format, meteor_contest, comprehensions, sqlglot_v2_parse, sqlglot_v2_optimize, sqlite_synth

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x