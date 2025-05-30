# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: darwin-arm64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.039x faster
- HPT reliability: 96.55%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.10 sec: 1.07x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                    |
| sphinx         | 434 ms                                                   | 429 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 273 ms: 1.82x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 274 ms: 1.75x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 277 ms: 1.66x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 272 ms: 1.64x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 114 ms: 1.51x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.49x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 160 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 272 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.12x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.2 ms: 1.11x faster                                                    |
| async_generators                 | 206 ms                                                   | 197 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.23x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.2 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.7 ms: 1.16x faster                                                    |
| nbody          | 54.2 ms                                                  | 49.3 ms: 1.10x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.9 ms: 1.07x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.9 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 881 ms: 1.09x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.1 ms: 1.08x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 47.9 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 96.1 us: 1.07x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.24 ms: 1.23x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.47 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.56 ms: 1.05x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                    |
| django_template | 13.6 ms                                                  | 17.3 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.14 ms: 2.27x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 273 ms: 1.82x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 274 ms: 1.75x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 277 ms: 1.66x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 272 ms: 1.64x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 114 ms: 1.51x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.49x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 160 ms: 1.39x faster                                                     |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 14.3 us: 1.28x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 272 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.11 us: 1.21x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.16x faster                                                    |
| float                            | 37.9 ms                                                  | 32.7 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| k_core                           | 1.12 sec                                                 | 974 ms: 1.15x faster                                                     |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.12x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.2 ms: 1.11x faster                                                    |
| nbody                            | 54.2 ms                                                  | 49.3 ms: 1.10x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 881 ms: 1.09x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.1 ms: 1.08x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.6 ms: 1.08x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 47.9 ms: 1.08x faster                                                    |
| raytrace                         | 145 ms                                                   | 135 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.09 sec: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.9 ms: 1.07x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 96.1 us: 1.07x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 623 ms: 1.07x faster                                                     |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 121 ms: 1.06x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 51.6 ms: 1.05x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.9 ms: 1.05x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.56 ms: 1.05x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.8 ms: 1.05x faster                                                    |
| async_generators                 | 206 ms                                                   | 197 ms: 1.05x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.99 ms: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                    |
| go                               | 70.0 ms                                                  | 68.1 ms: 1.03x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 38.7 ms: 1.03x faster                                                    |
| pyflate                          | 216 ms                                                   | 211 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| sphinx                           | 434 ms                                                   | 429 ms: 1.01x faster                                                     |
| thrift                           | 322 us                                                   | 324 us: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| mdp                              | 1.09 sec                                                 | 1.10 sec: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                     |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                     |
| logging_simple                   | 2.57 us                                                  | 2.63 us: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.88 us: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                     |
| nqueens                          | 43.5 ms                                                  | 44.6 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                     |
| scimark_sor                      | 61.0 ms                                                  | 63.0 ms: 1.03x slower                                                    |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.03x slower                                                     |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.7 ms: 1.05x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 439 us: 1.05x slower                                                     |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.44 ms: 1.05x slower                                                    |
| chaos                            | 28.9 ms                                                  | 30.5 ms: 1.05x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.4 ms: 1.05x slower                                                    |
| pycparser                        | 497 ms                                                   | 525 ms: 1.06x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.50 ms: 1.06x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.10 sec: 1.07x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 55.1 ms: 1.07x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 181 ms: 1.09x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.4 ms: 1.09x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.36 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 919 us: 1.11x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 24.2 ms: 1.11x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.47 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.19 ms: 1.22x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.24 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.23x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.7 ms: 1.25x slower                                                    |
| django_template                  | 13.6 ms                                                  | 17.3 ms: 1.27x slower                                                    |
| many_optionals                   | 195 us                                                   | 251 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.2 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (5): logging_silent, sympy_sum, typing_runtime_protocols, sqlalchemy_declarative, sqlite_synth
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 96.55% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x