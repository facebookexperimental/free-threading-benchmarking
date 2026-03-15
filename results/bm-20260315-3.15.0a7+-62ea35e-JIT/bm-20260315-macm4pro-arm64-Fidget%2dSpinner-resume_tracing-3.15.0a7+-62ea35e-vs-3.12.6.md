# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 62ea35e
- commit date: 2026-03-15
- overall geometric mean: 1.301x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.28x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.04x faster                                                         |
| docutils       | 1.02 sec                                                 | 953 ms: 1.07x faster                                                         |
| html5lib       | 23.0 ms                                                  | 18.7 ms: 1.23x faster                                                        |
| sphinx         | 434 ms                                                   | 383 ms: 1.13x faster                                                         |
| Geometric mean | (ref)                                                    | 1.12x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 207 ms: 2.32x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 204 ms: 2.25x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 202 ms: 2.21x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 87.9 ms: 2.03x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 89.0 ms: 1.93x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 127 ms: 1.82x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 126 ms: 1.77x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 9.20 ms: 1.48x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 235 ms: 1.42x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 102 ms: 1.29x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 35.9 ms: 1.27x faster                                                        |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 210 ms: 1.10x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 116 ms: 1.03x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.7 ms: 2.39x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.43x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.3 ms: 1.63x faster                                                        |
| nbody          | 54.2 ms                                                  | 39.9 ms: 1.36x faster                                                        |
| pidigits       | 161 ms                                                   | 157 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                    | 1.31x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.2 ms: 1.39x faster                                                        |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                        |
| regex_dna      | 99.6 ms                                                  | 92.7 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                    | 1.14x faster                                                                 |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 617 ms: 1.55x faster                                                         |
| xml_etree_iterparse  | 51.6 ms                                                  | 37.6 ms: 1.37x faster                                                        |
| xml_etree_process    | 26.7 ms                                                  | 21.2 ms: 1.26x faster                                                        |
| unpickle_pure_python | 103 us                                                   | 83.9 us: 1.23x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 31.7 ms: 1.23x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.48 ms: 1.22x faster                                                        |
| pickle_pure_python   | 139 us                                                   | 124 us: 1.12x faster                                                         |
| xml_etree_parse      | 67.9 ms                                                  | 62.3 ms: 1.09x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.2 us: 1.06x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.23x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.64 ms: 1.08x slower                                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.22 ms: 1.09x slower                                                        |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.97 ms: 1.20x faster                                                        |
| django_template | 13.6 ms                                                  | 12.3 ms: 1.10x faster                                                        |
| Geometric mean  | (ref)                                                    | 1.15x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.46 ms: 6.00x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                         |
| richards                         | 22.4 ms                                                  | 9.66 ms: 2.32x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 207 ms: 2.32x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 204 ms: 2.25x faster                                                         |
| richards_super                   | 25.4 ms                                                  | 11.4 ms: 2.23x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 202 ms: 2.21x faster                                                         |
| mdp                              | 1.09 sec                                                 | 520 ms: 2.10x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 87.9 ms: 2.03x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 89.0 ms: 1.93x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 9.98 us: 1.83x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 127 ms: 1.82x faster                                                         |
| scimark_lu                       | 51.3 ms                                                  | 28.6 ms: 1.79x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 126 ms: 1.77x faster                                                         |
| deepcopy                         | 161 us                                                   | 92.4 us: 1.75x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 5.82 us: 1.69x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 36.6 ms: 1.67x faster                                                        |
| float                            | 37.9 ms                                                  | 23.3 ms: 1.63x faster                                                        |
| deltablue                        | 1.73 ms                                                  | 1.11 ms: 1.56x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 617 ms: 1.55x faster                                                         |
| go                               | 70.0 ms                                                  | 45.4 ms: 1.54x faster                                                        |
| pyflate                          | 216 ms                                                   | 144 ms: 1.50x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 9.20 ms: 1.48x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 1.74 us: 1.47x faster                                                        |
| logging_format                   | 2.80 us                                                  | 1.90 us: 1.47x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 998 ns: 1.46x faster                                                         |
| logging_silent                   | 50.9 ns                                                  | 35.0 ns: 1.46x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 98.4 ms: 1.44x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 37.8 ms: 1.44x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                         |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.7 ms: 1.42x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 235 ms: 1.42x faster                                                         |
| chaos                            | 28.9 ms                                                  | 20.7 ms: 1.39x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 39.2 ms: 1.39x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.6 ms: 1.37x faster                                                        |
| nbody                            | 54.2 ms                                                  | 39.9 ms: 1.36x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 32.1 ms: 1.35x faster                                                        |
| raytrace                         | 145 ms                                                   | 110 ms: 1.32x faster                                                         |
| pprint_safe_repr                 | 328 ms                                                   | 249 ms: 1.32x faster                                                         |
| pprint_pformat                   | 665 ms                                                   | 507 ms: 1.31x faster                                                         |
| k_core                           | 1.12 sec                                                 | 854 ms: 1.31x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 102 ms: 1.29x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 35.9 ms: 1.27x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.40 ms: 1.27x faster                                                        |
| xml_etree_process                | 26.7 ms                                                  | 21.2 ms: 1.26x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.77 sec: 1.26x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 31.3 ms: 1.24x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 18.7 ms: 1.23x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 83.9 us: 1.23x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 31.7 ms: 1.23x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.48 ms: 1.22x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 17.6 ms: 1.21x faster                                                        |
| mako                             | 4.77 ms                                                  | 3.97 ms: 1.20x faster                                                        |
| generators                       | 21.9 ms                                                  | 18.2 ms: 1.20x faster                                                        |
| fannkuch                         | 176 ms                                                   | 148 ms: 1.18x faster                                                         |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                        |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                         |
| typing_runtime_protocols         | 71.0 us                                                  | 62.1 us: 1.14x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.14x faster                                                        |
| sphinx                           | 434 ms                                                   | 383 ms: 1.13x faster                                                         |
| pycparser                        | 497 ms                                                   | 440 ms: 1.13x faster                                                         |
| pickle_pure_python               | 139 us                                                   | 124 us: 1.12x faster                                                         |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                         |
| django_template                  | 13.6 ms                                                  | 12.3 ms: 1.10x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 210 ms: 1.10x faster                                                         |
| xml_etree_parse                  | 67.9 ms                                                  | 62.3 ms: 1.09x faster                                                        |
| thrift                           | 322 us                                                   | 298 us: 1.08x faster                                                         |
| meteor_contest                   | 47.7 ms                                                  | 44.2 ms: 1.08x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 53.4 ms: 1.08x faster                                                        |
| json                             | 1.93 ms                                                  | 1.80 ms: 1.08x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 92.7 ms: 1.07x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.47 ms: 1.07x faster                                                        |
| docutils                         | 1.02 sec                                                 | 953 ms: 1.07x faster                                                         |
| json_loads                       | 10.9 us                                                  | 10.2 us: 1.06x faster                                                        |
| sympy_str                        | 104 ms                                                   | 99.4 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                         |
| 2to3                             | 114 ms                                                   | 110 ms: 1.04x faster                                                         |
| sqlite_synth                     | 967 ns                                                   | 933 ns: 1.04x faster                                                         |
| sympy_expand                     | 167 ms                                                   | 162 ms: 1.03x faster                                                         |
| connected_components             | 201 ms                                                   | 195 ms: 1.03x faster                                                         |
| pidigits                         | 161 ms                                                   | 157 ms: 1.02x faster                                                         |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                         |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                         |
| gc_traversal                     | 2.01 ms                                                  | 1.98 ms: 1.01x faster                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 116 ms: 1.03x slower                                                         |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.04x slower                                                         |
| create_gc_cycles                 | 830 us                                                   | 878 us: 1.06x slower                                                         |
| python_startup                   | 8.01 ms                                                  | 8.64 ms: 1.08x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.22 ms: 1.09x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 232 ms: 1.09x slower                                                         |
| bench_mp_pool                    | 39.7 ms                                                  | 43.8 ms: 1.10x slower                                                        |
| many_optionals                   | 195 us                                                   | 222 us: 1.13x slower                                                         |
| coverage                         | 26.9 ms                                                  | 32.5 ms: 1.21x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.7 ms: 2.39x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.29x faster                                                                 |

Benchmark hidden because not significant (2): regex_v8, telco
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260315-3.15.0a7+-62ea35e-JIT/bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.301x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.28x