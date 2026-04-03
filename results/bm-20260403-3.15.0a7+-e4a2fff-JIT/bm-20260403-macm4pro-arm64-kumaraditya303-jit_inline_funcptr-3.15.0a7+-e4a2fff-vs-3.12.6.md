# Results vs. 3.12.6

- fork: kumaraditya303
- ref: jit_inline_funcptr
- machine: darwin-arm64
- commit hash: e4a2fff
- commit date: 2026-04-03
- overall geometric mean: 1.282x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                           |
| docutils       | 1.02 sec                                                 | 971 ms: 1.05x faster                                                           |
| html5lib       | 23.0 ms                                                  | 19.3 ms: 1.20x faster                                                          |
| sphinx         | 434 ms                                                   | 390 ms: 1.11x faster                                                           |
| Geometric mean | (ref)                                                    | 1.09x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.39x faster                                                           |
| async_tree_io_tg                 | 480 ms                                                   | 214 ms: 2.24x faster                                                           |
| async_tree_eager_io_tg           | 446 ms                                                   | 204 ms: 2.19x faster                                                           |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.18x faster                                                           |
| async_tree_none                  | 178 ms                                                   | 89.9 ms: 1.98x faster                                                          |
| async_tree_none_tg               | 172 ms                                                   | 89.3 ms: 1.93x faster                                                          |
| async_tree_memoization_tg        | 231 ms                                                   | 131 ms: 1.76x faster                                                           |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.74x faster                                                           |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                                           |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                           |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.27x faster                                                           |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                          |
| async_tree_eager                 | 45.6 ms                                                  | 36.6 ms: 1.24x faster                                                          |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                           |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                           |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                           |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.04x slower                                                           |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                           |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                          |
| Geometric mean                   | (ref)                                                    | 1.39x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.3 ms: 1.63x faster                                                          |
| nbody          | 54.2 ms                                                  | 34.0 ms: 1.60x faster                                                          |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                    | 1.37x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.9 ms: 1.37x faster                                                          |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.15x faster                                                          |
| regex_dna      | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                          |
| Geometric mean | (ref)                                                    | 1.13x faster                                                                   |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 633 ms: 1.51x faster                                                           |
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                          |
| xml_etree_process    | 26.7 ms                                                  | 21.1 ms: 1.26x faster                                                          |
| xml_etree_generate   | 38.9 ms                                                  | 31.8 ms: 1.22x faster                                                          |
| unpickle_pure_python | 103 us                                                   | 84.5 us: 1.22x faster                                                          |
| json_dumps           | 4.26 ms                                                  | 3.52 ms: 1.21x faster                                                          |
| pickle_pure_python   | 139 us                                                   | 125 us: 1.12x faster                                                           |
| xml_etree_parse      | 67.9 ms                                                  | 64.6 ms: 1.05x faster                                                          |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                          |
| Geometric mean       | (ref)                                                    | 1.21x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                          |
| python_startup_no_site | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                          |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 8.93 ms: 1.17x faster                                                          |
| mako            | 4.77 ms                                                  | 4.10 ms: 1.16x faster                                                          |
| django_template | 13.6 ms                                                  | 12.4 ms: 1.10x faster                                                          |
| genshi_xml      | 21.8 ms                                                  | 20.3 ms: 1.07x faster                                                          |
| Geometric mean  | (ref)                                                    | 1.13x faster                                                                   |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.54 ms: 5.87x faster                                                          |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.39x faster                                                           |
| richards                         | 22.4 ms                                                  | 9.74 ms: 2.30x faster                                                          |
| async_tree_io_tg                 | 480 ms                                                   | 214 ms: 2.24x faster                                                           |
| async_tree_eager_io_tg           | 446 ms                                                   | 204 ms: 2.19x faster                                                           |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.18x faster                                                           |
| richards_super                   | 25.4 ms                                                  | 11.6 ms: 2.18x faster                                                          |
| mdp                              | 1.09 sec                                                 | 520 ms: 2.10x faster                                                           |
| async_tree_none                  | 178 ms                                                   | 89.9 ms: 1.98x faster                                                          |
| async_tree_none_tg               | 172 ms                                                   | 89.3 ms: 1.93x faster                                                          |
| scimark_lu                       | 51.3 ms                                                  | 27.8 ms: 1.84x faster                                                          |
| scimark_sor                      | 61.0 ms                                                  | 34.7 ms: 1.76x faster                                                          |
| async_tree_memoization_tg        | 231 ms                                                   | 131 ms: 1.76x faster                                                           |
| async_tree_memoization           | 223 ms                                                   | 128 ms: 1.74x faster                                                           |
| deepcopy                         | 161 us                                                   | 94.5 us: 1.71x faster                                                          |
| comprehensions                   | 9.84 us                                                  | 5.87 us: 1.68x faster                                                          |
| deepcopy_memo                    | 18.3 us                                                  | 10.9 us: 1.67x faster                                                          |
| float                            | 37.9 ms                                                  | 23.3 ms: 1.63x faster                                                          |
| nbody                            | 54.2 ms                                                  | 34.0 ms: 1.60x faster                                                          |
| deltablue                        | 1.73 ms                                                  | 1.11 ms: 1.56x faster                                                          |
| logging_silent                   | 50.9 ns                                                  | 33.6 ns: 1.52x faster                                                          |
| tomli_loads                      | 957 ms                                                   | 633 ms: 1.51x faster                                                           |
| scimark_fft                      | 142 ms                                                   | 94.4 ms: 1.50x faster                                                          |
| go                               | 70.0 ms                                                  | 46.7 ms: 1.50x faster                                                          |
| spectral_norm                    | 54.4 ms                                                  | 36.5 ms: 1.49x faster                                                          |
| logging_format                   | 2.80 us                                                  | 1.90 us: 1.48x faster                                                          |
| logging_simple                   | 2.57 us                                                  | 1.74 us: 1.47x faster                                                          |
| pyflate                          | 216 ms                                                   | 148 ms: 1.46x faster                                                           |
| deepcopy_reduce                  | 1.46 us                                                  | 1.01 us: 1.44x faster                                                          |
| chaos                            | 28.9 ms                                                  | 20.5 ms: 1.41x faster                                                          |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.9 ms: 1.40x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                                           |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                           |
| regex_compile                    | 54.6 ms                                                  | 39.9 ms: 1.37x faster                                                          |
| nqueens                          | 43.5 ms                                                  | 31.9 ms: 1.36x faster                                                          |
| raytrace                         | 145 ms                                                   | 109 ms: 1.33x faster                                                           |
| pprint_pformat                   | 665 ms                                                   | 500 ms: 1.33x faster                                                           |
| pprint_safe_repr                 | 328 ms                                                   | 247 ms: 1.33x faster                                                           |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                          |
| k_core                           | 1.12 sec                                                 | 859 ms: 1.30x faster                                                           |
| async_tree_eager_memoization     | 132 ms                                                   | 104 ms: 1.27x faster                                                           |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                          |
| xml_etree_process                | 26.7 ms                                                  | 21.1 ms: 1.26x faster                                                          |
| hexiom                           | 3.04 ms                                                  | 2.41 ms: 1.26x faster                                                          |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.79 sec: 1.25x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 36.6 ms: 1.24x faster                                                          |
| crypto_pyaes                     | 38.8 ms                                                  | 31.6 ms: 1.23x faster                                                          |
| xml_etree_generate               | 38.9 ms                                                  | 31.8 ms: 1.22x faster                                                          |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.70 ms: 1.22x faster                                                          |
| unpickle_pure_python             | 103 us                                                   | 84.5 us: 1.22x faster                                                          |
| json_dumps                       | 4.26 ms                                                  | 3.52 ms: 1.21x faster                                                          |
| html5lib                         | 23.0 ms                                                  | 19.3 ms: 1.20x faster                                                          |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.19x faster                                                          |
| genshi_text                      | 10.5 ms                                                  | 8.93 ms: 1.17x faster                                                          |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                          |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                          |
| mako                             | 4.77 ms                                                  | 4.10 ms: 1.16x faster                                                          |
| fannkuch                         | 176 ms                                                   | 151 ms: 1.16x faster                                                           |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                           |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.15x faster                                                          |
| typing_runtime_protocols         | 71.0 us                                                  | 62.0 us: 1.14x faster                                                          |
| pycparser                        | 497 ms                                                   | 445 ms: 1.12x faster                                                           |
| pickle_pure_python               | 139 us                                                   | 125 us: 1.12x faster                                                           |
| sphinx                           | 434 ms                                                   | 390 ms: 1.11x faster                                                           |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                           |
| django_template                  | 13.6 ms                                                  | 12.4 ms: 1.10x faster                                                          |
| sympy_sum                        | 57.6 ms                                                  | 53.5 ms: 1.08x faster                                                          |
| genshi_xml                       | 21.8 ms                                                  | 20.3 ms: 1.07x faster                                                          |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                           |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                           |
| json                             | 1.93 ms                                                  | 1.82 ms: 1.06x faster                                                          |
| sympy_integrate                  | 8.02 ms                                                  | 7.56 ms: 1.06x faster                                                          |
| sympy_str                        | 104 ms                                                   | 98.5 ms: 1.06x faster                                                          |
| docutils                         | 1.02 sec                                                 | 971 ms: 1.05x faster                                                           |
| xml_etree_parse                  | 67.9 ms                                                  | 64.6 ms: 1.05x faster                                                          |
| meteor_contest                   | 47.7 ms                                                  | 45.5 ms: 1.05x faster                                                          |
| regex_dna                        | 99.6 ms                                                  | 95.4 ms: 1.04x faster                                                          |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                          |
| sqlite_synth                     | 967 ns                                                   | 939 ns: 1.03x faster                                                           |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                           |
| shortest_path                    | 219 ms                                                   | 214 ms: 1.02x faster                                                           |
| connected_components             | 201 ms                                                   | 196 ms: 1.02x faster                                                           |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                           |
| sympy_expand                     | 167 ms                                                   | 164 ms: 1.02x faster                                                           |
| telco                            | 2.61 ms                                                  | 2.57 ms: 1.01x faster                                                          |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                           |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                           |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                           |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.04x slower                                                           |
| python_startup                   | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                          |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                           |
| python_startup_no_site           | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                          |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                          |
| create_gc_cycles                 | 830 us                                                   | 943 us: 1.14x slower                                                           |
| many_optionals                   | 195 us                                                   | 225 us: 1.15x slower                                                           |
| gc_traversal                     | 2.01 ms                                                  | 2.38 ms: 1.19x slower                                                          |
| coverage                         | 26.9 ms                                                  | 34.2 ms: 1.27x slower                                                          |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.7 ms: 2.42x slower                                                          |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                                   |

Benchmark hidden because not significant (1): regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260403-3.15.0a7+-e4a2fff-JIT/bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.282x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.27x