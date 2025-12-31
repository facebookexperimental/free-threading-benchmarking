# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 564677c
- commit date: 2025-12-31
- overall geometric mean: 1.247x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 109 ms: 1.04x faster                                                         |
| html5lib       | 23.0 ms                                                  | 19.5 ms: 1.18x faster                                                        |
| sphinx         | 434 ms                                                   | 400 ms: 1.08x faster                                                         |
| Geometric mean | (ref)                                                    | 1.07x faster                                                                 |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 211 ms: 2.35x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 209 ms: 2.29x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 210 ms: 2.12x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 94.5 ms: 1.89x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 92.7 ms: 1.86x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 130 ms: 1.77x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.68x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.38x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 9.93 ms: 1.37x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 38.2 ms: 1.19x faster                                                        |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.04x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.3 ms: 2.40x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 24.2 ms: 1.57x faster                                                        |
| nbody          | 54.2 ms                                                  | 40.0 ms: 1.36x faster                                                        |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                    | 1.29x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.8 ms: 1.37x faster                                                        |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                        |
| regex_dna      | 99.6 ms                                                  | 94.4 ms: 1.05x faster                                                        |
| regex_v8       | 9.59 ms                                                  | 9.47 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                    | 1.14x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 72.6 us: 1.42x faster                                                        |
| xml_etree_iterparse  | 51.6 ms                                                  | 37.0 ms: 1.39x faster                                                        |
| pickle_pure_python   | 139 us                                                   | 112 us: 1.24x faster                                                         |
| tomli_loads          | 957 ms                                                   | 784 ms: 1.22x faster                                                         |
| xml_etree_process    | 26.7 ms                                                  | 22.3 ms: 1.20x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.64 ms: 1.17x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                        |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.04x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.22x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                        |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.11 ms: 1.16x faster                                                        |
| genshi_text     | 10.5 ms                                                  | 9.14 ms: 1.15x faster                                                        |
| django_template | 13.6 ms                                                  | 13.0 ms: 1.05x faster                                                        |
| genshi_xml      | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                        |
| Geometric mean  | (ref)                                                    | 1.09x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.86 ms: 5.38x faster                                                        |
| richards                         | 22.4 ms                                                  | 9.43 ms: 2.38x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 211 ms: 2.35x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 209 ms: 2.29x faster                                                         |
| richards_super                   | 25.4 ms                                                  | 11.4 ms: 2.23x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 210 ms: 2.12x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 94.5 ms: 1.89x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 92.7 ms: 1.86x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 130 ms: 1.77x faster                                                         |
| mdp                              | 1.09 sec                                                 | 648 ms: 1.68x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.68x faster                                                         |
| deepcopy                         | 161 us                                                   | 98.4 us: 1.64x faster                                                        |
| deltablue                        | 1.73 ms                                                  | 1.08 ms: 1.60x faster                                                        |
| go                               | 70.0 ms                                                  | 44.2 ms: 1.58x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.21 us: 1.58x faster                                                        |
| float                            | 37.9 ms                                                  | 24.2 ms: 1.57x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 33.6 ns: 1.52x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 40.5 ms: 1.51x faster                                                        |
| pyflate                          | 216 ms                                                   | 144 ms: 1.50x faster                                                         |
| deepcopy_reduce                  | 1.46 us                                                  | 1.01 us: 1.45x faster                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.3 ms: 1.44x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 72.6 us: 1.42x faster                                                        |
| raytrace                         | 145 ms                                                   | 102 ms: 1.42x faster                                                         |
| scimark_fft                      | 142 ms                                                   | 101 ms: 1.40x faster                                                         |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.0 ms: 1.39x faster                                                        |
| chaos                            | 28.9 ms                                                  | 20.8 ms: 1.39x faster                                                        |
| scimark_lu                       | 51.3 ms                                                  | 37.0 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 246 ms: 1.38x faster                                                         |
| regex_compile                    | 54.6 ms                                                  | 39.8 ms: 1.37x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.93 ms: 1.37x faster                                                        |
| nbody                            | 54.2 ms                                                  | 40.0 ms: 1.36x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 40.6 ms: 1.34x faster                                                        |
| k_core                           | 1.12 sec                                                 | 864 ms: 1.29x faster                                                         |
| logging_simple                   | 2.57 us                                                  | 2.01 us: 1.28x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 30.9 ms: 1.26x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.23 us: 1.26x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 529 ms: 1.26x faster                                                         |
| pprint_safe_repr                 | 328 ms                                                   | 263 ms: 1.25x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                         |
| pickle_pure_python               | 139 us                                                   | 112 us: 1.24x faster                                                         |
| tomli_loads                      | 957 ms                                                   | 784 ms: 1.22x faster                                                         |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.86 sec: 1.20x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 22.3 ms: 1.20x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 38.2 ms: 1.19x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 19.5 ms: 1.18x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.64 ms: 1.17x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.11 ms: 1.16x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                        |
| fannkuch                         | 176 ms                                                   | 152 ms: 1.15x faster                                                         |
| genshi_text                      | 10.5 ms                                                  | 9.14 ms: 1.15x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                        |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                         |
| typing_runtime_protocols         | 71.0 us                                                  | 62.8 us: 1.13x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.72 ms: 1.12x faster                                                        |
| generators                       | 21.9 ms                                                  | 19.7 ms: 1.11x faster                                                        |
| thrift                           | 322 us                                                   | 291 us: 1.11x faster                                                         |
| nqueens                          | 43.5 ms                                                  | 39.4 ms: 1.10x faster                                                        |
| pycparser                        | 497 ms                                                   | 458 ms: 1.09x faster                                                         |
| sphinx                           | 434 ms                                                   | 400 ms: 1.08x faster                                                         |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.07x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                         |
| json                             | 1.93 ms                                                  | 1.82 ms: 1.06x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 45.2 ms: 1.05x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 94.4 ms: 1.05x faster                                                        |
| django_template                  | 13.6 ms                                                  | 13.0 ms: 1.05x faster                                                        |
| 2to3                             | 114 ms                                                   | 109 ms: 1.04x faster                                                         |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.04x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                         |
| genshi_xml                       | 21.8 ms                                                  | 21.3 ms: 1.02x faster                                                        |
| connected_components             | 201 ms                                                   | 197 ms: 1.02x faster                                                         |
| telco                            | 2.61 ms                                                  | 2.57 ms: 1.02x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.47 ms: 1.01x faster                                                        |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                         |
| sqlite_synth                     | 967 ns                                                   | 956 ns: 1.01x faster                                                         |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                         |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 8.22 ms: 1.02x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.04x slower                                                         |
| sympy_sum                        | 57.6 ms                                                  | 61.0 ms: 1.06x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 179 ms: 1.07x slower                                                         |
| sympy_str                        | 104 ms                                                   | 114 ms: 1.09x slower                                                         |
| python_startup                   | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                        |
| create_gc_cycles                 | 830 us                                                   | 912 us: 1.10x slower                                                         |
| python_startup_no_site           | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 44.1 ms: 1.11x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                         |
| coverage                         | 26.9 ms                                                  | 32.4 ms: 1.20x slower                                                        |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.3 ms: 2.40x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                                 |

Benchmark hidden because not significant (2): pylint, docutils
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251231-3.15.0a3+-564677c-JIT/bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.247x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.15x
- 95% likely to have a speedup of 1.14x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: 1.24x