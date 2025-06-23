# Results vs. 3.12.6

- fork: python
- ref: 621a8bd6a8d97cf4c628
- machine: darwin-arm64
- commit hash: 621a8bd
- commit date: 2025-06-22
- overall geometric mean: 1.093x faster
- HPT reliability: 97.32%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 997 ms: 1.02x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 421 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.8 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.8 ms: 1.07x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.8 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                   |
| nbody          | 54.2 ms                                                  | 55.6 ms: 1.02x slower                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                   |
| tomli_loads          | 957 ms                                                   | 978 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.64 ms: 1.09x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.57 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 783 us: 2.56x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 203 ms: 2.44x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.65 ms: 2.15x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 86.8 ms: 1.98x faster                                                   |
| mdp                              | 1.09 sec                                                 | 563 ms: 1.94x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 485 us: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.6 us: 1.34x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.89 us: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 821 ns: 1.18x faster                                                    |
| go                               | 70.0 ms                                                  | 60.6 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 987 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 54.6 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.7 ms: 1.07x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.0 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 138 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 421 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 997 ms: 1.02x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.3 ms: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.98 ms: 1.00x faster                                                   |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 71.8 us: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 978 ms: 1.02x slower                                                    |
| thrift                           | 322 us                                                   | 329 us: 1.02x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.6 ms: 1.02x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.0 ms: 1.02x slower                                                   |
| nbody                            | 54.2 ms                                                  | 55.6 ms: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 165 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.5 ms: 1.05x slower                                                   |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.8 ms: 1.07x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.6 ms: 1.09x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.64 ms: 1.09x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.82 us: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.0 ms: 1.11x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.13 us: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.6 ms: 1.12x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 53.8 ms: 1.13x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 769 ms: 1.16x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 382 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.57 ms: 1.19x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.31 ms: 1.27x slower                                                   |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 67.7 ms: 1.32x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 596 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.9 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.8 ms: 2.42x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 217 ns: 4.27x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): hexiom
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250622-3.15.0a0-621a8bd-NOGIL/bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.093x faster

# HPT report

- Reliability score: 97.32% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x