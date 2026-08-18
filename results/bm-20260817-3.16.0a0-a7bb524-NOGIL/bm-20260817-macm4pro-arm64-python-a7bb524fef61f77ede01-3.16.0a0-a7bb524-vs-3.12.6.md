# Results vs. 3.12.6

- fork: python
- ref: a7bb524fef61f77ede01
- machine: darwin-arm64
- commit hash: a7bb524
- commit date: 2026-08-17
- overall geometric mean: 1.015x faster
- HPT reliability: 63.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.28x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 135 ms: 1.19x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.10 sec: 1.08x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 460 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 313 ms: 1.59x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 312 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 308 ms: 1.45x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 318 ms: 1.44x faster                                                    |
| async_generators                 | 206 ms                                                   | 163 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 148 ms: 1.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 146 ms: 1.18x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 192 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 301 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 307 ms: 1.08x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 12.5 ms: 1.08x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 128 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 239 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 52.9 ms: 1.16x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 280 ms: 1.32x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.70x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.4 ms: 1.07x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| nbody          | 54.2 ms                                                  | 64.6 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.38 ms: 1.21x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.5 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 68.8 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.0 ms: 1.23x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.7 ms: 1.14x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.12x faster                                                   |
| tomli_loads          | 957 ms                                                   | 949 ms: 1.01x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 39.6 ms: 1.02x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 117 us: 1.14x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 165 us: 1.18x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 31.8 ms: 1.19x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.26 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.27x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 6.01 ms: 1.26x slower                                                   |
| django_template | 13.6 ms                                                  | 18.0 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.29x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.55 ms: 4.57x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 783 us: 2.57x faster                                                    |
| pylint                           | 128 ms                                                   | 54.7 ms: 2.34x faster                                                   |
| mdp                              | 1.09 sec                                                 | 618 ms: 1.77x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 489 us: 1.70x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 313 ms: 1.59x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 312 ms: 1.54x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 308 ms: 1.45x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 318 ms: 1.44x faster                                                    |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                    |
| async_generators                 | 206 ms                                                   | 163 ms: 1.27x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.0 ms: 1.23x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.38 ms: 1.21x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 148 ms: 1.20x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 15.3 us: 1.20x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 817 ns: 1.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 146 ms: 1.18x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 60.4 us: 1.18x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 192 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.15x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.7 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 301 ms: 1.13x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.77 us: 1.12x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.10x faster                                                  |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 307 ms: 1.08x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 12.5 ms: 1.08x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.5 ms: 1.08x faster                                                   |
| float                            | 37.9 ms                                                  | 35.4 ms: 1.07x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.9 ms: 1.07x faster                                                   |
| go                               | 70.0 ms                                                  | 66.3 ms: 1.06x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 135 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 49.1 ns: 1.04x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 52.6 ms: 1.03x faster                                                   |
| pyflate                          | 216 ms                                                   | 210 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 128 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 60.1 ms: 1.01x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 949 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.07 ms: 1.00x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 43.7 ms: 1.01x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 39.6 ms: 1.02x slower                                                   |
| pycparser                        | 497 ms                                                   | 509 ms: 1.02x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.63 us: 1.02x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.89 us: 1.03x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 239 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.51 ms: 1.06x slower                                                   |
| sphinx                           | 434 ms                                                   | 460 ms: 1.06x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.10 sec: 1.08x slower                                                  |
| raytrace                         | 145 ms                                                   | 156 ms: 1.08x slower                                                    |
| fannkuch                         | 176 ms                                                   | 191 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.3 ms: 1.09x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 62.9 ms: 1.09x slower                                                   |
| chaos                            | 28.9 ms                                                  | 31.6 ms: 1.09x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.2 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| sympy_str                        | 104 ms                                                   | 115 ms: 1.11x slower                                                    |
| thrift                           | 322 us                                                   | 359 us: 1.12x slower                                                    |
| generators                       | 21.9 ms                                                  | 24.6 ms: 1.12x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 373 ms: 1.14x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 117 us: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.3 ms: 1.14x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 766 ms: 1.15x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 52.9 ms: 1.16x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.53 ms: 1.16x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 195 ms: 1.17x slower                                                    |
| shortest_path                    | 219 ms                                                   | 256 ms: 1.17x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 165 us: 1.18x slower                                                    |
| 2to3                             | 114 ms                                                   | 135 ms: 1.19x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 31.8 ms: 1.19x slower                                                   |
| nbody                            | 54.2 ms                                                  | 64.6 ms: 1.19x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 30.3 ms: 1.19x slower                                                   |
| richards                         | 22.4 ms                                                  | 27.0 ms: 1.21x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.16 ms: 1.21x slower                                                   |
| connected_components             | 201 ms                                                   | 247 ms: 1.23x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 68.8 ms: 1.26x slower                                                   |
| mako                             | 4.77 ms                                                  | 6.01 ms: 1.26x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.26 ms: 1.27x slower                                                   |
| deltablue                        | 1.73 ms                                                  | 2.20 ms: 1.27x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 280 ms: 1.32x slower                                                    |
| django_template                  | 13.6 ms                                                  | 18.0 ms: 1.32x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 577 us: 1.38x slower                                                    |
| many_optionals                   | 195 us                                                   | 271 us: 1.39x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 74.7 ms: 1.46x slower                                                   |
| coverage                         | 26.9 ms                                                  | 41.1 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.70x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (1): json
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 63.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.28x