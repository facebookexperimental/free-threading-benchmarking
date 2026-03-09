# Results vs. base

- fork: python
- ref: 5a15a52dd1dee37af4f2
- machine: darwin-arm64
- commit hash: 5a15a52
- commit date: 2026-03-08
- overall geometric mean: 1.008x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 120 ms                                                                   | 123 ms: 1.02x slower                                                     |
| docutils       | 1.00 sec                                                                 | 1.01 sec: 1.01x slower                                                   |
| html5lib       | 22.6 ms                                                                  | 23.1 ms: 1.02x slower                                                    |
| sphinx         | 422 ms                                                                   | 424 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                       | 10.1 ms                                                                  | 10.2 ms: 1.01x slower                                                    |
| asyncio_websockets               | 184 ms                                                                   | 186 ms: 1.01x slower                                                     |
| async_tree_eager_memoization     | 112 ms                                                                   | 114 ms: 1.01x slower                                                     |
| async_tree_none_tg               | 106 ms                                                                   | 108 ms: 1.01x slower                                                     |
| async_tree_eager                 | 46.3 ms                                                                  | 46.9 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 221 ms                                                                   | 225 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 255 ms                                                                   | 259 ms: 1.02x slower                                                     |
| async_tree_eager_tg              | 92.4 ms                                                                  | 94.2 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 243 ms                                                                   | 248 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed          | 260 ms                                                                   | 265 ms: 1.02x slower                                                     |
| async_generators                 | 184 ms                                                                   | 188 ms: 1.02x slower                                                     |
| Geometric mean                   | (ref)                                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (8): async_tree_memoization_tg, async_tree_io_tg, async_tree_memoization, async_tree_io, async_tree_eager_memoization_tg, async_tree_eager_io_tg, async_tree_eager_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 56.1 ms                                                                  | 55.8 ms: 1.01x faster                                                    |
| float          | 28.7 ms                                                                  | 28.9 ms: 1.01x slower                                                    |
| pidigits       | 164 ms                                                                   | 169 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 9.26 ms                                                                  | 9.23 ms: 1.00x faster                                                    |
| regex_compile  | 50.6 ms                                                                  | 50.7 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 3.92 ms                                                                  | 3.84 ms: 1.02x faster                                                    |
| tomli_loads          | 857 ms                                                                   | 846 ms: 1.01x faster                                                     |
| unpickle_pure_python | 107 us                                                                   | 107 us: 1.01x faster                                                     |
| pickle_pure_python   | 146 us                                                                   | 147 us: 1.01x slower                                                     |
| xml_etree_process    | 26.8 ms                                                                  | 27.0 ms: 1.01x slower                                                    |
| xml_etree_generate   | 37.2 ms                                                                  | 37.5 ms: 1.01x slower                                                    |
| json_loads           | 11.2 us                                                                  | 11.4 us: 1.01x slower                                                    |
| xml_etree_parse      | 59.3 ms                                                                  | 61.4 ms: 1.04x slower                                                    |
| xml_etree_iterparse  | 37.8 ms                                                                  | 41.0 ms: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.28 ms                                                                  | 7.43 ms: 1.02x slower                                                    |
| python_startup         | 9.98 ms                                                                  | 10.2 ms: 1.03x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 22.4 ms                                                                  | 22.5 ms: 1.00x slower                                                    |
| django_template | 15.6 ms                                                                  | 15.7 ms: 1.01x slower                                                    |
| mako            | 5.53 ms                                                                  | 5.58 ms: 1.01x slower                                                    |
| genshi_text     | 11.0 ms                                                                  | 11.2 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                    | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| fannkuch                         | 173 ms                                                                   | 169 ms: 1.03x faster                                                     |
| connected_components             | 303 ms                                                                   | 297 ms: 1.02x faster                                                     |
| json_dumps                       | 3.92 ms                                                                  | 3.84 ms: 1.02x faster                                                    |
| logging_silent                   | 44.3 ns                                                                  | 43.6 ns: 1.01x faster                                                    |
| tomli_loads                      | 857 ms                                                                   | 846 ms: 1.01x faster                                                     |
| nqueens                          | 40.9 ms                                                                  | 40.5 ms: 1.01x faster                                                    |
| sqlite_synth                     | 798 ns                                                                   | 791 ns: 1.01x faster                                                     |
| pprint_safe_repr                 | 331 ms                                                                   | 328 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 107 us                                                                   | 107 us: 1.01x faster                                                     |
| richards                         | 22.9 ms                                                                  | 22.8 ms: 1.01x faster                                                    |
| richards_super                   | 26.1 ms                                                                  | 26.0 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 2.14 ms                                                                  | 2.13 ms: 1.01x faster                                                    |
| deepcopy_memo                    | 12.6 us                                                                  | 12.6 us: 1.01x faster                                                    |
| nbody                            | 56.1 ms                                                                  | 55.8 ms: 1.01x faster                                                    |
| comprehensions                   | 8.25 us                                                                  | 8.22 us: 1.00x faster                                                    |
| regex_v8                         | 9.26 ms                                                                  | 9.23 ms: 1.00x faster                                                    |
| pprint_pformat                   | 674 ms                                                                   | 672 ms: 1.00x faster                                                     |
| hexiom                           | 3.16 ms                                                                  | 3.17 ms: 1.00x slower                                                    |
| regex_compile                    | 50.6 ms                                                                  | 50.7 ms: 1.00x slower                                                    |
| raytrace                         | 127 ms                                                                   | 127 ms: 1.00x slower                                                     |
| genshi_xml                       | 22.4 ms                                                                  | 22.5 ms: 1.00x slower                                                    |
| crypto_pyaes                     | 42.6 ms                                                                  | 42.8 ms: 1.00x slower                                                    |
| sqlglot_v2_transpile             | 710 us                                                                   | 713 us: 1.00x slower                                                     |
| sqlglot_v2_normalize             | 48.3 ms                                                                  | 48.6 ms: 1.00x slower                                                    |
| sqlglot_v2_optimize              | 23.8 ms                                                                  | 23.9 ms: 1.01x slower                                                    |
| sphinx                           | 422 ms                                                                   | 424 ms: 1.01x slower                                                     |
| float                            | 28.7 ms                                                                  | 28.9 ms: 1.01x slower                                                    |
| sympy_expand                     | 188 ms                                                                   | 189 ms: 1.01x slower                                                     |
| typing_runtime_protocols         | 72.5 us                                                                  | 72.9 us: 1.01x slower                                                    |
| bpe_tokeniser                    | 1.95 sec                                                                 | 1.96 sec: 1.01x slower                                                   |
| coverage                         | 38.7 ms                                                                  | 39.0 ms: 1.01x slower                                                    |
| pickle_pure_python               | 146 us                                                                   | 147 us: 1.01x slower                                                     |
| xml_etree_process                | 26.8 ms                                                                  | 27.0 ms: 1.01x slower                                                    |
| coroutines                       | 10.1 ms                                                                  | 10.2 ms: 1.01x slower                                                    |
| xml_etree_generate               | 37.2 ms                                                                  | 37.5 ms: 1.01x slower                                                    |
| scimark_sor                      | 55.1 ms                                                                  | 55.5 ms: 1.01x slower                                                    |
| django_template                  | 15.6 ms                                                                  | 15.7 ms: 1.01x slower                                                    |
| mako                             | 5.53 ms                                                                  | 5.58 ms: 1.01x slower                                                    |
| pycparser                        | 457 ms                                                                   | 461 ms: 1.01x slower                                                     |
| mdp                              | 608 ms                                                                   | 614 ms: 1.01x slower                                                     |
| deepcopy                         | 106 us                                                                   | 107 us: 1.01x slower                                                     |
| pyflate                          | 193 ms                                                                   | 194 ms: 1.01x slower                                                     |
| k_core                           | 988 ms                                                                   | 997 ms: 1.01x slower                                                     |
| chaos                            | 26.7 ms                                                                  | 27.0 ms: 1.01x slower                                                    |
| genshi_text                      | 11.0 ms                                                                  | 11.2 ms: 1.01x slower                                                    |
| asyncio_websockets               | 184 ms                                                                   | 186 ms: 1.01x slower                                                     |
| go                               | 59.6 ms                                                                  | 60.2 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                                   | 125 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                                  | 1.97 ms: 1.01x slower                                                    |
| async_tree_eager_memoization     | 112 ms                                                                   | 114 ms: 1.01x slower                                                     |
| async_tree_none_tg               | 106 ms                                                                   | 108 ms: 1.01x slower                                                     |
| docutils                         | 1.00 sec                                                                 | 1.01 sec: 1.01x slower                                                   |
| subparsers                       | 4.05 ms                                                                  | 4.11 ms: 1.01x slower                                                    |
| async_tree_eager                 | 46.3 ms                                                                  | 46.9 ms: 1.01x slower                                                    |
| json_loads                       | 11.2 us                                                                  | 11.4 us: 1.01x slower                                                    |
| logging_simple                   | 2.35 us                                                                  | 2.39 us: 1.02x slower                                                    |
| meteor_contest                   | 55.1 ms                                                                  | 56.1 ms: 1.02x slower                                                    |
| deltablue                        | 1.63 ms                                                                  | 1.66 ms: 1.02x slower                                                    |
| create_gc_cycles                 | 503 us                                                                   | 512 us: 1.02x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 221 ms                                                                   | 225 ms: 1.02x slower                                                     |
| dulwich_log                      | 18.5 ms                                                                  | 18.8 ms: 1.02x slower                                                    |
| scimark_lu                       | 58.1 ms                                                                  | 59.1 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg       | 255 ms                                                                   | 259 ms: 1.02x slower                                                     |
| async_tree_eager_tg              | 92.4 ms                                                                  | 94.2 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 243 ms                                                                   | 248 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed          | 260 ms                                                                   | 265 ms: 1.02x slower                                                     |
| 2to3                             | 120 ms                                                                   | 123 ms: 1.02x slower                                                     |
| logging_format                   | 2.63 us                                                                  | 2.68 us: 1.02x slower                                                    |
| python_startup_no_site           | 7.28 ms                                                                  | 7.43 ms: 1.02x slower                                                    |
| many_optionals                   | 262 us                                                                   | 267 us: 1.02x slower                                                     |
| generators                       | 21.2 ms                                                                  | 21.6 ms: 1.02x slower                                                    |
| html5lib                         | 22.6 ms                                                                  | 23.1 ms: 1.02x slower                                                    |
| async_generators                 | 184 ms                                                                   | 188 ms: 1.02x slower                                                     |
| python_startup                   | 9.98 ms                                                                  | 10.2 ms: 1.03x slower                                                    |
| bench_mp_pool                    | 46.8 ms                                                                  | 48.1 ms: 1.03x slower                                                    |
| spectral_norm                    | 48.6 ms                                                                  | 50.0 ms: 1.03x slower                                                    |
| pidigits                         | 164 ms                                                                   | 169 ms: 1.03x slower                                                     |
| xml_etree_parse                  | 59.3 ms                                                                  | 61.4 ms: 1.04x slower                                                    |
| gc_traversal                     | 792 us                                                                   | 823 us: 1.04x slower                                                     |
| xml_etree_iterparse              | 37.8 ms                                                                  | 41.0 ms: 1.08x slower                                                    |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (23): sympy_str, pathlib, sympy_sum, dask, thrift, telco, sympy_integrate, scimark_monte_carlo, sqlglot_v2_parse, shortest_path, bench_thread_pool, regex_effbot, regex_dna, deepcopy_reduce, async_tree_memoization_tg, async_tree_io_tg, async_tree_memoization, async_tree_io, pylint, async_tree_eager_memoization_tg, async_tree_eager_io_tg, async_tree_eager_io, async_tree_none
Ignored benchmarks (6) of results/bm-20260307-3.15.0a6+-149c465-NOGIL/bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465.json: pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x