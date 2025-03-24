# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: darwin-arm64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.054x slower
- HPT reliability: 99.91%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.09 sec: 1.04x slower                                                   |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                    |
| sphinx         | 409 ms                                                         | 428 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 273 ms: 1.93x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 273 ms: 1.91x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 275 ms: 1.47x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 279 ms: 1.39x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.20x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 114 ms: 1.16x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 117 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.0 ms: 1.07x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.9 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 138 ms: 1.35x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| float          | 31.4 ms                                                        | 35.8 ms: 1.14x slower                                                    |
| nbody          | 42.5 ms                                                        | 60.2 ms: 1.42x slower                                                    |
| Geometric mean | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 46.5 ms: 1.01x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 39.2 ms: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.19 ms: 1.12x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 28.7 ms: 1.13x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.14x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.08x slower                                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.71 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.45 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.17x slower                                                    |
| mako            | 4.41 ms                                                        | 5.30 ms: 1.20x slower                                                    |
| django_template | 12.5 ms                                                        | 17.2 ms: 1.38x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 273 ms: 1.93x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 273 ms: 1.91x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 275 ms: 1.47x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 279 ms: 1.39x faster                                                     |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 119 ms: 1.20x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 14.2 us: 1.16x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 114 ms: 1.16x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.12x faster                                                     |
| go                               | 72.6 ms                                                        | 65.9 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 926 us: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 117 ms: 1.04x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 63.3 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 46.5 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.71 ms: 1.01x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 38.4 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 212 ms: 1.02x slower                                                     |
| pyflate                          | 222 ms                                                         | 227 ms: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                    |
| shortest_path                    | 225 ms                                                         | 231 ms: 1.03x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 974 ns: 1.03x slower                                                     |
| docutils                         | 1.05 sec                                                       | 1.09 sec: 1.04x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                    |
| thrift                           | 309 us                                                         | 322 us: 1.04x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.13 ms: 1.05x slower                                                    |
| sphinx                           | 409 ms                                                         | 428 ms: 1.05x slower                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.23 sec: 1.05x slower                                                   |
| sqlalchemy_declarative           | 44.4 ms                                                        | 46.6 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.7 ms: 1.05x slower                                                    |
| 2to3                             | 112 ms                                                         | 117 ms: 1.05x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.27 ms: 1.07x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.0 ms: 1.07x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 442 us: 1.07x slower                                                     |
| mdp                              | 1.06 sec                                                       | 1.14 sec: 1.07x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 51.8 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.45 ms: 1.08x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 708 ms: 1.09x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 39.2 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.50 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.2 us: 1.10x slower                                                    |
| pycparser                        | 470 ms                                                         | 518 ms: 1.10x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.9 ms: 1.11x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 58.1 ms: 1.11x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.36 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.19 ms: 1.12x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 178 ms: 1.12x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.7 ms: 1.12x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.8 ms: 1.12x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.01 ms: 1.13x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 28.7 ms: 1.13x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.13x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.14x slower                                                     |
| float                            | 31.4 ms                                                        | 35.8 ms: 1.14x slower                                                    |
| pylint                           | 106 ms                                                         | 121 ms: 1.14x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.83 us: 1.16x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.60 us: 1.16x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.17x slower                                                    |
| fannkuch                         | 179 ms                                                         | 209 ms: 1.17x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 145 ms: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.8 ms: 1.18x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.38 ms: 1.19x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.30 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 242 us: 1.21x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.76 ms: 1.21x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 49.7 ns: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 46.3 ms: 1.24x slower                                                    |
| chaos                            | 24.3 ms                                                        | 30.3 ms: 1.25x slower                                                    |
| raytrace                         | 109 ms                                                         | 136 ms: 1.25x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.62 us: 1.27x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.7 ms: 1.27x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 56.6 ms: 1.32x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 138 ms: 1.35x slower                                                     |
| django_template                  | 12.5 ms                                                        | 17.2 ms: 1.38x slower                                                    |
| nbody                            | 42.5 ms                                                        | 60.2 ms: 1.42x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.07 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x slower                                                             |

Benchmark hidden because not significant (2): tomli_loads, async_tree_eager_cpu_io_mixed
Ignored benchmarks (8) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.054x slower

# HPT report

- Reliability score: 99.91% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.07x