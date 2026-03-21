# Results vs. 3.12.6

- fork: python
- ref: b5e4c46be24d1fade0de
- machine: darwin-arm64
- commit hash: b5e4c46
- commit date: 2026-03-20
- overall geometric mean: 1.161x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| sphinx         | 434 ms                                                   | 399 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 222 ms: 2.24x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.01x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.7 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.5 ms: 1.77x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.93 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.7 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.0 ms: 1.23x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.19x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.4 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                    |
| tomli_loads          | 957 ms                                                   | 826 ms: 1.16x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.9 us: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.79 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.31 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.66 ms: 1.09x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.02 ms: 5.16x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 222 ms: 2.24x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                     |
| mdp                              | 1.09 sec                                                 | 536 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.01x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.7 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.5 ms: 1.77x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.4 us: 1.64x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.57x faster                                                    |
| float                            | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.93 ms: 1.37x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.21 us: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                     |
| go                               | 70.0 ms                                                  | 53.2 ms: 1.32x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 41.8 ms: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.3 ns: 1.26x faster                                                    |
| k_core                           | 1.12 sec                                                 | 898 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.4 ms: 1.23x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.0 ms: 1.23x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 117 ms: 1.21x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 36.8 ms: 1.18x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.4 ms: 1.18x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.7 ms: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.16x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 826 ms: 1.16x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.82 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.6 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.0 us: 1.11x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.4 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 399 ms: 1.09x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.66 ms: 1.09x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.6 ms: 1.09x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.55 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 469 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 98.9 us: 1.04x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 316 ms: 1.04x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 641 ms: 1.04x faster                                                     |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                     |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 56.2 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 945 ns: 1.02x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                    |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                     |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.7 ms: 1.00x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                     |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.78 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| 2to3                             | 114 ms                                                   | 117 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.7 ms: 1.04x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.79 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.31 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 922 us: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.7 ms: 2.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (1): mako
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260320-3.15.0a7+-b5e4c46/bm-20260320-macm4pro-arm64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.161x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.23x