# Results vs. 3.12.6

- fork: python
- ref: 04242c027feeff726acb
- machine: darwin-arm64
- commit hash: 04242c0
- commit date: 2026-08-20
- overall geometric mean: 1.010x faster
- HPT reliability: 81.16%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 137 ms: 1.20x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.11 sec: 1.08x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.3 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 468 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 315 ms: 1.57x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 315 ms: 1.52x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 310 ms: 1.44x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 321 ms: 1.43x faster                                                    |
| async_generators                 | 206 ms                                                   | 167 ms: 1.23x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 187 ms: 1.23x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 149 ms: 1.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 192 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 303 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 308 ms: 1.08x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 129 ms: 1.02x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 240 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 53.0 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 281 ms: 1.32x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 160 ms: 1.42x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| nbody          | 54.2 ms                                                  | 62.6 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.38 ms: 1.21x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.7 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.10 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 69.2 ms: 1.27x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                   |
| tomli_loads          | 957 ms                                                   | 965 ms: 1.01x slower                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 39.4 ms: 1.01x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 119 us: 1.16x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 31.5 ms: 1.18x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 166 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 7.27 ms: 1.27x slower                                                   |
| python_startup         | 8.01 ms                                                  | 10.3 ms: 1.28x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.28x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 6.03 ms: 1.26x slower                                                   |
| django_template | 13.6 ms                                                  | 18.0 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.29x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.61 ms: 4.51x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 781 us: 2.57x faster                                                    |
| pylint                           | 128 ms                                                   | 54.8 ms: 2.34x faster                                                   |
| mdp                              | 1.09 sec                                                 | 624 ms: 1.75x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 489 us: 1.70x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 315 ms: 1.57x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 315 ms: 1.52x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 310 ms: 1.44x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 321 ms: 1.43x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.35x faster                                                    |
| async_generators                 | 206 ms                                                   | 167 ms: 1.23x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 187 ms: 1.23x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.4 ms: 1.22x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.38 ms: 1.21x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 149 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 813 ns: 1.19x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 60.5 us: 1.17x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 15.6 us: 1.17x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 192 ms: 1.16x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| xml_etree_parse                  | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 303 ms: 1.12x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.85 us: 1.11x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                  |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 308 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.7 ms: 1.07x faster                                                   |
| float                            | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 20.0 ms: 1.06x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.10 ms: 1.05x faster                                                   |
| go                               | 70.0 ms                                                  | 67.1 ms: 1.04x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 52.4 ms: 1.04x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 138 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 129 ms: 1.02x faster                                                    |
| pyflate                          | 216 ms                                                   | 213 ms: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 965 ms: 1.01x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 43.9 ms: 1.01x slower                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 39.4 ms: 1.01x slower                                                   |
| scimark_sor                      | 61.0 ms                                                  | 61.9 ms: 1.02x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.63 us: 1.02x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.87 us: 1.02x slower                                                   |
| pycparser                        | 497 ms                                                   | 511 ms: 1.03x slower                                                    |
| coroutines                       | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 240 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.3 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.58 ms: 1.07x slower                                                   |
| sphinx                           | 434 ms                                                   | 468 ms: 1.08x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.11 sec: 1.08x slower                                                  |
| raytrace                         | 145 ms                                                   | 157 ms: 1.09x slower                                                    |
| fannkuch                         | 176 ms                                                   | 191 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.4 ms: 1.09x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 63.1 ms: 1.10x slower                                                   |
| sympy_str                        | 104 ms                                                   | 115 ms: 1.10x slower                                                    |
| thrift                           | 322 us                                                   | 357 us: 1.11x slower                                                    |
| chaos                            | 28.9 ms                                                  | 32.2 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 36.3 ms: 1.13x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 370 ms: 1.13x slower                                                    |
| generators                       | 21.9 ms                                                  | 24.9 ms: 1.13x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 761 ms: 1.14x slower                                                    |
| nbody                            | 54.2 ms                                                  | 62.6 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 55.1 ms: 1.15x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 119 us: 1.16x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 53.0 ms: 1.16x slower                                                   |
| shortest_path                    | 219 ms                                                   | 256 ms: 1.17x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 196 ms: 1.17x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 31.5 ms: 1.18x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.09 ms: 1.18x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.60 ms: 1.19x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 166 us: 1.19x slower                                                    |
| richards                         | 22.4 ms                                                  | 26.9 ms: 1.20x slower                                                   |
| 2to3                             | 114 ms                                                   | 137 ms: 1.20x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 2.08 ms: 1.20x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 30.7 ms: 1.21x slower                                                   |
| connected_components             | 201 ms                                                   | 247 ms: 1.23x slower                                                    |
| mako                             | 4.77 ms                                                  | 6.03 ms: 1.26x slower                                                   |
| regex_compile                    | 54.6 ms                                                  | 69.2 ms: 1.27x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.27 ms: 1.27x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.3 ms: 1.28x slower                                                   |
| django_template                  | 13.6 ms                                                  | 18.0 ms: 1.32x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 281 ms: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 571 us: 1.36x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 70.9 ms: 1.38x slower                                                   |
| many_optionals                   | 195 us                                                   | 274 us: 1.40x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 160 ms: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 41.5 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.72x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (3): logging_silent, json_loads, json
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 81.16% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x