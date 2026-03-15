# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 2e9b980
- commit date: 2026-03-15
- overall geometric mean: 1.290x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.28x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                         |
| docutils       | 1.02 sec                                                 | 962 ms: 1.06x faster                                                         |
| html5lib       | 23.0 ms                                                  | 18.8 ms: 1.23x faster                                                        |
| sphinx         | 434 ms                                                   | 386 ms: 1.12x faster                                                         |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.39x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 207 ms: 2.31x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 203 ms: 2.19x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 88.2 ms: 2.02x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 89.4 ms: 1.93x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 127 ms: 1.82x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 126 ms: 1.77x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 9.35 ms: 1.45x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 237 ms: 1.41x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 102 ms: 1.29x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 36.5 ms: 1.25x faster                                                        |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 212 ms: 1.09x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 115 ms: 1.02x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.7 ms: 2.39x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.42x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.6 ms: 1.60x faster                                                        |
| nbody          | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                        |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                    | 1.30x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.5 ms: 1.38x faster                                                        |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                        |
| regex_dna      | 99.6 ms                                                  | 93.2 ms: 1.07x faster                                                        |
| regex_v8       | 9.59 ms                                                  | 9.53 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                    | 1.14x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 628 ms: 1.53x faster                                                         |
| xml_etree_iterparse  | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                        |
| xml_etree_process    | 26.7 ms                                                  | 21.5 ms: 1.25x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.51 ms: 1.21x faster                                                        |
| unpickle_pure_python | 103 us                                                   | 84.9 us: 1.21x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 32.1 ms: 1.21x faster                                                        |
| pickle_pure_python   | 139 us                                                   | 126 us: 1.11x faster                                                         |
| xml_etree_parse      | 67.9 ms                                                  | 64.2 ms: 1.06x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.03x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.21x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.68 ms: 1.08x slower                                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                        |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.00 ms: 1.19x faster                                                        |
| django_template | 13.6 ms                                                  | 12.4 ms: 1.10x faster                                                        |
| Geometric mean  | (ref)                                                    | 1.15x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.50 ms: 5.94x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.39x faster                                                         |
| richards                         | 22.4 ms                                                  | 9.63 ms: 2.33x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 207 ms: 2.31x faster                                                         |
| richards_super                   | 25.4 ms                                                  | 11.4 ms: 2.23x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 207 ms: 2.22x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 203 ms: 2.19x faster                                                         |
| mdp                              | 1.09 sec                                                 | 523 ms: 2.09x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 88.2 ms: 2.02x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 89.4 ms: 1.93x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 10.0 us: 1.83x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 127 ms: 1.82x faster                                                         |
| scimark_lu                       | 51.3 ms                                                  | 28.9 ms: 1.77x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 126 ms: 1.77x faster                                                         |
| deepcopy                         | 161 us                                                   | 94.3 us: 1.71x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 5.90 us: 1.67x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 36.8 ms: 1.66x faster                                                        |
| float                            | 37.9 ms                                                  | 23.6 ms: 1.60x faster                                                        |
| deltablue                        | 1.73 ms                                                  | 1.11 ms: 1.55x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 628 ms: 1.53x faster                                                         |
| go                               | 70.0 ms                                                  | 45.9 ms: 1.53x faster                                                        |
| pyflate                          | 216 ms                                                   | 145 ms: 1.49x faster                                                         |
| logging_format                   | 2.80 us                                                  | 1.91 us: 1.47x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 1.76 us: 1.46x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.00 us: 1.46x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.35 ms: 1.45x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 35.1 ns: 1.45x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 38.1 ms: 1.43x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 238 ms: 1.42x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 237 ms: 1.41x faster                                                         |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.9 ms: 1.41x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 101 ms: 1.40x faster                                                         |
| regex_compile                    | 54.6 ms                                                  | 39.5 ms: 1.38x faster                                                        |
| chaos                            | 28.9 ms                                                  | 21.0 ms: 1.38x faster                                                        |
| nbody                            | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 32.3 ms: 1.35x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 510 ms: 1.30x faster                                                         |
| raytrace                         | 145 ms                                                   | 111 ms: 1.30x faster                                                         |
| k_core                           | 1.12 sec                                                 | 858 ms: 1.30x faster                                                         |
| pprint_safe_repr                 | 328 ms                                                   | 252 ms: 1.30x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 102 ms: 1.29x faster                                                         |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.78 sec: 1.26x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.42 ms: 1.25x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 36.5 ms: 1.25x faster                                                        |
| xml_etree_process                | 26.7 ms                                                  | 21.5 ms: 1.25x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 31.6 ms: 1.23x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 18.8 ms: 1.23x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.51 ms: 1.21x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 84.9 us: 1.21x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 32.1 ms: 1.21x faster                                                        |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.00 ms: 1.19x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.19x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                        |
| fannkuch                         | 176 ms                                                   | 150 ms: 1.17x faster                                                         |
| typing_runtime_protocols         | 71.0 us                                                  | 62.2 us: 1.14x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                        |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                         |
| sphinx                           | 434 ms                                                   | 386 ms: 1.12x faster                                                         |
| pycparser                        | 497 ms                                                   | 444 ms: 1.12x faster                                                         |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.86 ms: 1.12x faster                                                        |
| pickle_pure_python               | 139 us                                                   | 126 us: 1.11x faster                                                         |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                         |
| django_template                  | 13.6 ms                                                  | 12.4 ms: 1.10x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 212 ms: 1.09x faster                                                         |
| regex_dna                        | 99.6 ms                                                  | 93.2 ms: 1.07x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 44.8 ms: 1.07x faster                                                        |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                         |
| sympy_sum                        | 57.6 ms                                                  | 54.2 ms: 1.06x faster                                                        |
| docutils                         | 1.02 sec                                                 | 962 ms: 1.06x faster                                                         |
| xml_etree_parse                  | 67.9 ms                                                  | 64.2 ms: 1.06x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.60 ms: 1.06x faster                                                        |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                        |
| sympy_str                        | 104 ms                                                   | 99.5 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                         |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                         |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.03x faster                                                        |
| connected_components             | 201 ms                                                   | 196 ms: 1.02x faster                                                         |
| sqlite_synth                     | 967 ns                                                   | 946 ns: 1.02x faster                                                         |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.02x faster                                                         |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                         |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                         |
| gc_traversal                     | 2.01 ms                                                  | 1.99 ms: 1.01x faster                                                        |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                         |
| regex_v8                         | 9.59 ms                                                  | 9.53 ms: 1.01x faster                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 115 ms: 1.02x slower                                                         |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.03x slower                                                         |
| create_gc_cycles                 | 830 us                                                   | 881 us: 1.06x slower                                                         |
| python_startup                   | 8.01 ms                                                  | 8.68 ms: 1.08x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                         |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                        |
| many_optionals                   | 195 us                                                   | 224 us: 1.15x slower                                                         |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.7 ms: 2.39x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                                 |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260315-3.15.0a7+-2e9b980-JIT/bm-20260315-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.290x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.28x