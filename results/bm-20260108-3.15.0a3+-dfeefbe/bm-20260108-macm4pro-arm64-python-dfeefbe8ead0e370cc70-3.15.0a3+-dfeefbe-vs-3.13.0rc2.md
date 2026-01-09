# Results vs. 3.13.0rc2

- fork: python
- ref: dfeefbe8ead0e370cc70
- machine: darwin-arm64
- commit hash: dfeefbe
- commit date: 2026-01-08
- overall geometric mean: 1.073x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.63x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 104 ms: 1.37x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.5 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 45.4 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.3 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.90 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 840 ms: 1.19x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 97.1 us: 1.02x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 65.4 ms: 1.05x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.96 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.45 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.70 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.68 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 226 ms: 2.32x faster                                                     |
| mdp                              | 1.06 sec                                                       | 543 ms: 1.95x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.79x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 236 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 906 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.07 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.4 us: 1.47x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                    |
| go                               | 72.6 ms                                                        | 52.7 ms: 1.38x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 104 ms: 1.37x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.7 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.24x faster                                                    |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.90 ms: 1.19x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 840 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.73 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 303 ms: 1.06x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.3 ms: 1.06x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 615 ms: 1.06x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 945 us: 1.05x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.5 ms: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.75 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.70 ms: 1.03x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.9 us: 1.03x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 97.1 us: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| scimark_lu                       | 42.8 ms                                                        | 43.0 ms: 1.01x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.6 ms: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 966 ns: 1.02x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.7 ns: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| chaos                            | 24.3 ms                                                        | 24.9 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.5 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 38.5 ms: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.96 ms: 1.04x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.08 us: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 431 us: 1.05x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 99.9 ms: 1.05x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.4 ms: 1.05x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.68 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.6 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.06x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 51.0 ms: 1.07x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.4 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.45 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                    |
| pylint                           | 106 ms                                                         | 116 ms: 1.09x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.8 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 259 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.5 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (6): json, logging_format, sympy_integrate, spectral_norm, json_loads, scimark_sparse_mat_mult
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260108-3.15.0a3+-dfeefbe/bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.17x