# Results vs. 3.13.0rc2

- fork: python
- ref: f8262b84f5b76e45cfea
- machine: darwin-arm64
- commit hash: f8262b8
- commit date: 2026-01-22
- overall geometric mean: 1.073x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.8 ms: 1.06x faster                                                    |
| sphinx         | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.35x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 104 ms: 1.37x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.3 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.2 ms: 1.16x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 45.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.65 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.4 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.3 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 845 ms: 1.18x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.9 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.1 us: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.8 ms: 1.01x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.98 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.47 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.72 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.71 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 221 ms: 2.35x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.35x faster                                                     |
| mdp                              | 1.06 sec                                                       | 545 ms: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 900 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.07 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 99.5 us: 1.46x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.45x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 104 ms: 1.37x faster                                                     |
| go                               | 72.6 ms                                                        | 53.1 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.08 us: 1.20x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 845 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                     |
| float                            | 31.4 ms                                                        | 27.2 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.65 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.4 ms: 1.09x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.3 ms: 1.09x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.8 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.4 ms: 1.06x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 946 us: 1.05x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 309 ms: 1.04x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 62.3 us: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 628 ms: 1.03x faster                                                     |
| sphinx                           | 409 ms                                                         | 396 ms: 1.03x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.6 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.76 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.72 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 98.1 us: 1.01x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 43.3 ms: 1.01x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 208 ms: 1.00x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.00x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.8 ms: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.3 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 967 ns: 1.02x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.03x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.0 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.5 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.2 ms: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.4 ms: 1.04x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.98 ms: 1.04x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.09 us: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 50.5 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| nbody                            | 42.5 ms                                                        | 45.0 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.7 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.71 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.47 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.8 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.21x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.7 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.3 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (8): pycparser, thrift, genshi_xml, shortest_path, sympy_integrate, logging_format, logging_silent, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260122-3.15.0a5+-f8262b8/bm-20260122-macm4pro-arm64-python-f8262b84f5b76e45cfea-3.15.0a5+-f8262b8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.17x