# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: darwin-arm64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.019x faster
- HPT reliability: 72.66%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.03x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.09 sec: 1.07x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                    |
| sphinx         | 434 ms                                                   | 428 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 273 ms: 1.82x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 275 ms: 1.75x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 279 ms: 1.65x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 273 ms: 1.63x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 114 ms: 1.51x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.50x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 270 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.9 ms: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 117 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.0 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 138 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.3 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.8 ms: 1.06x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 60.2 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.7 ms: 1.06x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 46.5 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 39.2 ms: 1.01x slower                                                    |
| tomli_loads          | 957 ms                                                   | 995 ms: 1.04x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 28.7 ms: 1.07x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.10x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.19 ms: 1.22x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.45 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                    |
| mako            | 4.77 ms                                                  | 5.30 ms: 1.11x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                    |
| django_template | 13.6 ms                                                  | 17.2 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.07 ms: 2.29x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 273 ms: 1.82x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 275 ms: 1.75x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 279 ms: 1.65x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 273 ms: 1.63x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 114 ms: 1.51x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.50x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                     |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 14.2 us: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 270 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.16x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.14x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.62 us: 1.14x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.9 ms: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 117 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 46.5 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                    |
| raytrace                         | 145 ms                                                   | 136 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 93.7 ms: 1.06x faster                                                    |
| go                               | 70.0 ms                                                  | 65.9 ms: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 121 ms: 1.06x faster                                                     |
| float                            | 37.9 ms                                                  | 35.8 ms: 1.06x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.7 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.8 ms: 1.05x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 38.4 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.01 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 49.7 ns: 1.02x faster                                                    |
| sphinx                           | 434 ms                                                   | 428 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 46.6 ms: 1.00x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.23 sec: 1.00x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 39.2 ms: 1.01x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 58.1 ms: 1.01x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.0 ms: 1.01x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.83 us: 1.01x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.60 us: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| deltablue                        | 1.73 ms                                                  | 1.76 ms: 1.02x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 145 ms: 1.02x slower                                                     |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.02x slower                                                     |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.03x slower                                                     |
| scimark_sor                      | 61.0 ms                                                  | 63.3 ms: 1.04x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 995 ms: 1.04x slower                                                     |
| mdp                              | 1.09 sec                                                 | 1.14 sec: 1.04x slower                                                   |
| pycparser                        | 497 ms                                                   | 518 ms: 1.04x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.36 ms: 1.04x slower                                                    |
| chaos                            | 28.9 ms                                                  | 30.3 ms: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                    |
| pyflate                          | 216 ms                                                   | 227 ms: 1.05x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| shortest_path                    | 219 ms                                                   | 231 ms: 1.05x slower                                                     |
| connected_components             | 201 ms                                                   | 212 ms: 1.05x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 442 us: 1.06x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.50 ms: 1.06x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.09 sec: 1.07x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 46.3 ms: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 708 ms: 1.07x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 178 ms: 1.07x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 28.7 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 353 ms: 1.08x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 51.8 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.7 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.10x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.7 ms: 1.10x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.6 ms: 1.10x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.8 ms: 1.11x slower                                                    |
| nbody                            | 54.2 ms                                                  | 60.2 ms: 1.11x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.30 ms: 1.11x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.38 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 926 us: 1.12x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.45 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| fannkuch                         | 176 ms                                                   | 209 ms: 1.19x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.19 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 138 ms: 1.23x slower                                                     |
| many_optionals                   | 195 us                                                   | 242 us: 1.24x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.27 ms: 1.25x slower                                                    |
| django_template                  | 13.6 ms                                                  | 17.2 ms: 1.26x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.3 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.02x faster                                                             |

Benchmark hidden because not significant (3): thrift, typing_runtime_protocols, sqlite_synth
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 72.66% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.12x