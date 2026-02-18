# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: no_invalidate_func
- machine: darwin-arm64
- commit hash: 170839d
- commit date: 2026-02-18
- overall geometric mean: 1.253x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                             |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                           |
| html5lib       | 23.0 ms                                                  | 20.5 ms: 1.12x faster                                                            |
| sphinx         | 434 ms                                                   | 395 ms: 1.10x faster                                                             |
| Geometric mean | (ref)                                                    | 1.06x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.32x faster                                                             |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                             |
| async_tree_io                    | 459 ms                                                   | 219 ms: 2.10x faster                                                             |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                             |
| async_tree_none                  | 178 ms                                                   | 94.9 ms: 1.88x faster                                                            |
| async_tree_none_tg               | 172 ms                                                   | 95.0 ms: 1.81x faster                                                            |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                             |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                             |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                            |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                             |
| async_tree_eager                 | 45.6 ms                                                  | 36.9 ms: 1.24x faster                                                            |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.07x faster                                                             |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                             |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                             |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 236 ms: 1.11x slower                                                             |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.45x slower                                                            |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 24.0 ms: 1.58x faster                                                            |
| nbody          | 54.2 ms                                                  | 40.0 ms: 1.35x faster                                                            |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                    | 1.27x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.4 ms: 1.35x faster                                                            |
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                            |
| regex_dna      | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                            |
| regex_v8       | 9.59 ms                                                  | 9.76 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 658 ms: 1.45x faster                                                             |
| xml_etree_iterparse  | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                            |
| xml_etree_generate   | 38.9 ms                                                  | 30.8 ms: 1.26x faster                                                            |
| xml_etree_process    | 26.7 ms                                                  | 21.8 ms: 1.23x faster                                                            |
| unpickle_pure_python | 103 us                                                   | 84.8 us: 1.21x faster                                                            |
| json_dumps           | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                            |
| pickle_pure_python   | 139 us                                                   | 126 us: 1.11x faster                                                             |
| xml_etree_parse      | 67.9 ms                                                  | 64.1 ms: 1.06x faster                                                            |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                            |
| Geometric mean       | (ref)                                                    | 1.20x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.08 ms: 1.13x slower                                                            |
| python_startup_no_site | 5.71 ms                                                  | 6.55 ms: 1.15x slower                                                            |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.95 ms: 1.21x faster                                                            |
| django_template | 13.6 ms                                                  | 13.8 ms: 1.01x slower                                                            |
| Geometric mean  | (ref)                                                    | 1.09x faster                                                                     |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.61 ms: 5.76x faster                                                            |
| richards                         | 22.4 ms                                                  | 9.54 ms: 2.35x faster                                                            |
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.32x faster                                                             |
| richards_super                   | 25.4 ms                                                  | 11.3 ms: 2.24x faster                                                            |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                             |
| async_tree_io                    | 459 ms                                                   | 219 ms: 2.10x faster                                                             |
| mdp                              | 1.09 sec                                                 | 535 ms: 2.04x faster                                                             |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                             |
| async_tree_none                  | 178 ms                                                   | 94.9 ms: 1.88x faster                                                            |
| async_tree_none_tg               | 172 ms                                                   | 95.0 ms: 1.81x faster                                                            |
| scimark_lu                       | 51.3 ms                                                  | 28.5 ms: 1.80x faster                                                            |
| deepcopy_memo                    | 18.3 us                                                  | 10.4 us: 1.75x faster                                                            |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                             |
| deepcopy                         | 161 us                                                   | 94.1 us: 1.72x faster                                                            |
| comprehensions                   | 9.84 us                                                  | 5.86 us: 1.68x faster                                                            |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.67x faster                                                             |
| float                            | 37.9 ms                                                  | 24.0 ms: 1.58x faster                                                            |
| scimark_sor                      | 61.0 ms                                                  | 39.4 ms: 1.55x faster                                                            |
| deltablue                        | 1.73 ms                                                  | 1.16 ms: 1.48x faster                                                            |
| deepcopy_reduce                  | 1.46 us                                                  | 994 ns: 1.47x faster                                                             |
| go                               | 70.0 ms                                                  | 47.8 ms: 1.47x faster                                                            |
| tomli_loads                      | 957 ms                                                   | 658 ms: 1.45x faster                                                             |
| scimark_fft                      | 142 ms                                                   | 97.8 ms: 1.45x faster                                                            |
| logging_silent                   | 50.9 ns                                                  | 35.3 ns: 1.44x faster                                                            |
| pyflate                          | 216 ms                                                   | 152 ms: 1.43x faster                                                             |
| scimark_monte_carlo              | 32.2 ms                                                  | 23.0 ms: 1.40x faster                                                            |
| spectral_norm                    | 54.4 ms                                                  | 39.2 ms: 1.39x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.37x faster                                                             |
| nbody                            | 54.2 ms                                                  | 40.0 ms: 1.35x faster                                                            |
| regex_compile                    | 54.6 ms                                                  | 40.4 ms: 1.35x faster                                                            |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                             |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                            |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.1 ms: 1.32x faster                                                            |
| pprint_pformat                   | 665 ms                                                   | 510 ms: 1.30x faster                                                             |
| k_core                           | 1.12 sec                                                 | 865 ms: 1.29x faster                                                             |
| pprint_safe_repr                 | 328 ms                                                   | 254 ms: 1.29x faster                                                             |
| chaos                            | 28.9 ms                                                  | 22.5 ms: 1.29x faster                                                            |
| raytrace                         | 145 ms                                                   | 113 ms: 1.29x faster                                                             |
| nqueens                          | 43.5 ms                                                  | 34.4 ms: 1.26x faster                                                            |
| xml_etree_generate               | 38.9 ms                                                  | 30.8 ms: 1.26x faster                                                            |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                             |
| hexiom                           | 3.04 ms                                                  | 2.44 ms: 1.25x faster                                                            |
| async_tree_eager                 | 45.6 ms                                                  | 36.9 ms: 1.24x faster                                                            |
| xml_etree_process                | 26.7 ms                                                  | 21.8 ms: 1.23x faster                                                            |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.84 sec: 1.22x faster                                                           |
| crypto_pyaes                     | 38.8 ms                                                  | 31.9 ms: 1.22x faster                                                            |
| unpickle_pure_python             | 103 us                                                   | 84.8 us: 1.21x faster                                                            |
| mako                             | 4.77 ms                                                  | 3.95 ms: 1.21x faster                                                            |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.19x faster                                                            |
| json_dumps                       | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                            |
| logging_format                   | 2.80 us                                                  | 2.36 us: 1.19x faster                                                            |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                            |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                            |
| fannkuch                         | 176 ms                                                   | 154 ms: 1.14x faster                                                             |
| pycparser                        | 497 ms                                                   | 438 ms: 1.14x faster                                                             |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                            |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.84 ms: 1.13x faster                                                            |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                             |
| html5lib                         | 23.0 ms                                                  | 20.5 ms: 1.12x faster                                                            |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                            |
| typing_runtime_protocols         | 71.0 us                                                  | 64.0 us: 1.11x faster                                                            |
| pickle_pure_python               | 139 us                                                   | 126 us: 1.11x faster                                                             |
| sphinx                           | 434 ms                                                   | 395 ms: 1.10x faster                                                             |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                             |
| sympy_integrate                  | 8.02 ms                                                  | 7.44 ms: 1.08x faster                                                            |
| thrift                           | 322 us                                                   | 301 us: 1.07x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.07x faster                                                             |
| sympy_str                        | 104 ms                                                   | 98.3 ms: 1.06x faster                                                            |
| xml_etree_parse                  | 67.9 ms                                                  | 64.1 ms: 1.06x faster                                                            |
| sympy_sum                        | 57.6 ms                                                  | 54.7 ms: 1.05x faster                                                            |
| meteor_contest                   | 47.7 ms                                                  | 45.8 ms: 1.04x faster                                                            |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                            |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                             |
| connected_components             | 201 ms                                                   | 196 ms: 1.03x faster                                                             |
| sqlite_synth                     | 967 ns                                                   | 943 ns: 1.03x faster                                                             |
| shortest_path                    | 219 ms                                                   | 214 ms: 1.02x faster                                                             |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                            |
| regex_dna                        | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                            |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                             |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                             |
| sympy_expand                     | 167 ms                                                   | 167 ms: 1.00x faster                                                             |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                           |
| django_template                  | 13.6 ms                                                  | 13.8 ms: 1.01x slower                                                            |
| regex_v8                         | 9.59 ms                                                  | 9.76 ms: 1.02x slower                                                            |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                             |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                             |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                            |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                             |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 236 ms: 1.11x slower                                                             |
| create_gc_cycles                 | 830 us                                                   | 932 us: 1.12x slower                                                             |
| python_startup                   | 8.01 ms                                                  | 9.08 ms: 1.13x slower                                                            |
| python_startup_no_site           | 5.71 ms                                                  | 6.55 ms: 1.15x slower                                                            |
| bench_mp_pool                    | 39.7 ms                                                  | 45.7 ms: 1.15x slower                                                            |
| many_optionals                   | 195 us                                                   | 237 us: 1.22x slower                                                             |
| coverage                         | 26.9 ms                                                  | 33.7 ms: 1.25x slower                                                            |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.45x slower                                                            |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                                     |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260218-3.15.0a6+-170839d-JIT/bm-20260218-macm4pro-arm64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.253x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.14x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: 1.27x