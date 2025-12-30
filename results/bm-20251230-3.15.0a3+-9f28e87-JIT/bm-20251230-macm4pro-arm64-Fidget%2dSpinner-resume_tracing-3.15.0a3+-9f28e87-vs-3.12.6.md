# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 9f28e87
- commit date: 2025-12-30
- overall geometric mean: 1.211x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                         |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                       |
| html5lib       | 23.0 ms                                                  | 20.5 ms: 1.12x faster                                                        |
| sphinx         | 434 ms                                                   | 407 ms: 1.06x faster                                                         |
| Geometric mean | (ref)                                                    | 1.05x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.27x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 216 ms: 2.22x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.00x faster                                                         |
| async_tree_none_tg               | 172 ms                                                   | 94.9 ms: 1.81x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 98.8 ms: 1.80x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.74x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.35x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 38.8 ms: 1.18x faster                                                        |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.1 ms: 2.52x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 24.4 ms: 1.55x faster                                                        |
| nbody          | 54.2 ms                                                  | 39.9 ms: 1.36x faster                                                        |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                    | 1.27x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                        |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                        |
| regex_dna      | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                        |
| regex_v8       | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                    | 1.08x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 73.2 us: 1.41x faster                                                        |
| xml_etree_iterparse  | 51.6 ms                                                  | 38.6 ms: 1.34x faster                                                        |
| pickle_pure_python   | 139 us                                                   | 114 us: 1.22x faster                                                         |
| xml_etree_generate   | 38.9 ms                                                  | 32.0 ms: 1.22x faster                                                        |
| tomli_loads          | 957 ms                                                   | 801 ms: 1.20x faster                                                         |
| xml_etree_process    | 26.7 ms                                                  | 22.4 ms: 1.19x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.70 ms: 1.15x faster                                                        |
| xml_etree_parse      | 67.9 ms                                                  | 62.6 ms: 1.09x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.20x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.93 ms: 1.11x slower                                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.43 ms: 1.13x slower                                                        |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 4.77 ms                                                  | 4.19 ms: 1.14x faster                                                        |
| genshi_text    | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                        |
| genshi_xml     | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                    | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.94 ms: 5.27x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.27x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 216 ms: 2.22x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.00x faster                                                         |
| richards                         | 22.4 ms                                                  | 11.4 ms: 1.97x faster                                                        |
| richards_super                   | 25.4 ms                                                  | 13.2 ms: 1.92x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 94.9 ms: 1.81x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 98.8 ms: 1.80x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.74x faster                                                         |
| mdp                              | 1.09 sec                                                 | 645 ms: 1.69x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                         |
| scimark_sor                      | 61.0 ms                                                  | 38.1 ms: 1.60x faster                                                        |
| deepcopy                         | 161 us                                                   | 103 us: 1.56x faster                                                         |
| float                            | 37.9 ms                                                  | 24.4 ms: 1.55x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                        |
| go                               | 70.0 ms                                                  | 46.0 ms: 1.52x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 33.8 ns: 1.51x faster                                                        |
| deltablue                        | 1.73 ms                                                  | 1.20 ms: 1.44x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 73.2 us: 1.41x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.40x faster                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 23.0 ms: 1.40x faster                                                        |
| pyflate                          | 216 ms                                                   | 154 ms: 1.40x faster                                                         |
| scimark_fft                      | 142 ms                                                   | 102 ms: 1.39x faster                                                         |
| logging_simple                   | 2.57 us                                                  | 1.87 us: 1.37x faster                                                        |
| raytrace                         | 145 ms                                                   | 106 ms: 1.37x faster                                                         |
| logging_format                   | 2.80 us                                                  | 2.05 us: 1.37x faster                                                        |
| nbody                            | 54.2 ms                                                  | 39.9 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.35x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                         |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.6 ms: 1.34x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.2 ms: 1.32x faster                                                        |
| chaos                            | 28.9 ms                                                  | 22.1 ms: 1.31x faster                                                        |
| k_core                           | 1.12 sec                                                 | 867 ms: 1.29x faster                                                         |
| comprehensions                   | 9.84 us                                                  | 7.70 us: 1.28x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 31.3 ms: 1.24x faster                                                        |
| scimark_lu                       | 51.3 ms                                                  | 41.5 ms: 1.24x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                         |
| pickle_pure_python               | 139 us                                                   | 114 us: 1.22x faster                                                         |
| xml_etree_generate               | 38.9 ms                                                  | 32.0 ms: 1.22x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 801 ms: 1.20x faster                                                         |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 22.4 ms: 1.19x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 46.0 ms: 1.19x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 38.8 ms: 1.18x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 280 ms: 1.17x faster                                                         |
| pprint_pformat                   | 665 ms                                                   | 568 ms: 1.17x faster                                                         |
| json_dumps                       | 4.26 ms                                                  | 3.70 ms: 1.15x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.19 ms: 1.14x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.5 ms: 1.12x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                        |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                         |
| fannkuch                         | 176 ms                                                   | 157 ms: 1.12x faster                                                         |
| typing_runtime_protocols         | 71.0 us                                                  | 63.6 us: 1.12x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 39.5 ms: 1.10x faster                                                        |
| thrift                           | 322 us                                                   | 295 us: 1.09x faster                                                         |
| xml_etree_parse                  | 67.9 ms                                                  | 62.6 ms: 1.09x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.07x faster                                                        |
| sphinx                           | 434 ms                                                   | 407 ms: 1.06x faster                                                         |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.95 ms: 1.06x faster                                                        |
| genshi_text                      | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 45.4 ms: 1.05x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                        |
| json                             | 1.93 ms                                                  | 1.87 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                         |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                        |
| generators                       | 21.9 ms                                                  | 21.4 ms: 1.02x faster                                                        |
| connected_components             | 201 ms                                                   | 197 ms: 1.02x faster                                                         |
| telco                            | 2.61 ms                                                  | 2.57 ms: 1.02x faster                                                        |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                         |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                         |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                       |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                         |
| regex_v8                         | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                                         |
| sympy_integrate                  | 8.02 ms                                                  | 8.34 ms: 1.04x slower                                                        |
| gc_traversal                     | 2.01 ms                                                  | 2.12 ms: 1.06x slower                                                        |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                         |
| sympy_sum                        | 57.6 ms                                                  | 63.5 ms: 1.10x slower                                                        |
| python_startup                   | 8.01 ms                                                  | 8.93 ms: 1.11x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                         |
| python_startup_no_site           | 5.71 ms                                                  | 6.43 ms: 1.13x slower                                                        |
| create_gc_cycles                 | 830 us                                                   | 937 us: 1.13x slower                                                         |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                         |
| sympy_str                        | 104 ms                                                   | 122 ms: 1.17x slower                                                         |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                        |
| many_optionals                   | 195 us                                                   | 259 us: 1.33x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.1 ms: 2.52x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.21x faster                                                                 |

Benchmark hidden because not significant (3): pylint, django_template, sqlite_synth
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, pycparser, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (2) of results/bm-20251230-3.15.0a3+-9f28e87-JIT/bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87.json: sqlglot_v2_normalize, sqlglot_v2_optimize

- Geometric mean (including insignificant results): 1.211x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.24x