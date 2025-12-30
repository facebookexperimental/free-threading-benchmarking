# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: d52a106
- commit date: 2025-12-30
- overall geometric mean: 1.261x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 109 ms: 1.05x faster                                                         |
| html5lib       | 23.0 ms                                                  | 19.8 ms: 1.16x faster                                                        |
| sphinx         | 434 ms                                                   | 397 ms: 1.09x faster                                                         |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 214 ms: 2.32x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 211 ms: 2.28x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 210 ms: 2.12x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 222 ms: 2.07x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 94.4 ms: 1.89x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 92.4 ms: 1.86x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 130 ms: 1.78x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.68x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 243 ms: 1.39x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 38.5 ms: 1.18x faster                                                        |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.04x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 24.4 ms: 1.56x faster                                                        |
| nbody          | 54.2 ms                                                  | 39.9 ms: 1.36x faster                                                        |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                    | 1.28x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.4 ms: 1.18x faster                                                        |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                        |
| regex_dna      | 99.6 ms                                                  | 95.3 ms: 1.05x faster                                                        |
| regex_v8       | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                    | 1.09x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 72.5 us: 1.42x faster                                                        |
| xml_etree_iterparse  | 51.6 ms                                                  | 37.2 ms: 1.39x faster                                                        |
| pickle_pure_python   | 139 us                                                   | 111 us: 1.25x faster                                                         |
| tomli_loads          | 957 ms                                                   | 786 ms: 1.22x faster                                                         |
| xml_etree_process    | 26.7 ms                                                  | 22.1 ms: 1.21x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 33.3 ms: 1.17x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.70 ms: 1.15x faster                                                        |
| xml_etree_parse      | 67.9 ms                                                  | 60.4 ms: 1.12x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.21x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.87 ms: 1.11x slower                                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.40 ms: 1.12x slower                                                        |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.17 ms: 1.14x faster                                                        |
| genshi_text     | 10.5 ms                                                  | 9.29 ms: 1.13x faster                                                        |
| django_template | 13.6 ms                                                  | 12.9 ms: 1.05x faster                                                        |
| genshi_xml      | 21.8 ms                                                  | 22.2 ms: 1.02x slower                                                        |
| Geometric mean  | (ref)                                                    | 1.07x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.85 ms: 5.39x faster                                                        |
| richards                         | 22.4 ms                                                  | 9.51 ms: 2.36x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 214 ms: 2.32x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 211 ms: 2.28x faster                                                         |
| richards_super                   | 25.4 ms                                                  | 11.5 ms: 2.22x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 210 ms: 2.12x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 222 ms: 2.07x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 94.4 ms: 1.89x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 92.4 ms: 1.86x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 130 ms: 1.78x faster                                                         |
| mdp                              | 1.09 sec                                                 | 641 ms: 1.70x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 133 ms: 1.68x faster                                                         |
| deltablue                        | 1.73 ms                                                  | 1.06 ms: 1.62x faster                                                        |
| deepcopy                         | 161 us                                                   | 101 us: 1.59x faster                                                         |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.57x faster                                                        |
| go                               | 70.0 ms                                                  | 44.9 ms: 1.56x faster                                                        |
| float                            | 37.9 ms                                                  | 24.4 ms: 1.56x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 40.5 ms: 1.50x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 34.3 ns: 1.48x faster                                                        |
| pyflate                          | 216 ms                                                   | 147 ms: 1.47x faster                                                         |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.6 ms: 1.42x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 72.5 us: 1.42x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 1.83 us: 1.41x faster                                                        |
| scimark_lu                       | 51.3 ms                                                  | 36.5 ms: 1.40x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.00 us: 1.40x faster                                                        |
| raytrace                         | 145 ms                                                   | 104 ms: 1.40x faster                                                         |
| scimark_fft                      | 142 ms                                                   | 101 ms: 1.40x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 243 ms: 1.39x faster                                                         |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.2 ms: 1.39x faster                                                        |
| nbody                            | 54.2 ms                                                  | 39.9 ms: 1.36x faster                                                        |
| chaos                            | 28.9 ms                                                  | 21.4 ms: 1.35x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.4 ms: 1.31x faster                                                        |
| k_core                           | 1.12 sec                                                 | 864 ms: 1.29x faster                                                         |
| comprehensions                   | 9.84 us                                                  | 7.69 us: 1.28x faster                                                        |
| pickle_pure_python               | 139 us                                                   | 111 us: 1.25x faster                                                         |
| pprint_pformat                   | 665 ms                                                   | 532 ms: 1.25x faster                                                         |
| crypto_pyaes                     | 38.8 ms                                                  | 31.3 ms: 1.24x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 265 ms: 1.24x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                         |
| tomli_loads                      | 957 ms                                                   | 786 ms: 1.22x faster                                                         |
| xml_etree_process                | 26.7 ms                                                  | 22.1 ms: 1.21x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 38.5 ms: 1.18x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 46.4 ms: 1.18x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 33.3 ms: 1.17x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 19.8 ms: 1.16x faster                                                        |
| fannkuch                         | 176 ms                                                   | 151 ms: 1.16x faster                                                         |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.70 ms: 1.15x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.17 ms: 1.14x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 62.7 us: 1.13x faster                                                        |
| genshi_text                      | 10.5 ms                                                  | 9.29 ms: 1.13x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 60.4 ms: 1.12x faster                                                        |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                         |
| thrift                           | 322 us                                                   | 288 us: 1.12x faster                                                         |
| hexiom                           | 3.04 ms                                                  | 2.73 ms: 1.11x faster                                                        |
| generators                       | 21.9 ms                                                  | 19.8 ms: 1.11x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 39.4 ms: 1.10x faster                                                        |
| sphinx                           | 434 ms                                                   | 397 ms: 1.09x faster                                                         |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                         |
| pycparser                        | 497 ms                                                   | 467 ms: 1.06x faster                                                         |
| meteor_contest                   | 47.7 ms                                                  | 45.0 ms: 1.06x faster                                                        |
| django_template                  | 13.6 ms                                                  | 12.9 ms: 1.05x faster                                                        |
| 2to3                             | 114 ms                                                   | 109 ms: 1.05x faster                                                         |
| regex_dna                        | 99.6 ms                                                  | 95.3 ms: 1.05x faster                                                        |
| json                             | 1.93 ms                                                  | 1.87 ms: 1.03x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                         |
| connected_components             | 201 ms                                                   | 198 ms: 1.01x faster                                                         |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                         |
| telco                            | 2.61 ms                                                  | 2.58 ms: 1.01x faster                                                        |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                         |
| regex_v8                         | 9.59 ms                                                  | 9.77 ms: 1.02x slower                                                        |
| genshi_xml                       | 21.8 ms                                                  | 22.2 ms: 1.02x slower                                                        |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.03x slower                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 118 ms: 1.04x slower                                                         |
| create_gc_cycles                 | 830 us                                                   | 915 us: 1.10x slower                                                         |
| python_startup                   | 8.01 ms                                                  | 8.87 ms: 1.11x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                         |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.40 ms: 1.12x slower                                                        |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                                        |
| many_optionals                   | 195 us                                                   | 249 us: 1.28x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                                 |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, docutils, gevent_hub, pylint, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, sympy_expand, sympy_integrate, sympy_str, sympy_sum, tornado_http
Ignored benchmarks (2) of results/bm-20251230-3.15.0a3+-d52a106-JIT/bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-d52a106.json: sqlglot_v2_optimize, sqlglot_v2_parse

- Geometric mean (including insignificant results): 1.261x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.25x