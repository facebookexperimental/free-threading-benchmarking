# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: loop_peeling
- machine: darwin-arm64
- commit hash: e650bf3
- commit date: 2026-01-03
- overall geometric mean: 1.168x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 107 ms: 1.04x faster                                                       |
| docutils       | 1.05 sec                                                       | 1000 ms: 1.05x faster                                                      |
| html5lib       | 23.1 ms                                                        | 19.7 ms: 1.17x faster                                                      |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                          | 1.08x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 216 ms: 2.41x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 217 ms: 1.87x faster                                                       |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.71x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 96.3 ms: 1.48x faster                                                      |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                       |
| async_tree_none_tg               | 133 ms                                                         | 96.1 ms: 1.38x faster                                                      |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 37.2 ms: 1.16x faster                                                      |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                      |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 213 ms: 1.05x faster                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                       |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.4 ms: 2.67x slower                                                      |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 22.2 ms: 1.42x faster                                                      |
| nbody          | 42.5 ms                                                        | 39.9 ms: 1.07x faster                                                      |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                          | 1.16x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.4 ms: 1.19x faster                                                      |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                      |
| regex_v8       | 10.7 ms                                                        | 9.83 ms: 1.09x faster                                                      |
| Geometric mean | (ref)                                                          | 1.10x faster                                                               |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 72.4 us: 1.37x faster                                                      |
| tomli_loads          | 1000 ms                                                        | 764 ms: 1.31x faster                                                       |
| json_dumps           | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                      |
| xml_etree_iterparse  | 46.1 ms                                                        | 36.4 ms: 1.27x faster                                                      |
| pickle_pure_python   | 130 us                                                         | 109 us: 1.19x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 21.9 ms: 1.16x faster                                                      |
| xml_etree_generate   | 35.8 ms                                                        | 31.0 ms: 1.15x faster                                                      |
| xml_etree_parse      | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                      |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                      |
| Geometric mean       | (ref)                                                          | 1.20x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.76 ms: 1.01x slower                                                      |
| python_startup_no_site | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                      |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|-----------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.87 ms: 1.14x faster                                                      |
| genshi_text     | 9.97 ms                                                        | 8.95 ms: 1.11x faster                                                      |
| genshi_xml      | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                      |
| django_template | 12.5 ms                                                        | 13.8 ms: 1.10x slower                                                      |
| Geometric mean  | (ref)                                                          | 1.04x faster                                                               |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 216 ms: 2.41x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.40x faster                                                       |
| richards                         | 22.1 ms                                                        | 9.52 ms: 2.32x faster                                                      |
| richards_super                   | 24.7 ms                                                        | 11.3 ms: 2.18x faster                                                      |
| async_tree_io_tg                 | 405 ms                                                         | 217 ms: 1.87x faster                                                       |
| mdp                              | 1.06 sec                                                       | 577 ms: 1.83x faster                                                       |
| async_tree_io                    | 386 ms                                                         | 225 ms: 1.71x faster                                                       |
| go                               | 72.6 ms                                                        | 42.8 ms: 1.69x faster                                                      |
| k_core                           | 1.46 sec                                                       | 864 ms: 1.69x faster                                                       |
| subparsers                       | 6.26 ms                                                        | 3.81 ms: 1.64x faster                                                      |
| pyflate                          | 222 ms                                                         | 142 ms: 1.57x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 42.2 ms: 1.52x faster                                                      |
| async_tree_none                  | 142 ms                                                         | 96.3 ms: 1.48x faster                                                      |
| deepcopy_memo                    | 16.5 us                                                        | 11.2 us: 1.47x faster                                                      |
| deepcopy                         | 145 us                                                         | 98.6 us: 1.47x faster                                                      |
| float                            | 31.4 ms                                                        | 22.2 ms: 1.42x faster                                                      |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                       |
| async_tree_none_tg               | 133 ms                                                         | 96.1 ms: 1.38x faster                                                      |
| unpickle_pure_python             | 99.5 us                                                        | 72.4 us: 1.37x faster                                                      |
| scimark_monte_carlo              | 29.9 ms                                                        | 21.9 ms: 1.36x faster                                                      |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.36x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 764 ms: 1.31x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.11 ms: 1.30x faster                                                      |
| json_dumps                       | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                      |
| deepcopy_reduce                  | 1.30 us                                                        | 1.00 us: 1.29x faster                                                      |
| pprint_safe_repr                 | 322 ms                                                         | 251 ms: 1.28x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 509 ms: 1.28x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.4 ms: 1.27x faster                                                      |
| scimark_fft                      | 124 ms                                                         | 97.8 ms: 1.26x faster                                                      |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                       |
| logging_silent                   | 40.6 ns                                                        | 33.7 ns: 1.20x faster                                                      |
| telco                            | 3.07 ms                                                        | 2.55 ms: 1.20x faster                                                      |
| pickle_pure_python               | 130 us                                                         | 109 us: 1.19x faster                                                       |
| scimark_lu                       | 42.8 ms                                                        | 35.9 ms: 1.19x faster                                                      |
| fannkuch                         | 179 ms                                                         | 150 ms: 1.19x faster                                                       |
| regex_compile                    | 47.9 ms                                                        | 40.4 ms: 1.19x faster                                                      |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.81 sec: 1.18x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 19.7 ms: 1.17x faster                                                      |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 37.2 ms: 1.16x faster                                                      |
| xml_etree_process                | 25.4 ms                                                        | 21.9 ms: 1.16x faster                                                      |
| xml_etree_generate               | 35.8 ms                                                        | 31.0 ms: 1.15x faster                                                      |
| mako                             | 4.41 ms                                                        | 3.87 ms: 1.14x faster                                                      |
| chaos                            | 24.3 ms                                                        | 21.6 ms: 1.12x faster                                                      |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                      |
| spectral_norm                    | 43.7 ms                                                        | 39.1 ms: 1.12x faster                                                      |
| genshi_text                      | 9.97 ms                                                        | 8.95 ms: 1.11x faster                                                      |
| comprehensions                   | 6.80 us                                                        | 6.13 us: 1.11x faster                                                      |
| crypto_pyaes                     | 33.6 ms                                                        | 30.4 ms: 1.11x faster                                                      |
| create_gc_cycles                 | 993 us                                                         | 901 us: 1.10x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.62 ms: 1.09x faster                                                      |
| regex_v8                         | 10.7 ms                                                        | 9.83 ms: 1.09x faster                                                      |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                       |
| pycparser                        | 470 ms                                                         | 436 ms: 1.08x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                      |
| json                             | 1.94 ms                                                        | 1.81 ms: 1.07x faster                                                      |
| nbody                            | 42.5 ms                                                        | 39.9 ms: 1.07x faster                                                      |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                      |
| meteor_contest                   | 47.9 ms                                                        | 45.3 ms: 1.06x faster                                                      |
| logging_simple                   | 2.24 us                                                        | 2.12 us: 1.06x faster                                                      |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 213 ms: 1.05x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                      |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1000 ms: 1.05x faster                                                      |
| connected_components             | 208 ms                                                         | 199 ms: 1.05x faster                                                       |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                       |
| 2to3                             | 112 ms                                                         | 107 ms: 1.04x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                      |
| typing_runtime_protocols         | 64.6 us                                                        | 62.3 us: 1.04x faster                                                      |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                      |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.03x faster                                                       |
| raytrace                         | 109 ms                                                         | 106 ms: 1.03x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                      |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                       |
| genshi_xml                       | 21.4 ms                                                        | 21.2 ms: 1.01x faster                                                      |
| sqlite_synth                     | 948 ns                                                         | 955 ns: 1.01x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 8.76 ms: 1.01x slower                                                      |
| sympy_integrate                  | 7.53 ms                                                        | 7.65 ms: 1.02x slower                                                      |
| nqueens                          | 37.2 ms                                                        | 38.4 ms: 1.03x slower                                                      |
| coverage                         | 31.2 ms                                                        | 32.4 ms: 1.04x slower                                                      |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                      |
| sympy_sum                        | 52.3 ms                                                        | 57.7 ms: 1.10x slower                                                      |
| django_template                  | 12.5 ms                                                        | 13.8 ms: 1.10x slower                                                      |
| sympy_expand                     | 159 ms                                                         | 176 ms: 1.11x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 237 ms: 1.14x slower                                                       |
| pylint                           | 106 ms                                                         | 122 ms: 1.16x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                       |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.17x slower                                                      |
| bench_mp_pool                    | 37.8 ms                                                        | 44.2 ms: 1.17x slower                                                      |
| many_optionals                   | 200 us                                                         | 244 us: 1.22x slower                                                       |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.4 ms: 2.67x slower                                                      |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                               |

Benchmark hidden because not significant (3): regex_dna, gc_traversal, scimark_sparse_mat_mult
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260103-3.15.0a3+-e650bf3-JIT/bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.168x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.21x