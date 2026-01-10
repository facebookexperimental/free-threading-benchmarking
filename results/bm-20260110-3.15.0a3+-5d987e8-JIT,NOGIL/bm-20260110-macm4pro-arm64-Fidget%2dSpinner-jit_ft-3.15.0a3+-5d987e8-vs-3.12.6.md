# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: jit_ft
- machine: darwin-arm64
- commit hash: 5d987e8
- commit date: 2026-01-10
- overall geometric mean: 1.188x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                 |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                               |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                |
| sphinx         | 434 ms                                                   | 417 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                    | 1.02x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.05x faster                                                 |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                 |
| async_tree_io                    | 459 ms                                                   | 239 ms: 1.92x faster                                                 |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.85x faster                                                 |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                 |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.63x faster                                                 |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                 |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                 |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                 |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                 |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                 |
| async_tree_eager                 | 45.6 ms                                                  | 41.4 ms: 1.10x faster                                                |
| async_generators                 | 206 ms                                                   | 200 ms: 1.03x faster                                                 |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                 |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                 |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                 |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.6 ms: 2.85x slower                                                |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 21.6 ms: 1.75x faster                                                |
| nbody          | 54.2 ms                                                  | 43.7 ms: 1.24x faster                                                |
| pidigits       | 161 ms                                                   | 165 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                    | 1.28x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.3 ms: 1.23x faster                                                |
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                |
| regex_v8       | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                |
| regex_dna      | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                |
| Geometric mean | (ref)                                                    | 1.11x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.8 ms: 1.40x faster                                                |
| unpickle_pure_python | 103 us                                                   | 76.8 us: 1.34x faster                                                |
| tomli_loads          | 957 ms                                                   | 739 ms: 1.30x faster                                                 |
| pickle_pure_python   | 139 us                                                   | 113 us: 1.23x faster                                                 |
| xml_etree_generate   | 38.9 ms                                                  | 32.3 ms: 1.20x faster                                                |
| xml_etree_parse      | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                |
| json_dumps           | 4.26 ms                                                  | 3.72 ms: 1.15x faster                                                |
| xml_etree_process    | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                |
| Geometric mean       | (ref)                                                    | 1.20x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.93 ms: 1.24x slower                                                |
| python_startup_no_site | 5.71 ms                                                  | 7.12 ms: 1.25x slower                                                |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                |
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                |
| genshi_xml      | 21.8 ms                                                  | 27.4 ms: 1.26x slower                                                |
| Geometric mean  | (ref)                                                    | 1.09x slower                                                         |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.78 ms: 5.49x faster                                                |
| gc_traversal                     | 2.01 ms                                                  | 819 us: 2.45x faster                                                 |
| richards                         | 22.4 ms                                                  | 10.4 ms: 2.16x faster                                                |
| async_tree_eager_io              | 496 ms                                                   | 241 ms: 2.05x faster                                                 |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                 |
| richards_super                   | 25.4 ms                                                  | 12.6 ms: 2.01x faster                                                |
| async_tree_io                    | 459 ms                                                   | 239 ms: 1.92x faster                                                 |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.85x faster                                                 |
| float                            | 37.9 ms                                                  | 21.6 ms: 1.75x faster                                                |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                 |
| mdp                              | 1.09 sec                                                 | 664 ms: 1.64x faster                                                 |
| deepcopy                         | 161 us                                                   | 98.6 us: 1.64x faster                                                |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.63x faster                                                 |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                 |
| create_gc_cycles                 | 830 us                                                   | 519 us: 1.60x faster                                                 |
| logging_silent                   | 50.9 ns                                                  | 32.6 ns: 1.56x faster                                                |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                 |
| go                               | 70.0 ms                                                  | 46.1 ms: 1.52x faster                                                |
| pyflate                          | 216 ms                                                   | 145 ms: 1.49x faster                                                 |
| deltablue                        | 1.73 ms                                                  | 1.17 ms: 1.47x faster                                                |
| comprehensions                   | 9.84 us                                                  | 6.92 us: 1.42x faster                                                |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.8 ms: 1.40x faster                                                |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.38x faster                                                |
| scimark_sor                      | 61.0 ms                                                  | 44.5 ms: 1.37x faster                                                |
| unpickle_pure_python             | 103 us                                                   | 76.8 us: 1.34x faster                                                |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                 |
| scimark_fft                      | 142 ms                                                   | 109 ms: 1.30x faster                                                 |
| tomli_loads                      | 957 ms                                                   | 739 ms: 1.30x faster                                                 |
| scimark_monte_carlo              | 32.2 ms                                                  | 25.0 ms: 1.29x faster                                                |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                 |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.78 sec: 1.26x faster                                               |
| scimark_lu                       | 51.3 ms                                                  | 40.8 ms: 1.26x faster                                                |
| nbody                            | 54.2 ms                                                  | 43.7 ms: 1.24x faster                                                |
| spectral_norm                    | 54.4 ms                                                  | 43.8 ms: 1.24x faster                                                |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                 |
| pickle_pure_python               | 139 us                                                   | 113 us: 1.23x faster                                                 |
| regex_compile                    | 54.6 ms                                                  | 44.3 ms: 1.23x faster                                                |
| fannkuch                         | 176 ms                                                   | 143 ms: 1.23x faster                                                 |
| chaos                            | 28.9 ms                                                  | 23.9 ms: 1.21x faster                                                |
| pprint_safe_repr                 | 328 ms                                                   | 271 ms: 1.21x faster                                                 |
| xml_etree_generate               | 38.9 ms                                                  | 32.3 ms: 1.20x faster                                                |
| pprint_pformat                   | 665 ms                                                   | 556 ms: 1.19x faster                                                 |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                 |
| sqlite_synth                     | 967 ns                                                   | 817 ns: 1.18x faster                                                 |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                 |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                |
| xml_etree_parse                  | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                |
| json_dumps                       | 4.26 ms                                                  | 3.72 ms: 1.15x faster                                                |
| pycparser                        | 497 ms                                                   | 436 ms: 1.14x faster                                                 |
| xml_etree_process                | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                |
| crypto_pyaes                     | 38.8 ms                                                  | 34.4 ms: 1.13x faster                                                |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                |
| logging_simple                   | 2.57 us                                                  | 2.33 us: 1.10x faster                                                |
| async_tree_eager                 | 45.6 ms                                                  | 41.4 ms: 1.10x faster                                                |
| hexiom                           | 3.04 ms                                                  | 2.78 ms: 1.09x faster                                                |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.09x faster                                                |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.09x faster                                                |
| generators                       | 21.9 ms                                                  | 21.0 ms: 1.05x faster                                                |
| regex_v8                         | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                |
| mako                             | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                |
| sphinx                           | 434 ms                                                   | 417 ms: 1.04x faster                                                 |
| regex_dna                        | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                |
| async_generators                 | 206 ms                                                   | 200 ms: 1.03x faster                                                 |
| typing_runtime_protocols         | 71.0 us                                                  | 68.8 us: 1.03x faster                                                |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                 |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                               |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                 |
| sympy_integrate                  | 8.02 ms                                                  | 8.19 ms: 1.02x slower                                                |
| pidigits                         | 161 ms                                                   | 165 ms: 1.03x slower                                                 |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                |
| thrift                           | 322 us                                                   | 335 us: 1.04x slower                                                 |
| meteor_contest                   | 47.7 ms                                                  | 49.8 ms: 1.04x slower                                                |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                 |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                |
| telco                            | 2.61 ms                                                  | 2.81 ms: 1.08x slower                                                |
| sympy_sum                        | 57.6 ms                                                  | 62.2 ms: 1.08x slower                                                |
| sympy_str                        | 104 ms                                                   | 114 ms: 1.10x slower                                                 |
| shortest_path                    | 219 ms                                                   | 245 ms: 1.12x slower                                                 |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                 |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                 |
| connected_components             | 201 ms                                                   | 233 ms: 1.16x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                 |
| bench_mp_pool                    | 39.7 ms                                                  | 47.2 ms: 1.19x slower                                                |
| python_startup                   | 8.01 ms                                                  | 9.93 ms: 1.24x slower                                                |
| python_startup_no_site           | 5.71 ms                                                  | 7.12 ms: 1.25x slower                                                |
| genshi_xml                       | 21.8 ms                                                  | 27.4 ms: 1.26x slower                                                |
| bench_thread_pool                | 419 us                                                   | 564 us: 1.35x slower                                                 |
| many_optionals                   | 195 us                                                   | 267 us: 1.37x slower                                                 |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.6 ms: 2.85x slower                                                |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                         |

Benchmark hidden because not significant (3): pylint, json, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260110-3.15.0a3+-5d987e8-JIT,NOGIL/bm-20260110-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-5d987e8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.188x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.39x