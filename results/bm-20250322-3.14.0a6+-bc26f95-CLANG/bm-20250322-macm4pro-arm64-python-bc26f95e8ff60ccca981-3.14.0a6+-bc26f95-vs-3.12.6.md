# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: darwin-arm64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.136x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 106 ms: 1.08x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 245 ms: 1.96x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 248 ms: 1.80x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 106 ms: 1.67x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.59 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                     |
| async_generators                 | 206 ms                                                   | 164 ms: 1.26x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 215 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.2 ms: 2.65x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.2 ms: 1.25x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.6 ms: 1.16x faster                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.2 ms: 1.21x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 103 ms: 1.03x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 10.6 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                    |
| tomli_loads          | 957 ms                                                   | 818 ms: 1.17x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.7 ms: 1.13x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 93.4 us: 1.10x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.9 ms: 1.10x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 135 us: 1.03x faster                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.89 ms: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.56 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.35 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.72 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| django_template | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.41 ms: 2.47x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.01x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 245 ms: 1.96x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 248 ms: 1.80x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 106 ms: 1.67x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| deepcopy                         | 161 us                                                   | 99.1 us: 1.63x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| generators                       | 21.9 ms                                                  | 13.9 ms: 1.58x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.59 ms: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.37x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.23 us: 1.36x faster                                                    |
| go                               | 70.0 ms                                                  | 53.5 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.30x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 39.1 ns: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 16.8 ms: 1.27x faster                                                    |
| async_generators                 | 206 ms                                                   | 164 ms: 1.26x faster                                                     |
| float                            | 37.9 ms                                                  | 30.2 ms: 1.25x faster                                                    |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 45.2 ms: 1.21x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.3 ms: 1.20x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.8 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.7 ms: 1.18x faster                                                    |
| k_core                           | 1.12 sec                                                 | 950 ms: 1.18x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 43.7 ms: 1.17x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 818 ms: 1.17x faster                                                     |
| pylint                           | 128 ms                                                   | 110 ms: 1.17x faster                                                     |
| nbody                            | 54.2 ms                                                  | 46.6 ms: 1.16x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.21 us: 1.16x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.16x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.64 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.0 us: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.14x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.7 ms: 1.13x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.84 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.1 ms: 1.11x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.0 ms: 1.11x faster                                                    |
| thrift                           | 322 us                                                   | 292 us: 1.10x faster                                                     |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 42.4 ms: 1.10x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 93.4 us: 1.10x faster                                                    |
| sympy_str                        | 104 ms                                                   | 94.8 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.9 ms: 1.10x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.34 ms: 1.09x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 52.8 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.8 ms: 1.08x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.72 ms: 1.08x faster                                                    |
| 2to3                             | 114 ms                                                   | 106 ms: 1.08x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 215 ms: 1.07x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 37.2 ms: 1.07x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 626 ms: 1.06x faster                                                     |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 311 ms: 1.05x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 159 ms: 1.05x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 931 ns: 1.04x faster                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 4.98 ms: 1.04x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 135 us: 1.03x faster                                                     |
| mdp                              | 1.09 sec                                                 | 1.06 sec: 1.03x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 47.0 ms: 1.02x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 412 us: 1.02x faster                                                     |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                     |
| regex_dna                        | 99.6 ms                                                  | 103 ms: 1.03x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.3 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 881 us: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.56 ms: 1.07x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.6 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.35 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 4.89 ms: 1.15x slower                                                    |
| many_optionals                   | 195 us                                                   | 227 us: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.07 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.2 ms: 2.65x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                             |

Benchmark hidden because not significant (5): mako, pidigits, gc_traversal, connected_components, fannkuch
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.136x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.11x