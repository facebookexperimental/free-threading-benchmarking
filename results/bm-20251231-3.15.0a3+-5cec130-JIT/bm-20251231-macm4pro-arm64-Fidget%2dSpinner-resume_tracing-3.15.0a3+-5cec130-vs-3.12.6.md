# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 5cec130
- commit date: 2025-12-31
- overall geometric mean: 1.243x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.02x faster                                                         |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                       |
| html5lib       | 23.0 ms                                                  | 19.7 ms: 1.17x faster                                                        |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                         |
| Geometric mean | (ref)                                                    | 1.06x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 209 ms: 2.29x faster                                                         |
| async_tree_eager_io              | 496 ms                                                   | 217 ms: 2.29x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 212 ms: 2.10x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 223 ms: 2.06x faster                                                         |
| async_tree_none_tg               | 172 ms                                                   | 92.7 ms: 1.86x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 96.1 ms: 1.86x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 130 ms: 1.77x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.67x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.36x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                        |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.04x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 24.2 ms: 1.57x faster                                                        |
| nbody          | 54.2 ms                                                  | 39.4 ms: 1.38x faster                                                        |
| Geometric mean | (ref)                                                    | 1.29x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.7 ms: 1.38x faster                                                        |
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                        |
| regex_dna      | 99.6 ms                                                  | 94.5 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                    | 1.14x faster                                                                 |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 72.4 us: 1.42x faster                                                        |
| xml_etree_iterparse  | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                        |
| pickle_pure_python   | 139 us                                                   | 110 us: 1.26x faster                                                         |
| xml_etree_process    | 26.7 ms                                                  | 22.0 ms: 1.22x faster                                                        |
| tomli_loads          | 957 ms                                                   | 793 ms: 1.21x faster                                                         |
| xml_etree_generate   | 38.9 ms                                                  | 33.0 ms: 1.18x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.67 ms: 1.16x faster                                                        |
| xml_etree_parse      | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.03x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.21x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.79 ms: 1.10x slower                                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                        |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.10 ms: 1.17x faster                                                        |
| genshi_text     | 10.5 ms                                                  | 9.37 ms: 1.12x faster                                                        |
| django_template | 13.6 ms                                                  | 13.1 ms: 1.04x faster                                                        |
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                        |
| Geometric mean  | (ref)                                                    | 1.07x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.92 ms: 5.30x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 209 ms: 2.29x faster                                                         |
| async_tree_eager_io              | 496 ms                                                   | 217 ms: 2.29x faster                                                         |
| richards                         | 22.4 ms                                                  | 10.2 ms: 2.21x faster                                                        |
| richards_super                   | 25.4 ms                                                  | 11.9 ms: 2.14x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 212 ms: 2.10x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 223 ms: 2.06x faster                                                         |
| async_tree_none_tg               | 172 ms                                                   | 92.7 ms: 1.86x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 96.1 ms: 1.86x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 130 ms: 1.77x faster                                                         |
| mdp                              | 1.09 sec                                                 | 634 ms: 1.72x faster                                                         |
| go                               | 70.0 ms                                                  | 42.0 ms: 1.67x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.67x faster                                                         |
| deltablue                        | 1.73 ms                                                  | 1.09 ms: 1.58x faster                                                        |
| deepcopy                         | 161 us                                                   | 102 us: 1.58x faster                                                         |
| comprehensions                   | 9.84 us                                                  | 6.22 us: 1.58x faster                                                        |
| float                            | 37.9 ms                                                  | 24.2 ms: 1.57x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 40.4 ms: 1.51x faster                                                        |
| pyflate                          | 216 ms                                                   | 143 ms: 1.51x faster                                                         |
| logging_silent                   | 50.9 ns                                                  | 34.2 ns: 1.49x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.02 us: 1.44x faster                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.5 ms: 1.43x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 1.79 us: 1.43x faster                                                        |
| raytrace                         | 145 ms                                                   | 102 ms: 1.43x faster                                                         |
| logging_format                   | 2.80 us                                                  | 1.97 us: 1.42x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 72.4 us: 1.42x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 101 ms: 1.41x faster                                                         |
| scimark_lu                       | 51.3 ms                                                  | 36.5 ms: 1.41x faster                                                        |
| chaos                            | 28.9 ms                                                  | 21.0 ms: 1.38x faster                                                        |
| nbody                            | 54.2 ms                                                  | 39.4 ms: 1.38x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 39.7 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.36x faster                                                         |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.2 ms: 1.32x faster                                                        |
| k_core                           | 1.12 sec                                                 | 863 ms: 1.30x faster                                                         |
| pickle_pure_python               | 139 us                                                   | 110 us: 1.26x faster                                                         |
| pprint_pformat                   | 665 ms                                                   | 531 ms: 1.25x faster                                                         |
| crypto_pyaes                     | 38.8 ms                                                  | 31.0 ms: 1.25x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 263 ms: 1.25x faster                                                         |
| xml_etree_process                | 26.7 ms                                                  | 22.0 ms: 1.22x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                         |
| tomli_loads                      | 957 ms                                                   | 793 ms: 1.21x faster                                                         |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 33.0 ms: 1.18x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 19.7 ms: 1.17x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.10 ms: 1.17x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.67 ms: 1.16x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                        |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                        |
| fannkuch                         | 176 ms                                                   | 153 ms: 1.15x faster                                                         |
| hexiom                           | 3.04 ms                                                  | 2.65 ms: 1.15x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.15x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 62.4 us: 1.14x faster                                                        |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                         |
| thrift                           | 322 us                                                   | 287 us: 1.12x faster                                                         |
| genshi_text                      | 10.5 ms                                                  | 9.37 ms: 1.12x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 39.2 ms: 1.11x faster                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.09x faster                                                        |
| pycparser                        | 497 ms                                                   | 463 ms: 1.08x faster                                                         |
| meteor_contest                   | 47.7 ms                                                  | 44.9 ms: 1.06x faster                                                        |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                         |
| regex_dna                        | 99.6 ms                                                  | 94.5 ms: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                         |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.05x faster                                                        |
| django_template                  | 13.6 ms                                                  | 13.1 ms: 1.04x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.03x faster                                                        |
| 2to3                             | 114 ms                                                   | 111 ms: 1.02x faster                                                         |
| connected_components             | 201 ms                                                   | 197 ms: 1.02x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                         |
| telco                            | 2.61 ms                                                  | 2.58 ms: 1.01x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 956 ns: 1.01x faster                                                         |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                         |
| gc_traversal                     | 2.01 ms                                                  | 2.04 ms: 1.02x slower                                                        |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                       |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.03x slower                                                         |
| sympy_integrate                  | 8.02 ms                                                  | 8.33 ms: 1.04x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.04x slower                                                         |
| sympy_sum                        | 57.6 ms                                                  | 61.2 ms: 1.06x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 179 ms: 1.07x slower                                                         |
| python_startup                   | 8.01 ms                                                  | 8.79 ms: 1.10x slower                                                        |
| create_gc_cycles                 | 830 us                                                   | 914 us: 1.10x slower                                                         |
| sympy_str                        | 104 ms                                                   | 115 ms: 1.10x slower                                                         |
| python_startup_no_site           | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 44.6 ms: 1.12x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                         |
| coverage                         | 26.9 ms                                                  | 32.1 ms: 1.20x slower                                                        |
| many_optionals                   | 195 us                                                   | 259 us: 1.33x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                                 |

Benchmark hidden because not significant (3): pidigits, regex_v8, pylint
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251231-3.15.0a3+-5cec130-JIT/bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-5cec130.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.243x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.15x
- 95% likely to have a speedup of 1.14x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: 1.25x