# Results vs. 3.12.6

- fork: python
- ref: dffac6163e693cf80ed4
- machine: darwin-arm64
- commit hash: dffac61
- commit date: 2026-08-14
- overall geometric mean: 1.007x faster
- HPT reliability: 83.68%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 137 ms: 1.20x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.11 sec: 1.08x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 464 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 316 ms: 1.57x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 315 ms: 1.52x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 311 ms: 1.43x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 321 ms: 1.43x faster                                                    |
| async_generators                 | 206 ms                                                   | 164 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 188 ms: 1.23x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 151 ms: 1.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 148 ms: 1.16x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 194 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 303 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 310 ms: 1.08x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 129 ms: 1.02x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 241 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 52.9 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 282 ms: 1.32x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 160 ms: 1.42x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 120 ms: 3.75x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.1 ms: 1.08x faster                                                   |
| pidigits       | 161 ms                                                   | 171 ms: 1.06x slower                                                    |
| nbody          | 54.2 ms                                                  | 64.1 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.9 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.08 ms: 1.06x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 69.4 ms: 1.27x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.1 ms: 1.20x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.0 ms: 1.13x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 39.4 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 973 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 118 us: 1.15x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 31.4 ms: 1.17x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 166 us: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 7.29 ms: 1.28x slower                                                   |
| python_startup         | 8.01 ms                                                  | 10.3 ms: 1.28x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.28x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 6.05 ms: 1.27x slower                                                   |
| django_template | 13.6 ms                                                  | 18.0 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.29x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.58 ms: 4.53x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 795 us: 2.53x faster                                                    |
| pylint                           | 128 ms                                                   | 55.1 ms: 2.32x faster                                                   |
| mdp                              | 1.09 sec                                                 | 624 ms: 1.75x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 490 us: 1.69x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 316 ms: 1.57x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 315 ms: 1.52x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 311 ms: 1.43x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 321 ms: 1.43x faster                                                    |
| deepcopy                         | 161 us                                                   | 120 us: 1.35x faster                                                    |
| async_generators                 | 206 ms                                                   | 164 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 188 ms: 1.23x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.1 ms: 1.20x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 808 ns: 1.20x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 151 ms: 1.18x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 15.5 us: 1.18x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 60.3 us: 1.18x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 148 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 194 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.13x faster                                                  |
| xml_etree_parse                  | 67.9 ms                                                  | 60.0 ms: 1.13x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.80 us: 1.12x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 303 ms: 1.12x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.09x faster                                                  |
| float                            | 37.9 ms                                                  | 35.1 ms: 1.08x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 310 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.9 ms: 1.07x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.08 ms: 1.06x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 20.2 ms: 1.05x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 52.1 ms: 1.04x faster                                                   |
| go                               | 70.0 ms                                                  | 67.3 ms: 1.04x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 137 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 129 ms: 1.02x faster                                                    |
| pyflate                          | 216 ms                                                   | 215 ms: 1.01x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 43.7 ms: 1.00x slower                                                   |
| coroutines                       | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 39.4 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 973 ms: 1.02x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 62.1 ms: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| pycparser                        | 497 ms                                                   | 509 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.64 us: 1.03x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 241 ms: 1.04x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.93 us: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 171 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| sphinx                           | 434 ms                                                   | 464 ms: 1.07x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.11 sec: 1.08x slower                                                  |
| raytrace                         | 145 ms                                                   | 157 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.3 ms: 1.09x slower                                                   |
| fannkuch                         | 176 ms                                                   | 192 ms: 1.09x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.4 ms: 1.10x slower                                                   |
| chaos                            | 28.9 ms                                                  | 32.0 ms: 1.11x slower                                                   |
| thrift                           | 322 us                                                   | 357 us: 1.11x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 64.4 ms: 1.12x slower                                                   |
| sympy_str                        | 104 ms                                                   | 117 ms: 1.12x slower                                                    |
| generators                       | 21.9 ms                                                  | 24.8 ms: 1.13x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 371 ms: 1.13x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 118 us: 1.15x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 764 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.1 ms: 1.15x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 52.9 ms: 1.16x slower                                                   |
| shortest_path                    | 219 ms                                                   | 256 ms: 1.17x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 196 ms: 1.17x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 31.4 ms: 1.17x slower                                                   |
| nbody                            | 54.2 ms                                                  | 64.1 ms: 1.18x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.60 ms: 1.18x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 166 us: 1.19x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.12 ms: 1.20x slower                                                   |
| richards                         | 22.4 ms                                                  | 26.9 ms: 1.20x slower                                                   |
| 2to3                             | 114 ms                                                   | 137 ms: 1.20x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 30.6 ms: 1.20x slower                                                   |
| connected_components             | 201 ms                                                   | 250 ms: 1.24x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 2.16 ms: 1.25x slower                                                   |
| mako                             | 4.77 ms                                                  | 6.05 ms: 1.27x slower                                                   |
| regex_compile                    | 54.6 ms                                                  | 69.4 ms: 1.27x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.29 ms: 1.28x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.3 ms: 1.28x slower                                                   |
| django_template                  | 13.6 ms                                                  | 18.0 ms: 1.32x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 282 ms: 1.32x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 69.3 ms: 1.35x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 583 us: 1.39x slower                                                    |
| many_optionals                   | 195 us                                                   | 276 us: 1.41x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 160 ms: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.7 ms: 1.52x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 120 ms: 3.75x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.00x faster                                                            |

Benchmark hidden because not significant (1): logging_silent
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 83.68% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x