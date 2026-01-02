# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: darwin-arm64
- commit hash: 8f7b4f4
- commit date: 2026-01-02
- overall geometric mean: 1.272x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 107 ms: 1.07x faster                                                            |
| docutils       | 1.02 sec                                                 | 980 ms: 1.04x faster                                                            |
| html5lib       | 23.0 ms                                                  | 19.4 ms: 1.19x faster                                                           |
| sphinx         | 434 ms                                                   | 382 ms: 1.14x faster                                                            |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 215 ms: 2.30x faster                                                            |
| async_tree_io_tg                 | 480 ms                                                   | 214 ms: 2.25x faster                                                            |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.08x faster                                                            |
| async_tree_io                    | 459 ms                                                   | 224 ms: 2.05x faster                                                            |
| async_tree_none                  | 178 ms                                                   | 95.2 ms: 1.87x faster                                                           |
| async_tree_none_tg               | 172 ms                                                   | 94.5 ms: 1.82x faster                                                           |
| async_tree_memoization_tg        | 231 ms                                                   | 133 ms: 1.74x faster                                                            |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                            |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 238 ms: 1.40x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 243 ms: 1.39x faster                                                            |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                           |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.27x faster                                                            |
| async_tree_eager                 | 45.6 ms                                                  | 37.0 ms: 1.23x faster                                                           |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 210 ms: 1.10x faster                                                            |
| asyncio_websockets               | 190 ms                                                   | 181 ms: 1.05x faster                                                            |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                            |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                            |
| async_tree_eager_tg              | 32.1 ms                                                  | 75.9 ms: 2.36x slower                                                           |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 22.5 ms: 1.68x faster                                                           |
| nbody          | 54.2 ms                                                  | 38.9 ms: 1.40x faster                                                           |
| pidigits       | 161 ms                                                   | 155 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                    | 1.35x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.4 ms: 1.38x faster                                                           |
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.18x faster                                                           |
| regex_dna      | 99.6 ms                                                  | 91.8 ms: 1.09x faster                                                           |
| regex_v8       | 9.59 ms                                                  | 9.45 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                    | 1.16x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 71.6 us: 1.44x faster                                                           |
| xml_etree_iterparse  | 51.6 ms                                                  | 36.1 ms: 1.43x faster                                                           |
| xml_etree_generate   | 38.9 ms                                                  | 30.5 ms: 1.28x faster                                                           |
| pickle_pure_python   | 139 us                                                   | 110 us: 1.27x faster                                                            |
| xml_etree_process    | 26.7 ms                                                  | 21.6 ms: 1.24x faster                                                           |
| tomli_loads          | 957 ms                                                   | 788 ms: 1.21x faster                                                            |
| json_dumps           | 4.26 ms                                                  | 3.61 ms: 1.18x faster                                                           |
| xml_etree_parse      | 67.9 ms                                                  | 59.4 ms: 1.14x faster                                                           |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.05x faster                                                           |
| Geometric mean       | (ref)                                                    | 1.24x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|------------------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.08x slower                                                           |
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                           |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 4.77 ms                                                  | 3.83 ms: 1.25x faster                                                           |
| genshi_text    | 10.5 ms                                                  | 8.71 ms: 1.20x faster                                                           |
| genshi_xml     | 21.8 ms                                                  | 19.7 ms: 1.11x faster                                                           |
| Geometric mean | (ref)                                                    | 1.13x faster                                                                    |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4 |
|----------------------------------|:--------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.76 ms: 5.52x faster                                                           |
| richards                         | 22.4 ms                                                  | 9.44 ms: 2.37x faster                                                           |
| async_tree_eager_io              | 496 ms                                                   | 215 ms: 2.30x faster                                                            |
| richards_super                   | 25.4 ms                                                  | 11.3 ms: 2.25x faster                                                           |
| async_tree_io_tg                 | 480 ms                                                   | 214 ms: 2.25x faster                                                            |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.08x faster                                                            |
| async_tree_io                    | 459 ms                                                   | 224 ms: 2.05x faster                                                            |
| mdp                              | 1.09 sec                                                 | 573 ms: 1.91x faster                                                            |
| async_tree_none                  | 178 ms                                                   | 95.2 ms: 1.87x faster                                                           |
| async_tree_none_tg               | 172 ms                                                   | 94.5 ms: 1.82x faster                                                           |
| async_tree_memoization_tg        | 231 ms                                                   | 133 ms: 1.74x faster                                                            |
| float                            | 37.9 ms                                                  | 22.5 ms: 1.68x faster                                                           |
| go                               | 70.0 ms                                                  | 41.7 ms: 1.68x faster                                                           |
| deepcopy                         | 161 us                                                   | 96.4 us: 1.68x faster                                                           |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                            |
| deepcopy_memo                    | 18.3 us                                                  | 11.2 us: 1.64x faster                                                           |
| comprehensions                   | 9.84 us                                                  | 6.08 us: 1.62x faster                                                           |
| deltablue                        | 1.73 ms                                                  | 1.10 ms: 1.56x faster                                                           |
| pyflate                          | 216 ms                                                   | 141 ms: 1.54x faster                                                            |
| logging_silent                   | 50.9 ns                                                  | 33.2 ns: 1.53x faster                                                           |
| deepcopy_reduce                  | 1.46 us                                                  | 1.00 us: 1.46x faster                                                           |
| scimark_sor                      | 61.0 ms                                                  | 41.9 ms: 1.46x faster                                                           |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.3 ms: 1.44x faster                                                           |
| unpickle_pure_python             | 103 us                                                   | 71.6 us: 1.44x faster                                                           |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.1 ms: 1.43x faster                                                           |
| scimark_lu                       | 51.3 ms                                                  | 36.1 ms: 1.42x faster                                                           |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 238 ms: 1.40x faster                                                            |
| raytrace                         | 145 ms                                                   | 104 ms: 1.40x faster                                                            |
| nbody                            | 54.2 ms                                                  | 38.9 ms: 1.40x faster                                                           |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 243 ms: 1.39x faster                                                            |
| scimark_fft                      | 142 ms                                                   | 102 ms: 1.39x faster                                                            |
| regex_compile                    | 54.6 ms                                                  | 39.4 ms: 1.38x faster                                                           |
| chaos                            | 28.9 ms                                                  | 21.4 ms: 1.35x faster                                                           |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                           |
| spectral_norm                    | 54.4 ms                                                  | 40.6 ms: 1.34x faster                                                           |
| pprint_pformat                   | 665 ms                                                   | 509 ms: 1.31x faster                                                            |
| pprint_safe_repr                 | 328 ms                                                   | 251 ms: 1.30x faster                                                            |
| k_core                           | 1.12 sec                                                 | 861 ms: 1.30x faster                                                            |
| crypto_pyaes                     | 38.8 ms                                                  | 30.0 ms: 1.29x faster                                                           |
| xml_etree_generate               | 38.9 ms                                                  | 30.5 ms: 1.28x faster                                                           |
| pickle_pure_python               | 139 us                                                   | 110 us: 1.27x faster                                                            |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.27x faster                                                            |
| mako                             | 4.77 ms                                                  | 3.83 ms: 1.25x faster                                                           |
| xml_etree_process                | 26.7 ms                                                  | 21.6 ms: 1.24x faster                                                           |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.81 sec: 1.24x faster                                                          |
| logging_simple                   | 2.57 us                                                  | 2.08 us: 1.23x faster                                                           |
| async_tree_eager                 | 45.6 ms                                                  | 37.0 ms: 1.23x faster                                                           |
| generators                       | 21.9 ms                                                  | 17.9 ms: 1.23x faster                                                           |
| logging_format                   | 2.80 us                                                  | 2.30 us: 1.22x faster                                                           |
| tomli_loads                      | 957 ms                                                   | 788 ms: 1.21x faster                                                            |
| genshi_text                      | 10.5 ms                                                  | 8.71 ms: 1.20x faster                                                           |
| html5lib                         | 23.0 ms                                                  | 19.4 ms: 1.19x faster                                                           |
| hexiom                           | 3.04 ms                                                  | 2.58 ms: 1.18x faster                                                           |
| json_dumps                       | 4.26 ms                                                  | 3.61 ms: 1.18x faster                                                           |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.18x faster                                                           |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                           |
| fannkuch                         | 176 ms                                                   | 151 ms: 1.17x faster                                                            |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.16x faster                                                           |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                            |
| typing_runtime_protocols         | 71.0 us                                                  | 61.2 us: 1.16x faster                                                           |
| pycparser                        | 497 ms                                                   | 430 ms: 1.16x faster                                                            |
| nqueens                          | 43.5 ms                                                  | 37.8 ms: 1.15x faster                                                           |
| xml_etree_parse                  | 67.9 ms                                                  | 59.4 ms: 1.14x faster                                                           |
| sphinx                           | 434 ms                                                   | 382 ms: 1.14x faster                                                            |
| thrift                           | 322 us                                                   | 284 us: 1.13x faster                                                            |
| genshi_xml                       | 21.8 ms                                                  | 19.7 ms: 1.11x faster                                                           |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 210 ms: 1.10x faster                                                            |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                           |
| regex_dna                        | 99.6 ms                                                  | 91.8 ms: 1.09x faster                                                           |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                            |
| json                             | 1.93 ms                                                  | 1.79 ms: 1.08x faster                                                           |
| sympy_integrate                  | 8.02 ms                                                  | 7.45 ms: 1.08x faster                                                           |
| meteor_contest                   | 47.7 ms                                                  | 44.5 ms: 1.07x faster                                                           |
| 2to3                             | 114 ms                                                   | 107 ms: 1.07x faster                                                            |
| asyncio_websockets               | 190 ms                                                   | 181 ms: 1.05x faster                                                            |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.05x faster                                                           |
| docutils                         | 1.02 sec                                                 | 980 ms: 1.04x faster                                                            |
| pidigits                         | 161 ms                                                   | 155 ms: 1.04x faster                                                            |
| sympy_sum                        | 57.6 ms                                                  | 55.6 ms: 1.04x faster                                                           |
| sqlite_synth                     | 967 ns                                                   | 944 ns: 1.02x faster                                                            |
| telco                            | 2.61 ms                                                  | 2.56 ms: 1.02x faster                                                           |
| regex_v8                         | 9.59 ms                                                  | 9.45 ms: 1.01x faster                                                           |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                            |
| connected_components             | 201 ms                                                   | 198 ms: 1.01x faster                                                            |
| bench_thread_pool                | 419 us                                                   | 426 us: 1.02x slower                                                            |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.03x slower                                                            |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.05x slower                                                            |
| create_gc_cycles                 | 830 us                                                   | 885 us: 1.07x slower                                                            |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.08x slower                                                           |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                            |
| bench_mp_pool                    | 39.7 ms                                                  | 43.5 ms: 1.10x slower                                                           |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                           |
| coverage                         | 26.9 ms                                                  | 32.1 ms: 1.19x slower                                                           |
| many_optionals                   | 195 us                                                   | 240 us: 1.23x slower                                                            |
| async_tree_eager_tg              | 32.1 ms                                                  | 75.9 ms: 2.36x slower                                                           |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                                    |

Benchmark hidden because not significant (3): gc_traversal, sympy_str, django_template
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260102-3.15.0a3+-8f7b4f4-JIT/bm-20260102-macm4pro-arm64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-8f7b4f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.272x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.25x