# Results vs. 3.12.6

- fork: kumaraditya303
- ref: interp_tls
- machine: darwin-arm64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.071x faster
- HPT reliability: 92.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                   |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                 |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                  |
| sphinx         | 434 ms                                                   | 418 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                    | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 201 ms: 2.38x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 209 ms: 2.38x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 198 ms: 2.25x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 213 ms: 2.15x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 88.3 ms: 1.95x faster                                                  |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.84x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                  |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                   |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                  |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.5 ms: 2.47x slower                                                  |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                           |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                  |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                   |
| nbody          | 54.2 ms                                                  | 61.0 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                    | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                  |
| regex_dna      | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                                  |
| regex_v8       | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                  |
| regex_compile  | 54.6 ms                                                  | 53.9 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                    | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                  |
| xml_etree_parse      | 67.9 ms                                                  | 58.7 ms: 1.16x faster                                                  |
| json_dumps           | 4.26 ms                                                  | 4.07 ms: 1.05x faster                                                  |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                  |
| tomli_loads          | 957 ms                                                   | 977 ms: 1.02x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                  |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                  |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.74 ms: 1.21x slower                                                  |
| python_startup_no_site | 5.71 ms                                                  | 7.08 ms: 1.24x slower                                                  |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 12.0 ms: 1.14x slower                                                  |
| genshi_xml      | 21.8 ms                                                  | 25.2 ms: 1.16x slower                                                  |
| mako            | 4.77 ms                                                  | 5.81 ms: 1.22x slower                                                  |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                  |
| Geometric mean  | (ref)                                                    | 1.19x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 763 us: 2.63x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 201 ms: 2.38x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 209 ms: 2.38x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 198 ms: 2.25x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 213 ms: 2.15x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 88.3 ms: 1.95x faster                                                  |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.84x faster                                                   |
| mdp                              | 1.09 sec                                                 | 619 ms: 1.76x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 474 us: 1.75x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.6 us: 1.35x faster                                                  |
| deepcopy                         | 161 us                                                   | 120 us: 1.34x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                  |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                  |
| float                            | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                  |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 825 ns: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                  |
| xml_etree_parse                  | 67.9 ms                                                  | 58.7 ms: 1.16x faster                                                  |
| comprehensions                   | 9.84 us                                                  | 8.51 us: 1.16x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                  |
| deepcopy_reduce                  | 1.46 us                                                  | 1.29 us: 1.13x faster                                                  |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                  |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                   |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                   |
| go                               | 70.0 ms                                                  | 63.2 ms: 1.11x faster                                                  |
| logging_silent                   | 50.9 ns                                                  | 46.0 ns: 1.11x faster                                                  |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.03 sec: 1.10x faster                                                 |
| dulwich_log                      | 21.3 ms                                                  | 19.3 ms: 1.10x faster                                                  |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 134 ms: 1.08x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 56.6 ms: 1.08x faster                                                  |
| pyflate                          | 216 ms                                                   | 201 ms: 1.08x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 19.3 ms: 1.07x faster                                                  |
| spectral_norm                    | 54.4 ms                                                  | 51.1 ms: 1.06x faster                                                  |
| regex_dna                        | 99.6 ms                                                  | 94.6 ms: 1.05x faster                                                  |
| scimark_fft                      | 142 ms                                                   | 135 ms: 1.05x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.07 ms: 1.05x faster                                                  |
| pycparser                        | 497 ms                                                   | 477 ms: 1.04x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                  |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                  |
| sphinx                           | 434 ms                                                   | 418 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.9 ms: 1.01x faster                                                  |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                 |
| logging_simple                   | 2.57 us                                                  | 2.55 us: 1.01x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 530 ms: 1.00x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.09 ms: 1.01x slower                                                  |
| logging_format                   | 2.80 us                                                  | 2.83 us: 1.01x slower                                                  |
| tomli_loads                      | 957 ms                                                   | 977 ms: 1.02x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                  |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 44.6 ms: 1.03x slower                                                  |
| chaos                            | 28.9 ms                                                  | 29.9 ms: 1.03x slower                                                  |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.04x slower                                                  |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 75.1 us: 1.06x slower                                                  |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                  |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.2 ms: 1.06x slower                                                  |
| fannkuch                         | 176 ms                                                   | 187 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.3 ms: 1.06x slower                                                  |
| thrift                           | 322 us                                                   | 344 us: 1.07x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.25 ms: 1.07x slower                                                  |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.7 ms: 1.08x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                  |
| sympy_str                        | 104 ms                                                   | 113 ms: 1.08x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.5 ms: 1.08x slower                                                  |
| pprint_safe_repr                 | 328 ms                                                   | 356 ms: 1.09x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.25 ms: 1.09x slower                                                  |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                  |
| pprint_pformat                   | 665 ms                                                   | 725 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                   |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.11x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 43.0 ms: 1.11x slower                                                  |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 56.9 ms: 1.11x slower                                                  |
| nbody                            | 54.2 ms                                                  | 61.0 ms: 1.12x slower                                                  |
| genshi_text                      | 10.5 ms                                                  | 12.0 ms: 1.14x slower                                                  |
| sympy_expand                     | 167 ms                                                   | 193 ms: 1.15x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 25.2 ms: 1.16x slower                                                  |
| telco                            | 2.61 ms                                                  | 3.08 ms: 1.18x slower                                                  |
| meteor_contest                   | 47.7 ms                                                  | 56.9 ms: 1.19x slower                                                  |
| python_startup                   | 8.01 ms                                                  | 9.74 ms: 1.21x slower                                                  |
| mako                             | 4.77 ms                                                  | 5.81 ms: 1.22x slower                                                  |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                  |
| python_startup_no_site           | 5.71 ms                                                  | 7.08 ms: 1.24x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 548 us: 1.31x slower                                                   |
| coverage                         | 26.9 ms                                                  | 40.9 ms: 1.52x slower                                                  |
| many_optionals                   | 195 us                                                   | 393 us: 2.01x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.5 ms: 2.47x slower                                                  |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                           |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251024-3.15.0a1+-04318d0-NOGIL/bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 92.77% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x