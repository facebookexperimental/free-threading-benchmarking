# Results vs. default_base_vs_NOGIL

- fork: python
- ref: 5a15a52dd1dee37af4f2
- machine: darwin-arm64
- commit hash: 5a15a52
- commit date: 2026-03-08
- overall geometric mean: 1.049x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 117 ms                                                                   | 123 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 21.9 ms                                                                  | 23.1 ms: 1.06x slower                                                    |
| sphinx         | 397 ms                                                                   | 424 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                                    | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                       | 10.6 ms                                                                  | 10.2 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                   | 225 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 250 ms                                                                   | 259 ms: 1.04x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 238 ms                                                                   | 248 ms: 1.04x slower                                                     |
| async_tree_cpu_io_mixed          | 251 ms                                                                   | 265 ms: 1.06x slower                                                     |
| async_tree_io_tg                 | 227 ms                                                                   | 240 ms: 1.06x slower                                                     |
| async_generators                 | 177 ms                                                                   | 188 ms: 1.06x slower                                                     |
| async_tree_memoization_tg        | 137 ms                                                                   | 145 ms: 1.06x slower                                                     |
| async_tree_io                    | 238 ms                                                                   | 253 ms: 1.06x slower                                                     |
| async_tree_eager_memoization     | 107 ms                                                                   | 114 ms: 1.06x slower                                                     |
| async_tree_none_tg               | 101 ms                                                                   | 108 ms: 1.07x slower                                                     |
| async_tree_eager_memoization_tg  | 120 ms                                                                   | 129 ms: 1.08x slower                                                     |
| async_tree_memoization           | 138 ms                                                                   | 152 ms: 1.10x slower                                                     |
| async_tree_eager_io_tg           | 224 ms                                                                   | 249 ms: 1.11x slower                                                     |
| async_tree_eager_io              | 226 ms                                                                   | 253 ms: 1.12x slower                                                     |
| async_tree_none                  | 103 ms                                                                   | 115 ms: 1.12x slower                                                     |
| async_tree_eager                 | 41.8 ms                                                                  | 46.9 ms: 1.12x slower                                                    |
| async_tree_eager_tg              | 83.5 ms                                                                  | 94.2 ms: 1.13x slower                                                    |
| Geometric mean                   | (ref)                                                                    | 1.07x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 28.1 ms                                                                  | 28.9 ms: 1.03x slower                                                    |
| pidigits       | 160 ms                                                                   | 169 ms: 1.05x slower                                                     |
| nbody          | 46.4 ms                                                                  | 55.8 ms: 1.20x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.09x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 9.62 ms                                                                  | 9.23 ms: 1.04x faster                                                    |
| regex_effbot   | 1.44 ms                                                                  | 1.46 ms: 1.01x slower                                                    |
| regex_dna      | 94.7 ms                                                                  | 96.0 ms: 1.01x slower                                                    |
| regex_compile  | 47.6 ms                                                                  | 50.7 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 855 ms                                                                   | 846 ms: 1.01x faster                                                     |
| xml_etree_parse      | 60.7 ms                                                                  | 61.4 ms: 1.01x slower                                                    |
| json_dumps           | 3.78 ms                                                                  | 3.84 ms: 1.02x slower                                                    |
| pickle_pure_python   | 145 us                                                                   | 147 us: 1.02x slower                                                     |
| xml_etree_iterparse  | 39.7 ms                                                                  | 41.0 ms: 1.03x slower                                                    |
| unpickle_pure_python | 102 us                                                                   | 107 us: 1.05x slower                                                     |
| xml_etree_generate   | 35.6 ms                                                                  | 37.5 ms: 1.05x slower                                                    |
| xml_etree_process    | 25.3 ms                                                                  | 27.0 ms: 1.06x slower                                                    |
| json_loads           | 10.6 us                                                                  | 11.4 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                                    | 1.03x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.79 ms                                                                  | 10.2 ms: 1.16x slower                                                    |
| python_startup_no_site | 6.36 ms                                                                  | 7.43 ms: 1.17x slower                                                    |
| Geometric mean         | (ref)                                                                    | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.9 ms                                                                  | 22.5 ms: 1.03x slower                                                    |
| django_template | 15.2 ms                                                                  | 15.7 ms: 1.03x slower                                                    |
| genshi_text     | 10.1 ms                                                                  | 11.2 ms: 1.11x slower                                                    |
| mako            | 4.84 ms                                                                  | 5.58 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                                    | 1.08x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                                  | 823 us: 2.45x faster                                                     |
| create_gc_cycles                 | 893 us                                                                   | 512 us: 1.74x faster                                                     |
| sqlite_synth                     | 956 ns                                                                   | 791 ns: 1.21x faster                                                     |
| regex_v8                         | 9.62 ms                                                                  | 9.23 ms: 1.04x faster                                                    |
| coroutines                       | 10.6 ms                                                                  | 10.2 ms: 1.03x faster                                                    |
| pycparser                        | 469 ms                                                                   | 461 ms: 1.02x faster                                                     |
| tomli_loads                      | 855 ms                                                                   | 846 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                                 | 1.01 sec: 1.01x faster                                                   |
| bpe_tokeniser                    | 1.96 sec                                                                 | 1.96 sec: 1.00x slower                                                   |
| dask                             | 522 ms                                                                   | 528 ms: 1.01x slower                                                     |
| xml_etree_parse                  | 60.7 ms                                                                  | 61.4 ms: 1.01x slower                                                    |
| regex_effbot                     | 1.44 ms                                                                  | 1.46 ms: 1.01x slower                                                    |
| regex_dna                        | 94.7 ms                                                                  | 96.0 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 324 ms                                                                   | 328 ms: 1.01x slower                                                     |
| json_dumps                       | 3.78 ms                                                                  | 3.84 ms: 1.02x slower                                                    |
| pickle_pure_python               | 145 us                                                                   | 147 us: 1.02x slower                                                     |
| sqlglot_v2_normalize             | 47.5 ms                                                                  | 48.6 ms: 1.02x slower                                                    |
| pprint_pformat                   | 657 ms                                                                   | 672 ms: 1.02x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 219 ms                                                                   | 225 ms: 1.02x slower                                                     |
| float                            | 28.1 ms                                                                  | 28.9 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.9 ms                                                                  | 22.5 ms: 1.03x slower                                                    |
| logging_silent                   | 42.3 ns                                                                  | 43.6 ns: 1.03x slower                                                    |
| django_template                  | 15.2 ms                                                                  | 15.7 ms: 1.03x slower                                                    |
| pylint                           | 116 ms                                                                   | 120 ms: 1.03x slower                                                     |
| xml_etree_iterparse              | 39.7 ms                                                                  | 41.0 ms: 1.03x slower                                                    |
| sqlglot_v2_optimize              | 23.1 ms                                                                  | 23.9 ms: 1.04x slower                                                    |
| pyflate                          | 188 ms                                                                   | 194 ms: 1.04x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 250 ms                                                                   | 259 ms: 1.04x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 238 ms                                                                   | 248 ms: 1.04x slower                                                     |
| generators                       | 20.7 ms                                                                  | 21.6 ms: 1.04x slower                                                    |
| scimark_fft                      | 120 ms                                                                   | 125 ms: 1.04x slower                                                     |
| unpickle_pure_python             | 102 us                                                                   | 107 us: 1.05x slower                                                     |
| 2to3                             | 117 ms                                                                   | 123 ms: 1.05x slower                                                     |
| deepcopy_reduce                  | 1.09 us                                                                  | 1.15 us: 1.05x slower                                                    |
| json                             | 1.87 ms                                                                  | 1.97 ms: 1.05x slower                                                    |
| pidigits                         | 160 ms                                                                   | 169 ms: 1.05x slower                                                     |
| xml_etree_generate               | 35.6 ms                                                                  | 37.5 ms: 1.05x slower                                                    |
| telco                            | 2.85 ms                                                                  | 3.00 ms: 1.05x slower                                                    |
| html5lib                         | 21.9 ms                                                                  | 23.1 ms: 1.06x slower                                                    |
| async_tree_cpu_io_mixed          | 251 ms                                                                   | 265 ms: 1.06x slower                                                     |
| async_tree_io_tg                 | 227 ms                                                                   | 240 ms: 1.06x slower                                                     |
| raytrace                         | 120 ms                                                                   | 127 ms: 1.06x slower                                                     |
| async_generators                 | 177 ms                                                                   | 188 ms: 1.06x slower                                                     |
| async_tree_memoization_tg        | 137 ms                                                                   | 145 ms: 1.06x slower                                                     |
| async_tree_io                    | 238 ms                                                                   | 253 ms: 1.06x slower                                                     |
| many_optionals                   | 252 us                                                                   | 267 us: 1.06x slower                                                     |
| async_tree_eager_memoization     | 107 ms                                                                   | 114 ms: 1.06x slower                                                     |
| xml_etree_process                | 25.3 ms                                                                  | 27.0 ms: 1.06x slower                                                    |
| regex_compile                    | 47.6 ms                                                                  | 50.7 ms: 1.07x slower                                                    |
| async_tree_none_tg               | 101 ms                                                                   | 108 ms: 1.07x slower                                                     |
| bench_mp_pool                    | 45.1 ms                                                                  | 48.1 ms: 1.07x slower                                                    |
| chaos                            | 25.3 ms                                                                  | 27.0 ms: 1.07x slower                                                    |
| json_loads                       | 10.6 us                                                                  | 11.4 us: 1.07x slower                                                    |
| sphinx                           | 397 ms                                                                   | 424 ms: 1.07x slower                                                     |
| deepcopy                         | 99.8 us                                                                  | 107 us: 1.07x slower                                                     |
| deepcopy_memo                    | 11.7 us                                                                  | 12.6 us: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 120 ms                                                                   | 129 ms: 1.08x slower                                                     |
| nqueens                          | 37.5 ms                                                                  | 40.5 ms: 1.08x slower                                                    |
| logging_simple                   | 2.21 us                                                                  | 2.39 us: 1.08x slower                                                    |
| sympy_integrate                  | 7.58 ms                                                                  | 8.20 ms: 1.08x slower                                                    |
| go                               | 55.7 ms                                                                  | 60.2 ms: 1.08x slower                                                    |
| sympy_str                        | 102 ms                                                                   | 111 ms: 1.08x slower                                                     |
| comprehensions                   | 7.57 us                                                                  | 8.22 us: 1.09x slower                                                    |
| sympy_sum                        | 56.6 ms                                                                  | 61.5 ms: 1.09x slower                                                    |
| thrift                           | 313 us                                                                   | 341 us: 1.09x slower                                                     |
| sqlglot_v2_parse                 | 525 us                                                                   | 572 us: 1.09x slower                                                     |
| scimark_sor                      | 50.8 ms                                                                  | 55.5 ms: 1.09x slower                                                    |
| sympy_expand                     | 173 ms                                                                   | 189 ms: 1.09x slower                                                     |
| richards                         | 20.8 ms                                                                  | 22.8 ms: 1.10x slower                                                    |
| k_core                           | 909 ms                                                                   | 997 ms: 1.10x slower                                                     |
| async_tree_memoization           | 138 ms                                                                   | 152 ms: 1.10x slower                                                     |
| deltablue                        | 1.51 ms                                                                  | 1.66 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                                  | 42.8 ms: 1.10x slower                                                    |
| logging_format                   | 2.43 us                                                                  | 2.68 us: 1.10x slower                                                    |
| genshi_text                      | 10.1 ms                                                                  | 11.2 ms: 1.11x slower                                                    |
| sqlglot_v2_transpile             | 643 us                                                                   | 713 us: 1.11x slower                                                     |
| hexiom                           | 2.85 ms                                                                  | 3.17 ms: 1.11x slower                                                    |
| async_tree_eager_io_tg           | 224 ms                                                                   | 249 ms: 1.11x slower                                                     |
| typing_runtime_protocols         | 65.6 us                                                                  | 72.9 us: 1.11x slower                                                    |
| richards_super                   | 23.3 ms                                                                  | 26.0 ms: 1.11x slower                                                    |
| mdp                              | 550 ms                                                                   | 614 ms: 1.12x slower                                                     |
| async_tree_eager_io              | 226 ms                                                                   | 253 ms: 1.12x slower                                                     |
| shortest_path                    | 227 ms                                                                   | 255 ms: 1.12x slower                                                     |
| async_tree_none                  | 103 ms                                                                   | 115 ms: 1.12x slower                                                     |
| async_tree_eager                 | 41.8 ms                                                                  | 46.9 ms: 1.12x slower                                                    |
| async_tree_eager_tg              | 83.5 ms                                                                  | 94.2 ms: 1.13x slower                                                    |
| meteor_contest                   | 49.7 ms                                                                  | 56.1 ms: 1.13x slower                                                    |
| spectral_norm                    | 44.0 ms                                                                  | 50.0 ms: 1.13x slower                                                    |
| scimark_sparse_mat_mult          | 1.88 ms                                                                  | 2.13 ms: 1.13x slower                                                    |
| scimark_monte_carlo              | 28.7 ms                                                                  | 32.6 ms: 1.13x slower                                                    |
| mako                             | 4.84 ms                                                                  | 5.58 ms: 1.15x slower                                                    |
| python_startup                   | 8.79 ms                                                                  | 10.2 ms: 1.16x slower                                                    |
| python_startup_no_site           | 6.36 ms                                                                  | 7.43 ms: 1.17x slower                                                    |
| nbody                            | 46.4 ms                                                                  | 55.8 ms: 1.20x slower                                                    |
| coverage                         | 32.1 ms                                                                  | 39.0 ms: 1.21x slower                                                    |
| scimark_lu                       | 46.4 ms                                                                  | 59.1 ms: 1.28x slower                                                    |
| bench_thread_pool                | 435 us                                                                   | 586 us: 1.35x slower                                                     |
| connected_components             | 211 ms                                                                   | 297 ms: 1.40x slower                                                     |
| Geometric mean                   | (ref)                                                                    | 1.05x slower                                                             |

Benchmark hidden because not significant (4): fannkuch, pathlib, subparsers, dulwich_log
Ignored benchmarks (6) of results/bm-20260307-3.15.0a6+-149c465/bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6+-149c465.json: pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (1) of results/bm-20260308-3.15.0a6+-5a15a52-NOGIL/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52.json: asyncio_websockets

- Geometric mean (including insignificant results): 1.049x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.11x