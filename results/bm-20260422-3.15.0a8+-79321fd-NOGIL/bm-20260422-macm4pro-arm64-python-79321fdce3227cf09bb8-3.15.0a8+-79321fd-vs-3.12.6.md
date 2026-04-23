# Results vs. 3.12.6

- fork: python
- ref: 79321fdce3227cf09bb8
- machine: darwin-arm64
- commit hash: 79321fd
- commit date: 2026-04-22
- overall geometric mean: 1.112x faster
- HPT reliability: 99.87%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 988 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.88x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.49x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.8 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.1 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| nbody          | 54.2 ms                                                  | 57.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.6 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.10 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.7 ms: 1.37x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                    |
| tomli_loads          | 957 ms                                                   | 845 ms: 1.13x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.63 ms: 1.16x slower                                                    |
| python_startup         | 8.01 ms                                                  | 9.50 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                    |
| mako            | 4.77 ms                                                  | 5.69 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.12 ms: 5.04x faster                                                    |
| pylint                           | 128 ms                                                   | 50.8 ms: 2.52x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 810 us: 2.48x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.06x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.88x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                     |
| mdp                              | 1.09 sec                                                 | 603 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 512 us: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.7 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 798 ns: 1.21x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.12 us: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 58.6 ms: 1.19x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.7 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 44.6 ns: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 190 ms: 1.13x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 845 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 987 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.33 us: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.4 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 455 ms: 1.09x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.57 us: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.0 ms: 1.09x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.6 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.08x faster                                                     |
| chaos                            | 28.9 ms                                                  | 27.1 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.1 ms: 1.06x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.10 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.9 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 988 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.04 ms: 1.00x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 332 ms: 1.01x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 675 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.2 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.2 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.6 ms: 1.05x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.8 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.6 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.1 ms: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 54.3 ms: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                     |
| shortest_path                    | 219 ms                                                   | 247 ms: 1.13x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 44.0 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.9 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.63 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.50 ms: 1.19x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.69 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.5 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 242 ms: 1.21x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 570 us: 1.36x slower                                                     |
| many_optionals                   | 195 us                                                   | 268 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.1 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (4): pidigits, dask, json, typing_runtime_protocols
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260422-3.15.0a8+-79321fd-NOGIL/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.112x faster

# HPT report

- Reliability score: 99.87% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.38x