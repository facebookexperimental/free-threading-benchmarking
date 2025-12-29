# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: jit_ft
- machine: darwin-arm64
- commit hash: 0678505
- commit date: 2025-12-28
- overall geometric mean: 1.165x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                 |
| html5lib       | 23.0 ms                                                  | 22.1 ms: 1.04x faster                                                |
| sphinx         | 434 ms                                                   | 431 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                    | 1.00x slower                                                         |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 237 ms: 2.03x faster                                                 |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                 |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                 |
| async_tree_eager_io_tg           | 446 ms                                                   | 247 ms: 1.81x faster                                                 |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                 |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                 |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                 |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                 |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                 |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                 |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.24x faster                                                |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                 |
| async_generators                 | 206 ms                                                   | 198 ms: 1.04x faster                                                 |
| async_tree_eager                 | 45.6 ms                                                  | 43.9 ms: 1.04x faster                                                |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                 |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                 |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.17x slower                                                 |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.0 ms: 2.89x slower                                                |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.0 ms: 1.65x faster                                                |
| nbody          | 54.2 ms                                                  | 44.2 ms: 1.23x faster                                                |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                    | 1.25x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.6 ms: 1.20x faster                                                |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                |
| regex_dna      | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                |
| Geometric mean | (ref)                                                    | 1.10x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.7 ms: 1.41x faster                                                |
| unpickle_pure_python | 103 us                                                   | 78.3 us: 1.31x faster                                                |
| pickle_pure_python   | 139 us                                                   | 116 us: 1.20x faster                                                 |
| xml_etree_generate   | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                |
| xml_etree_parse      | 67.9 ms                                                  | 58.8 ms: 1.16x faster                                                |
| json_dumps           | 4.26 ms                                                  | 3.72 ms: 1.14x faster                                                |
| tomli_loads          | 957 ms                                                   | 849 ms: 1.13x faster                                                 |
| xml_etree_process    | 26.7 ms                                                  | 23.8 ms: 1.12x faster                                                |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                |
| Geometric mean       | (ref)                                                    | 1.17x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                |
| python_startup_no_site | 5.71 ms                                                  | 7.24 ms: 1.27x slower                                                |
| Geometric mean         | (ref)                                                    | 1.27x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.74 ms: 1.01x faster                                                |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                |
| genshi_xml      | 21.8 ms                                                  | 28.3 ms: 1.30x slower                                                |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                         |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.88 ms: 5.36x faster                                                |
| gc_traversal                     | 2.01 ms                                                  | 812 us: 2.47x faster                                                 |
| async_tree_io_tg                 | 480 ms                                                   | 237 ms: 2.03x faster                                                 |
| async_tree_eager_io              | 496 ms                                                   | 249 ms: 1.99x faster                                                 |
| richards                         | 22.4 ms                                                  | 11.5 ms: 1.95x faster                                                |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                 |
| richards_super                   | 25.4 ms                                                  | 13.8 ms: 1.84x faster                                                |
| async_tree_eager_io_tg           | 446 ms                                                   | 247 ms: 1.81x faster                                                 |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                 |
| float                            | 37.9 ms                                                  | 23.0 ms: 1.65x faster                                                |
| mdp                              | 1.09 sec                                                 | 673 ms: 1.62x faster                                                 |
| logging_silent                   | 50.9 ns                                                  | 31.4 ns: 1.62x faster                                                |
| create_gc_cycles                 | 830 us                                                   | 514 us: 1.61x faster                                                 |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                 |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                 |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.57x faster                                                |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                 |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                 |
| pyflate                          | 216 ms                                                   | 148 ms: 1.46x faster                                                 |
| deltablue                        | 1.73 ms                                                  | 1.20 ms: 1.44x faster                                                |
| go                               | 70.0 ms                                                  | 49.0 ms: 1.43x faster                                                |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.7 ms: 1.41x faster                                                |
| scimark_sor                      | 61.0 ms                                                  | 44.3 ms: 1.38x faster                                                |
| comprehensions                   | 9.84 us                                                  | 7.36 us: 1.34x faster                                                |
| unpickle_pure_python             | 103 us                                                   | 78.3 us: 1.31x faster                                                |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                 |
| scimark_fft                      | 142 ms                                                   | 111 ms: 1.28x faster                                                 |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                |
| scimark_monte_carlo              | 32.2 ms                                                  | 25.6 ms: 1.26x faster                                                |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                 |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                 |
| spectral_norm                    | 54.4 ms                                                  | 43.9 ms: 1.24x faster                                                |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.24x faster                                                |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.81 sec: 1.24x faster                                               |
| nbody                            | 54.2 ms                                                  | 44.2 ms: 1.23x faster                                                |
| scimark_lu                       | 51.3 ms                                                  | 41.9 ms: 1.22x faster                                                |
| pickle_pure_python               | 139 us                                                   | 116 us: 1.20x faster                                                 |
| regex_compile                    | 54.6 ms                                                  | 45.6 ms: 1.20x faster                                                |
| sqlite_synth                     | 967 ns                                                   | 814 ns: 1.19x faster                                                 |
| chaos                            | 28.9 ms                                                  | 24.4 ms: 1.18x faster                                                |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                 |
| xml_etree_generate               | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                |
| k_core                           | 1.12 sec                                                 | 963 ms: 1.16x faster                                                 |
| pprint_safe_repr                 | 328 ms                                                   | 283 ms: 1.16x faster                                                 |
| xml_etree_parse                  | 67.9 ms                                                  | 58.8 ms: 1.16x faster                                                |
| fannkuch                         | 176 ms                                                   | 152 ms: 1.16x faster                                                 |
| json_dumps                       | 4.26 ms                                                  | 3.72 ms: 1.14x faster                                                |
| pprint_pformat                   | 665 ms                                                   | 581 ms: 1.14x faster                                                 |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                |
| tomli_loads                      | 957 ms                                                   | 849 ms: 1.13x faster                                                 |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                |
| xml_etree_process                | 26.7 ms                                                  | 23.8 ms: 1.12x faster                                                |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                |
| crypto_pyaes                     | 38.8 ms                                                  | 34.8 ms: 1.12x faster                                                |
| pycparser                        | 497 ms                                                   | 449 ms: 1.11x faster                                                 |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                |
| hexiom                           | 3.04 ms                                                  | 2.85 ms: 1.07x faster                                                |
| logging_format                   | 2.80 us                                                  | 2.65 us: 1.06x faster                                                |
| generators                       | 21.9 ms                                                  | 21.0 ms: 1.05x faster                                                |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                |
| async_generators                 | 206 ms                                                   | 198 ms: 1.04x faster                                                 |
| html5lib                         | 23.0 ms                                                  | 22.1 ms: 1.04x faster                                                |
| async_tree_eager                 | 45.6 ms                                                  | 43.9 ms: 1.04x faster                                                |
| regex_dna                        | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                 |
| typing_runtime_protocols         | 71.0 us                                                  | 70.1 us: 1.01x faster                                                |
| thrift                           | 322 us                                                   | 319 us: 1.01x faster                                                 |
| sphinx                           | 434 ms                                                   | 431 ms: 1.01x faster                                                 |
| mako                             | 4.77 ms                                                  | 4.74 ms: 1.01x faster                                                |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                 |
| nqueens                          | 43.5 ms                                                  | 43.3 ms: 1.00x faster                                                |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                 |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                 |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.18 ms: 1.05x slower                                                |
| sympy_integrate                  | 8.02 ms                                                  | 8.49 ms: 1.06x slower                                                |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                |
| meteor_contest                   | 47.7 ms                                                  | 51.6 ms: 1.08x slower                                                |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                |
| sympy_sum                        | 57.6 ms                                                  | 64.1 ms: 1.11x slower                                                |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                |
| sympy_str                        | 104 ms                                                   | 117 ms: 1.13x slower                                                 |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                 |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.15x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.17x slower                                                 |
| bench_mp_pool                    | 39.7 ms                                                  | 46.6 ms: 1.17x slower                                                |
| sympy_expand                     | 167 ms                                                   | 196 ms: 1.18x slower                                                 |
| connected_components             | 201 ms                                                   | 239 ms: 1.19x slower                                                 |
| python_startup                   | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                |
| python_startup_no_site           | 5.71 ms                                                  | 7.24 ms: 1.27x slower                                                |
| genshi_xml                       | 21.8 ms                                                  | 28.3 ms: 1.30x slower                                                |
| bench_thread_pool                | 419 us                                                   | 554 us: 1.32x slower                                                 |
| many_optionals                   | 195 us                                                   | 267 us: 1.37x slower                                                 |
| coverage                         | 26.9 ms                                                  | 39.7 ms: 1.48x slower                                                |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.0 ms: 2.89x slower                                                |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                         |

Benchmark hidden because not significant (3): json, docutils, pylint
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251228-3.15.0a3+-0678505-JIT,NOGIL/bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.165x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.38x