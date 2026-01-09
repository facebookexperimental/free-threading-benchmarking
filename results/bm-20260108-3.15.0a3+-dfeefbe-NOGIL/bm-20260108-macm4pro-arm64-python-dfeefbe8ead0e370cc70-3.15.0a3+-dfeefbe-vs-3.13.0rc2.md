# Results vs. 3.13.0rc2

- fork: python
- ref: dfeefbe8ead0e370cc70
- machine: darwin-arm64
- commit hash: dfeefbe
- commit date: 2026-01-08
- overall geometric mean: 1.009x faster
- HPT reliability: 64.75%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 429 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 243 ms: 2.14x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.2 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.1 ms: 3.25x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.00 ms: 1.16x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 908 ms: 1.10x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.95 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.21 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                    |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| mako            | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 820 us: 2.49x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 243 ms: 2.14x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 249 ms: 2.11x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 521 us: 1.91x faster                                                     |
| mdp                              | 1.06 sec                                                       | 609 ms: 1.74x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.70x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.15 ms: 1.51x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                     |
| k_core                           | 1.46 sec                                                       | 998 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 107 us: 1.36x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 60.4 ms: 1.20x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.00 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.24 ms: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 828 ns: 1.14x faster                                                     |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 908 ms: 1.10x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                     |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| pycparser                        | 470 ms                                                         | 473 ms: 1.01x slower                                                     |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 126 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                    |
| sphinx                           | 409 ms                                                         | 429 ms: 1.05x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 686 ms: 1.06x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.14 ms: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.7 ms: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.5 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.2 ms: 1.09x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.09x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 44.5 ns: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 339 us: 1.10x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.3 us: 1.10x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.70 us: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.13x slower                                                    |
| shortest_path                    | 225 ms                                                         | 254 ms: 1.13x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.8 ms: 1.14x slower                                                    |
| pylint                           | 106 ms                                                         | 121 ms: 1.14x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.95 ms: 1.15x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.1 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                     |
| chaos                            | 24.3 ms                                                        | 28.2 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.6 ms: 1.18x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.5 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.11 ms: 1.19x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.21 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.33 us: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.5 ms: 1.23x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.7 ms: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.7 ms: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.57 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| nbody                            | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 267 us: 1.33x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 552 us: 1.34x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.1 ms: 1.34x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 58.2 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.1 ms: 3.25x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260108-3.15.0a3+-dfeefbe-NOGIL/bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 64.75% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x