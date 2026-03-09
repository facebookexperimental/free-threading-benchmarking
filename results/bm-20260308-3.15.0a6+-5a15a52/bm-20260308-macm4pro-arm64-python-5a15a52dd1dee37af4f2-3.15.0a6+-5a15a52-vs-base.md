# Results vs. base

- fork: python
- ref: 5a15a52dd1dee37af4f2
- machine: darwin-arm64
- commit hash: 5a15a52
- commit date: 2026-03-08
- overall geometric mean: 1.014x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 117 ms                                                                   | 120 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                                 | 1.05 sec: 1.03x slower                                                   |
| html5lib       | 21.9 ms                                                                  | 22.4 ms: 1.02x slower                                                    |
| sphinx         | 397 ms                                                                   | 407 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager                 | 41.8 ms                                                                  | 42.0 ms: 1.00x slower                                                    |
| async_tree_eager_memoization     | 107 ms                                                                   | 108 ms: 1.01x slower                                                     |
| async_tree_none_tg               | 101 ms                                                                   | 103 ms: 1.02x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 238 ms                                                                   | 242 ms: 1.02x slower                                                     |
| async_tree_eager_tg              | 83.5 ms                                                                  | 84.8 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed          | 251 ms                                                                   | 255 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 250 ms                                                                   | 254 ms: 1.02x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                   | 223 ms: 1.02x slower                                                     |
| async_tree_io                    | 238 ms                                                                   | 243 ms: 1.02x slower                                                     |
| async_tree_none                  | 103 ms                                                                   | 105 ms: 1.02x slower                                                     |
| async_generators                 | 177 ms                                                                   | 181 ms: 1.02x slower                                                     |
| async_tree_io_tg                 | 227 ms                                                                   | 233 ms: 1.03x slower                                                     |
| async_tree_eager_io              | 226 ms                                                                   | 233 ms: 1.03x slower                                                     |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (5): async_tree_eager_io_tg, coroutines, async_tree_eager_memoization_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 28.1 ms                                                                  | 28.4 ms: 1.01x slower                                                    |
| pidigits       | 160 ms                                                                   | 168 ms: 1.04x slower                                                     |
| nbody          | 46.4 ms                                                                  | 48.8 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.44 ms                                                                  | 1.46 ms: 1.01x slower                                                    |
| regex_compile  | 47.6 ms                                                                  | 48.0 ms: 1.01x slower                                                    |
| regex_v8       | 9.62 ms                                                                  | 9.75 ms: 1.01x slower                                                    |
| regex_dna      | 94.7 ms                                                                  | 96.8 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|---------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads         | 855 ms                                                                   | 862 ms: 1.01x slower                                                     |
| pickle_pure_python  | 145 us                                                                   | 146 us: 1.01x slower                                                     |
| xml_etree_process   | 25.3 ms                                                                  | 25.6 ms: 1.01x slower                                                    |
| xml_etree_generate  | 35.6 ms                                                                  | 36.0 ms: 1.01x slower                                                    |
| json_loads          | 10.6 us                                                                  | 10.9 us: 1.02x slower                                                    |
| xml_etree_iterparse | 39.7 ms                                                                  | 40.5 ms: 1.02x slower                                                    |
| json_dumps          | 3.78 ms                                                                  | 3.89 ms: 1.03x slower                                                    |
| xml_etree_parse     | 60.7 ms                                                                  | 63.8 ms: 1.05x slower                                                    |
| Geometric mean      | (ref)                                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 6.36 ms                                                                  | 6.54 ms: 1.03x slower                                                    |
| python_startup         | 8.79 ms                                                                  | 9.06 ms: 1.03x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 15.2 ms                                                                  | 15.3 ms: 1.00x slower                                                    |
| genshi_xml      | 21.9 ms                                                                  | 22.1 ms: 1.01x slower                                                    |
| genshi_text     | 10.1 ms                                                                  | 10.3 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| sqlite_synth                     | 956 ns                                                                   | 949 ns: 1.01x faster                                                     |
| scimark_sor                      | 50.8 ms                                                                  | 50.4 ms: 1.01x faster                                                    |
| connected_components             | 211 ms                                                                   | 212 ms: 1.00x slower                                                     |
| shortest_path                    | 227 ms                                                                   | 228 ms: 1.00x slower                                                     |
| k_core                           | 909 ms                                                                   | 911 ms: 1.00x slower                                                     |
| django_template                  | 15.2 ms                                                                  | 15.3 ms: 1.00x slower                                                    |
| spectral_norm                    | 44.0 ms                                                                  | 44.3 ms: 1.00x slower                                                    |
| scimark_sparse_mat_mult          | 1.88 ms                                                                  | 1.89 ms: 1.00x slower                                                    |
| async_tree_eager                 | 41.8 ms                                                                  | 42.0 ms: 1.00x slower                                                    |
| sqlglot_v2_normalize             | 47.5 ms                                                                  | 47.8 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 324 ms                                                                   | 326 ms: 1.01x slower                                                     |
| tomli_loads                      | 855 ms                                                                   | 862 ms: 1.01x slower                                                     |
| sympy_expand                     | 173 ms                                                                   | 174 ms: 1.01x slower                                                     |
| async_tree_eager_memoization     | 107 ms                                                                   | 108 ms: 1.01x slower                                                     |
| raytrace                         | 120 ms                                                                   | 121 ms: 1.01x slower                                                     |
| pickle_pure_python               | 145 us                                                                   | 146 us: 1.01x slower                                                     |
| regex_effbot                     | 1.44 ms                                                                  | 1.46 ms: 1.01x slower                                                    |
| fannkuch                         | 170 ms                                                                   | 171 ms: 1.01x slower                                                     |
| xml_etree_process                | 25.3 ms                                                                  | 25.6 ms: 1.01x slower                                                    |
| subparsers                       | 4.10 ms                                                                  | 4.14 ms: 1.01x slower                                                    |
| deltablue                        | 1.51 ms                                                                  | 1.53 ms: 1.01x slower                                                    |
| nqueens                          | 37.5 ms                                                                  | 37.9 ms: 1.01x slower                                                    |
| float                            | 28.1 ms                                                                  | 28.4 ms: 1.01x slower                                                    |
| regex_compile                    | 47.6 ms                                                                  | 48.0 ms: 1.01x slower                                                    |
| mdp                              | 550 ms                                                                   | 555 ms: 1.01x slower                                                     |
| chaos                            | 25.3 ms                                                                  | 25.6 ms: 1.01x slower                                                    |
| deepcopy                         | 99.8 us                                                                  | 101 us: 1.01x slower                                                     |
| deepcopy_memo                    | 11.7 us                                                                  | 11.8 us: 1.01x slower                                                    |
| richards                         | 20.8 ms                                                                  | 21.0 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 65.6 us                                                                  | 66.3 us: 1.01x slower                                                    |
| xml_etree_generate               | 35.6 ms                                                                  | 36.0 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.9 ms                                                                  | 22.1 ms: 1.01x slower                                                    |
| thrift                           | 313 us                                                                   | 317 us: 1.01x slower                                                     |
| scimark_fft                      | 120 ms                                                                   | 122 ms: 1.01x slower                                                     |
| regex_v8                         | 9.62 ms                                                                  | 9.75 ms: 1.01x slower                                                    |
| hexiom                           | 2.85 ms                                                                  | 2.89 ms: 1.01x slower                                                    |
| deepcopy_reduce                  | 1.09 us                                                                  | 1.11 us: 1.01x slower                                                    |
| scimark_monte_carlo              | 28.7 ms                                                                  | 29.1 ms: 1.01x slower                                                    |
| sqlglot_v2_parse                 | 525 us                                                                   | 532 us: 1.01x slower                                                     |
| pprint_pformat                   | 657 ms                                                                   | 667 ms: 1.01x slower                                                     |
| async_tree_none_tg               | 101 ms                                                                   | 103 ms: 1.02x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 238 ms                                                                   | 242 ms: 1.02x slower                                                     |
| json                             | 1.87 ms                                                                  | 1.90 ms: 1.02x slower                                                    |
| sqlglot_v2_transpile             | 643 us                                                                   | 653 us: 1.02x slower                                                     |
| async_tree_eager_tg              | 83.5 ms                                                                  | 84.8 ms: 1.02x slower                                                    |
| richards_super                   | 23.3 ms                                                                  | 23.7 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed          | 251 ms                                                                   | 255 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 250 ms                                                                   | 254 ms: 1.02x slower                                                     |
| sympy_str                        | 102 ms                                                                   | 104 ms: 1.02x slower                                                     |
| go                               | 55.7 ms                                                                  | 56.6 ms: 1.02x slower                                                    |
| logging_format                   | 2.43 us                                                                  | 2.47 us: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                   | 223 ms: 1.02x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                                  | 39.5 ms: 1.02x slower                                                    |
| async_tree_io                    | 238 ms                                                                   | 243 ms: 1.02x slower                                                     |
| bpe_tokeniser                    | 1.96 sec                                                                 | 1.99 sec: 1.02x slower                                                   |
| pyflate                          | 188 ms                                                                   | 191 ms: 1.02x slower                                                     |
| async_tree_none                  | 103 ms                                                                   | 105 ms: 1.02x slower                                                     |
| json_loads                       | 10.6 us                                                                  | 10.9 us: 1.02x slower                                                    |
| scimark_lu                       | 46.4 ms                                                                  | 47.3 ms: 1.02x slower                                                    |
| sympy_integrate                  | 7.58 ms                                                                  | 7.74 ms: 1.02x slower                                                    |
| pycparser                        | 469 ms                                                                   | 479 ms: 1.02x slower                                                     |
| xml_etree_iterparse              | 39.7 ms                                                                  | 40.5 ms: 1.02x slower                                                    |
| sympy_sum                        | 56.6 ms                                                                  | 57.9 ms: 1.02x slower                                                    |
| dulwich_log                      | 18.8 ms                                                                  | 19.2 ms: 1.02x slower                                                    |
| logging_silent                   | 42.3 ns                                                                  | 43.3 ns: 1.02x slower                                                    |
| genshi_text                      | 10.1 ms                                                                  | 10.3 ms: 1.02x slower                                                    |
| async_generators                 | 177 ms                                                                   | 181 ms: 1.02x slower                                                     |
| pathlib                          | 10.7 ms                                                                  | 11.0 ms: 1.02x slower                                                    |
| 2to3                             | 117 ms                                                                   | 120 ms: 1.02x slower                                                     |
| regex_dna                        | 94.7 ms                                                                  | 96.8 ms: 1.02x slower                                                    |
| logging_simple                   | 2.21 us                                                                  | 2.26 us: 1.02x slower                                                    |
| generators                       | 20.7 ms                                                                  | 21.2 ms: 1.02x slower                                                    |
| html5lib                         | 21.9 ms                                                                  | 22.4 ms: 1.02x slower                                                    |
| sphinx                           | 397 ms                                                                   | 407 ms: 1.02x slower                                                     |
| python_startup_no_site           | 6.36 ms                                                                  | 6.54 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                                 | 1.05 sec: 1.03x slower                                                   |
| async_tree_io_tg                 | 227 ms                                                                   | 233 ms: 1.03x slower                                                     |
| meteor_contest                   | 49.7 ms                                                                  | 51.1 ms: 1.03x slower                                                    |
| bench_mp_pool                    | 45.1 ms                                                                  | 46.4 ms: 1.03x slower                                                    |
| python_startup                   | 8.79 ms                                                                  | 9.06 ms: 1.03x slower                                                    |
| async_tree_eager_io              | 226 ms                                                                   | 233 ms: 1.03x slower                                                     |
| json_dumps                       | 3.78 ms                                                                  | 3.89 ms: 1.03x slower                                                    |
| many_optionals                   | 252 us                                                                   | 260 us: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                                  | 2.08 ms: 1.03x slower                                                    |
| create_gc_cycles                 | 893 us                                                                   | 931 us: 1.04x slower                                                     |
| pidigits                         | 160 ms                                                                   | 168 ms: 1.04x slower                                                     |
| xml_etree_parse                  | 60.7 ms                                                                  | 63.8 ms: 1.05x slower                                                    |
| nbody                            | 46.4 ms                                                                  | 48.8 ms: 1.05x slower                                                    |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (14): comprehensions, mako, telco, dask, async_tree_eager_io_tg, coroutines, coverage, bench_thread_pool, unpickle_pure_python, sqlglot_v2_optimize, async_tree_eager_memoization_tg, async_tree_memoization, async_tree_memoization_tg, pylint
Ignored benchmarks (6) of results/bm-20260307-3.15.0a6+-149c465/bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465.json: pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.014x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.00x