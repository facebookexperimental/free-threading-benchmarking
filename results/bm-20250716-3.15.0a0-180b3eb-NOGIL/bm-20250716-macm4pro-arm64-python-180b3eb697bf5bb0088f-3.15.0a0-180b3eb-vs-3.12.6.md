# Results vs. 3.12.6

- fork: python
- ref: 180b3eb697bf5bb0088f
- machine: darwin-arm64
- commit hash: 180b3eb
- commit date: 2025-07-16
- overall geometric mean: 1.100x faster
- HPT reliability: 97.88%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 996 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 407 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 201 ms: 2.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.1 ms: 2.00x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 98.7 ms: 1.81x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.73x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.3 ms: 1.04x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.8 ms: 2.39x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                   |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.51 ms: 1.11x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.16 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.6 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.6 ms: 1.33x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.6 ms: 1.01x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| tomli_loads          | 957 ms                                                   | 1.00 sec: 1.05x slower                                                  |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.08x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.63 ms: 1.09x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.47 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.69 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.3 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 775 us: 2.59x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 201 ms: 2.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.79 ms: 2.12x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 86.1 ms: 2.00x faster                                                   |
| mdp                              | 1.09 sec                                                 | 580 ms: 1.88x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 98.7 ms: 1.81x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.73x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 484 us: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                    |
| deepcopy                         | 161 us                                                   | 118 us: 1.37x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.6 ms: 1.33x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.7 us: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                   |
| float                            | 37.9 ms                                                  | 30.0 ms: 1.26x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.92 us: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 816 ns: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.15x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.3 ns: 1.15x faster                                                   |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| go                               | 70.0 ms                                                  | 61.5 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.51 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.5 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                    |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 407 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 469 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.6 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.16 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.6 ms: 1.04x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.6 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 996 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.95 ms: 1.01x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.6 ms: 1.01x faster                                                   |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.05 ms: 1.00x slower                                                   |
| dask                             | 528 ms                                                   | 530 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                   |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.88 us: 1.03x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.5 us: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 334 us: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.3 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.5 ms: 1.04x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 1.00 sec: 1.05x slower                                                  |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.3 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                   |
| 2to3                             | 114 ms                                                   | 120 ms: 1.06x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.7 ms: 1.06x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 348 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 707 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.2 ms: 1.07x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.08x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.63 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.4 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.6 ms: 1.17x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.47 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.69 ms: 1.19x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.3 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.21 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 245 us: 1.26x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 592 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.8 ms: 1.48x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.8 ms: 2.39x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (2): logging_simple, scimark_fft
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 97.88% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x