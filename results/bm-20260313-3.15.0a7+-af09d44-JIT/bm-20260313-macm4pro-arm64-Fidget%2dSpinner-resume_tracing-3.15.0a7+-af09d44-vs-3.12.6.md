# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: af09d44
- commit date: 2026-03-13
- overall geometric mean: 1.287x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.28x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                         |
| docutils       | 1.02 sec                                                 | 963 ms: 1.06x faster                                                         |
| html5lib       | 23.0 ms                                                  | 19.2 ms: 1.20x faster                                                        |
| sphinx         | 434 ms                                                   | 388 ms: 1.12x faster                                                         |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 208 ms: 2.30x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 203 ms: 2.19x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 89.5 ms: 1.99x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 90.9 ms: 1.89x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 129 ms: 1.79x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 127 ms: 1.75x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 9.15 ms: 1.48x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 241 ms: 1.41x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 101 ms: 1.30x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 36.3 ms: 1.26x faster                                                        |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 212 ms: 1.09x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 116 ms: 1.03x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.2 ms: 2.40x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.41x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.6 ms: 1.60x faster                                                        |
| nbody          | 54.2 ms                                                  | 40.1 ms: 1.35x faster                                                        |
| Geometric mean | (ref)                                                    | 1.30x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.5 ms: 1.38x faster                                                        |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                        |
| regex_dna      | 99.6 ms                                                  | 94.3 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                    | 1.14x faster                                                                 |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 630 ms: 1.52x faster                                                         |
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                        |
| xml_etree_process    | 26.7 ms                                                  | 21.3 ms: 1.25x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 31.5 ms: 1.23x faster                                                        |
| unpickle_pure_python | 103 us                                                   | 84.2 us: 1.22x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.51 ms: 1.21x faster                                                        |
| pickle_pure_python   | 139 us                                                   | 125 us: 1.11x faster                                                         |
| xml_etree_parse      | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.05x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.22x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                        |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.97 ms: 1.20x faster                                                        |
| django_template | 13.6 ms                                                  | 12.5 ms: 1.09x faster                                                        |
| Geometric mean  | (ref)                                                    | 1.15x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.52 ms: 5.91x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 208 ms: 2.30x faster                                                         |
| richards                         | 22.4 ms                                                  | 9.83 ms: 2.28x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                         |
| richards_super                   | 25.4 ms                                                  | 11.5 ms: 2.21x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 203 ms: 2.19x faster                                                         |
| mdp                              | 1.09 sec                                                 | 511 ms: 2.14x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 89.5 ms: 1.99x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 90.9 ms: 1.89x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 10.0 us: 1.82x faster                                                        |
| scimark_lu                       | 51.3 ms                                                  | 28.2 ms: 1.82x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 129 ms: 1.79x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 127 ms: 1.75x faster                                                         |
| deepcopy                         | 161 us                                                   | 93.4 us: 1.73x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 37.1 ms: 1.64x faster                                                        |
| float                            | 37.9 ms                                                  | 23.6 ms: 1.60x faster                                                        |
| deltablue                        | 1.73 ms                                                  | 1.11 ms: 1.56x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 630 ms: 1.52x faster                                                         |
| go                               | 70.0 ms                                                  | 46.3 ms: 1.51x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.15 ms: 1.48x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 34.4 ns: 1.48x faster                                                        |
| logging_format                   | 2.80 us                                                  | 1.90 us: 1.47x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 994 ns: 1.47x faster                                                         |
| pyflate                          | 216 ms                                                   | 147 ms: 1.47x faster                                                         |
| scimark_fft                      | 142 ms                                                   | 97.0 ms: 1.46x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 1.76 us: 1.46x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 37.7 ms: 1.44x faster                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.7 ms: 1.42x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 241 ms: 1.41x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                         |
| regex_compile                    | 54.6 ms                                                  | 39.5 ms: 1.38x faster                                                        |
| chaos                            | 28.9 ms                                                  | 21.3 ms: 1.36x faster                                                        |
| nbody                            | 54.2 ms                                                  | 40.1 ms: 1.35x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 7.33 us: 1.34x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 32.4 ms: 1.34x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                        |
| raytrace                         | 145 ms                                                   | 111 ms: 1.31x faster                                                         |
| pprint_safe_repr                 | 328 ms                                                   | 251 ms: 1.31x faster                                                         |
| pprint_pformat                   | 665 ms                                                   | 509 ms: 1.31x faster                                                         |
| k_core                           | 1.12 sec                                                 | 857 ms: 1.30x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 101 ms: 1.30x faster                                                         |
| hexiom                           | 3.04 ms                                                  | 2.39 ms: 1.27x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.77 sec: 1.27x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 36.3 ms: 1.26x faster                                                        |
| generators                       | 21.9 ms                                                  | 17.5 ms: 1.25x faster                                                        |
| xml_etree_process                | 26.7 ms                                                  | 21.3 ms: 1.25x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 31.5 ms: 1.23x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 31.7 ms: 1.23x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 84.2 us: 1.22x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.51 ms: 1.21x faster                                                        |
| mako                             | 4.77 ms                                                  | 3.97 ms: 1.20x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 19.2 ms: 1.20x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.19x faster                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.17x faster                                                        |
| fannkuch                         | 176 ms                                                   | 151 ms: 1.16x faster                                                         |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                        |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                         |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 62.1 us: 1.14x faster                                                        |
| pycparser                        | 497 ms                                                   | 442 ms: 1.13x faster                                                         |
| sphinx                           | 434 ms                                                   | 388 ms: 1.12x faster                                                         |
| pickle_pure_python               | 139 us                                                   | 125 us: 1.11x faster                                                         |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                         |
| django_template                  | 13.6 ms                                                  | 12.5 ms: 1.09x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 212 ms: 1.09x faster                                                         |
| xml_etree_parse                  | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                        |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                         |
| json                             | 1.93 ms                                                  | 1.82 ms: 1.06x faster                                                        |
| docutils                         | 1.02 sec                                                 | 963 ms: 1.06x faster                                                         |
| regex_dna                        | 99.6 ms                                                  | 94.3 ms: 1.06x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 45.4 ms: 1.05x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.66 ms: 1.05x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.05x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 55.6 ms: 1.04x faster                                                        |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                         |
| sqlite_synth                     | 967 ns                                                   | 939 ns: 1.03x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                         |
| connected_components             | 201 ms                                                   | 196 ms: 1.03x faster                                                         |
| telco                            | 2.61 ms                                                  | 2.56 ms: 1.02x faster                                                        |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                         |
| sympy_expand                     | 167 ms                                                   | 164 ms: 1.02x faster                                                         |
| sympy_str                        | 104 ms                                                   | 103 ms: 1.01x faster                                                         |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                         |
| gc_traversal                     | 2.01 ms                                                  | 2.02 ms: 1.01x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 116 ms: 1.03x slower                                                         |
| python_startup                   | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                        |
| create_gc_cycles                 | 830 us                                                   | 904 us: 1.09x slower                                                         |
| python_startup_no_site           | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 235 ms: 1.11x slower                                                         |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.12x slower                                                        |
| many_optionals                   | 195 us                                                   | 225 us: 1.15x slower                                                         |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.2 ms: 2.40x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                                 |

Benchmark hidden because not significant (2): regex_v8, pidigits
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260313-3.15.0a7+-af09d44-JIT/bm-20260313-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-af09d44.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.287x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.28x