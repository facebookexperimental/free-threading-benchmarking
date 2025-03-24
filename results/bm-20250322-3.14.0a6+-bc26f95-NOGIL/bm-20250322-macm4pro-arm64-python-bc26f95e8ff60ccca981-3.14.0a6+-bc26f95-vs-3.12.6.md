# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: darwin-arm64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.015x slower
- HPT reliability: 99.48%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 132 ms: 1.16x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.5 ms: 1.06x slower                                                    |
| sphinx         | 434 ms                                                   | 437 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.06x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.14x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 233 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 240 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.1 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 244 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.9 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 121 ms: 1.09x faster                                                     |
| async_generators                 | 206 ms                                                   | 191 ms: 1.08x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 230 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 56.3 ms: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 36.2 ms: 1.05x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 78.1 ms: 1.44x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 59.1 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.5 ms: 1.20x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 40.8 ms: 1.05x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.08 sec: 1.13x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 30.4 ms: 1.14x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 169 us: 1.22x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.20 ms: 1.22x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 128 us: 1.24x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.20 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.24 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 26.3 ms: 1.21x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 13.1 ms: 1.25x slower                                                    |
| mako            | 4.77 ms                                                  | 6.17 ms: 1.29x slower                                                    |
| django_template | 13.6 ms                                                  | 18.4 ms: 1.35x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.27x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.40 ms: 2.21x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 925 us: 2.17x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.14x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 233 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 240 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.1 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 499 us: 1.66x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 244 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 254 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| deepcopy                         | 161 us                                                   | 129 us: 1.25x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 56.5 ms: 1.20x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 835 ns: 1.16x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.9 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 121 ms: 1.09x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                    |
| async_generators                 | 206 ms                                                   | 191 ms: 1.08x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 17.2 us: 1.07x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.7 ms: 1.05x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.06 sec: 1.05x faster                                                   |
| float                            | 37.9 ms                                                  | 36.2 ms: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.40 us: 1.05x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 230 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                     |
| generators                       | 21.9 ms                                                  | 22.1 ms: 1.01x slower                                                    |
| sphinx                           | 434 ms                                                   | 437 ms: 1.01x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 40.1 ms: 1.01x slower                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.26 sec: 1.01x slower                                                   |
| pycparser                        | 497 ms                                                   | 505 ms: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                   |
| comprehensions                   | 9.84 us                                                  | 10.2 us: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.03x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 40.8 ms: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.5 ms: 1.06x slower                                                    |
| go                               | 70.0 ms                                                  | 74.7 ms: 1.07x slower                                                    |
| pyflate                          | 216 ms                                                   | 232 ms: 1.08x slower                                                     |
| thrift                           | 322 us                                                   | 347 us: 1.08x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 59.1 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                     |
| spectral_norm                    | 54.4 ms                                                  | 59.5 ms: 1.09x slower                                                    |
| mdp                              | 1.09 sec                                                 | 1.20 sec: 1.10x slower                                                   |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.3 ms: 1.10x slower                                                    |
| logging_silent                   | 50.9 ns                                                  | 56.1 ns: 1.10x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 63.8 ms: 1.11x slower                                                    |
| raytrace                         | 145 ms                                                   | 161 ms: 1.11x slower                                                     |
| logging_format                   | 2.80 us                                                  | 3.15 us: 1.13x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.89 us: 1.13x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.08 sec: 1.13x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 49.2 ms: 1.13x slower                                                    |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.87 ms: 1.13x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 9.11 ms: 1.14x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 30.4 ms: 1.14x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 162 ms: 1.14x slower                                                     |
| scimark_sor                      | 61.0 ms                                                  | 69.9 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.20 ms: 1.15x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 81.5 us: 1.15x slower                                                    |
| chaos                            | 28.9 ms                                                  | 33.3 ms: 1.15x slower                                                    |
| sympy_str                        | 104 ms                                                   | 120 ms: 1.15x slower                                                     |
| 2to3                             | 114 ms                                                   | 132 ms: 1.16x slower                                                     |
| connected_components             | 201 ms                                                   | 236 ms: 1.18x slower                                                     |
| deltablue                        | 1.73 ms                                                  | 2.04 ms: 1.18x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.47 ms: 1.19x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 46.7 ms: 1.20x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 26.3 ms: 1.21x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 203 ms: 1.22x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 169 us: 1.22x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.20 ms: 1.22x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 31.3 ms: 1.23x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 56.3 ms: 1.24x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 128 us: 1.24x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 59.3 ms: 1.24x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 40.1 ms: 1.24x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 13.1 ms: 1.25x slower                                                    |
| richards                         | 22.4 ms                                                  | 28.1 ms: 1.25x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 413 ms: 1.26x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 840 ms: 1.26x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.24 ms: 1.27x slower                                                    |
| fannkuch                         | 176 ms                                                   | 225 ms: 1.28x slower                                                     |
| mako                             | 4.77 ms                                                  | 6.17 ms: 1.29x slower                                                    |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.96 ms: 1.30x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 68.4 ms: 1.33x slower                                                    |
| django_template                  | 13.6 ms                                                  | 18.4 ms: 1.35x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.60 ms: 1.38x slower                                                    |
| nbody                            | 54.2 ms                                                  | 78.1 ms: 1.44x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 614 us: 1.47x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.2 ms: 1.50x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (2): pylint, regex_v8
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.015x slower

# HPT report

- Reliability score: 99.48% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x