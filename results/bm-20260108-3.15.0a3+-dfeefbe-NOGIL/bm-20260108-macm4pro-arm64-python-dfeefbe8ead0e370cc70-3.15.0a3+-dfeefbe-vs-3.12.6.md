# Results vs. 3.12.6

- fork: python
- ref: dfeefbe8ead0e370cc70
- machine: darwin-arm64
- commit hash: dfeefbe
- commit date: 2026-01-08
- overall geometric mean: 1.087x faster
- HPT reliability: 98.88%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 429 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 243 ms: 1.84x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.46x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.2 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.1 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.7 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.00 ms: 1.07x faster                                                    |
| tomli_loads          | 957 ms                                                   | 908 ms: 1.05x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.95 ms: 1.24x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.21 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                                    |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.16x slower                                                    |
| mako            | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.15 ms: 5.01x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 820 us: 2.45x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 243 ms: 1.84x faster                                                     |
| mdp                              | 1.09 sec                                                 | 609 ms: 1.79x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 521 us: 1.59x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.46x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                    |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.33 us: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 828 ns: 1.17x faster                                                     |
| go                               | 70.0 ms                                                  | 60.4 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.5 ns: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 128 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 998 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.12x faster                                                    |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.8 ms: 1.09x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.00 ms: 1.07x faster                                                    |
| pylint                           | 128 ms                                                   | 121 ms: 1.06x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 908 ms: 1.05x faster                                                     |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.9 ms: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.1 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.70 us: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.2 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| sphinx                           | 434 ms                                                   | 429 ms: 1.01x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 43.1 ms: 1.01x faster                                                    |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.14 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 333 ms: 1.02x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.11 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 686 ms: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.2 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.3 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.7 ms: 1.05x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.7 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                     |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                     |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.6 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.7 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 58.2 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.16x slower                                                    |
| shortest_path                    | 219 ms                                                   | 254 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.5 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.5 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.95 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.21 ms: 1.26x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 552 us: 1.32x slower                                                     |
| many_optionals                   | 195 us                                                   | 267 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.7 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.1 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (2): dask, typing_runtime_protocols
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260108-3.15.0a3+-dfeefbe-NOGIL/bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 98.88% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x