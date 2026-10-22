# Results vs. 3.12.6

- fork: python
- ref: ab5187ce84a1e6641b5a
- machine: darwin-arm64
- commit hash: ab5187c
- commit date: 2026-10-22
- overall geometric mean: 1.073x faster
- HPT reliability: 95.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 126 ms: 1.11x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                      |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                       |
| sphinx         | 434 ms                                                   | 440 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                    | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 290 ms: 1.71x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 289 ms: 1.66x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 287 ms: 1.55x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 298 ms: 1.54x faster                                                        |
| async_generators                 | 206 ms                                                   | 157 ms: 1.31x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 178 ms: 1.30x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 140 ms: 1.28x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 137 ms: 1.26x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 183 ms: 1.21x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 289 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 296 ms: 1.13x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.7 ms: 1.07x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 124 ms: 1.06x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 48.4 ms: 1.06x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 270 ms: 1.27x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 161 ms: 1.43x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 111 ms: 3.47x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                                |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.5 ms: 1.16x faster                                                       |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                        |
| nbody          | 54.2 ms                                                  | 58.9 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                    | 1.03x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 89.4 ms: 1.11x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.07 ms: 1.06x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 63.2 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                    | 1.06x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 57.9 ms: 1.17x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                       |
| tomli_loads          | 957 ms                                                   | 881 ms: 1.09x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 38.7 ms: 1.00x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.4 ms: 1.10x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 159 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.28 ms: 1.16x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 7.22 ms: 1.27x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                       |
| django_template | 13.6 ms                                                  | 17.2 ms: 1.26x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.23x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.28 ms: 4.85x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 758 us: 2.65x faster                                                        |
| pylint                           | 128 ms                                                   | 52.4 ms: 2.45x faster                                                       |
| mdp                              | 1.09 sec                                                 | 579 ms: 1.89x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 456 us: 1.82x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 290 ms: 1.71x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 289 ms: 1.66x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 287 ms: 1.55x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 298 ms: 1.54x faster                                                        |
| deepcopy                         | 161 us                                                   | 107 us: 1.51x faster                                                        |
| async_generators                 | 206 ms                                                   | 157 ms: 1.31x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 178 ms: 1.30x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 140 ms: 1.28x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.26x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 137 ms: 1.26x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 57.2 us: 1.24x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 790 ns: 1.22x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 183 ms: 1.21x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 8.25 us: 1.19x faster                                                       |
| go                               | 70.0 ms                                                  | 59.6 ms: 1.17x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 57.9 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 289 ms: 1.17x faster                                                        |
| float                            | 37.9 ms                                                  | 32.5 ms: 1.16x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.16x faster                                                      |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 296 ms: 1.13x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 89.4 ms: 1.11x faster                                                       |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.2 ms: 1.11x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 881 ms: 1.09x faster                                                        |
| raytrace                         | 145 ms                                                   | 134 ms: 1.08x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.7 ms: 1.07x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.42 us: 1.06x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 57.6 ms: 1.06x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 124 ms: 1.06x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.07 ms: 1.06x faster                                                       |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.66 us: 1.05x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 48.5 ns: 1.05x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                       |
| chaos                            | 28.9 ms                                                  | 28.3 ms: 1.02x faster                                                       |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 42.9 ms: 1.01x faster                                                       |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 38.7 ms: 1.00x faster                                                       |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                      |
| sphinx                           | 434 ms                                                   | 440 ms: 1.01x slower                                                        |
| deltablue                        | 1.73 ms                                                  | 1.77 ms: 1.02x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.11 ms: 1.02x slower                                                       |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                        |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 40.5 ms: 1.04x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.04x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.7 ms: 1.05x slower                                                       |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                        |
| sympy_sum                        | 57.6 ms                                                  | 60.4 ms: 1.05x slower                                                       |
| generators                       | 21.9 ms                                                  | 23.1 ms: 1.05x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 42.2 ms: 1.06x slower                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 48.4 ms: 1.06x slower                                                       |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.06x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 351 ms: 1.07x slower                                                        |
| thrift                           | 322 us                                                   | 345 us: 1.07x slower                                                        |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.08x slower                                                       |
| nbody                            | 54.2 ms                                                  | 58.9 ms: 1.09x slower                                                       |
| meteor_contest                   | 47.7 ms                                                  | 52.2 ms: 1.09x slower                                                       |
| pprint_pformat                   | 665 ms                                                   | 728 ms: 1.09x slower                                                        |
| xml_etree_process                | 26.7 ms                                                  | 29.4 ms: 1.10x slower                                                       |
| 2to3                             | 114 ms                                                   | 126 ms: 1.11x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 186 ms: 1.11x slower                                                        |
| shortest_path                    | 219 ms                                                   | 246 ms: 1.12x slower                                                        |
| pickle_pure_python               | 139 us                                                   | 159 us: 1.14x slower                                                        |
| regex_compile                    | 54.6 ms                                                  | 63.2 ms: 1.16x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 9.28 ms: 1.16x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.10 ms: 1.19x slower                                                       |
| connected_components             | 201 ms                                                   | 239 ms: 1.19x slower                                                        |
| mako                             | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                       |
| django_template                  | 13.6 ms                                                  | 17.2 ms: 1.26x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 7.22 ms: 1.27x slower                                                       |
| scimark_lu                       | 51.3 ms                                                  | 65.1 ms: 1.27x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 270 ms: 1.27x slower                                                        |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 577 us: 1.38x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 161 ms: 1.43x slower                                                        |
| coverage                         | 26.9 ms                                                  | 40.5 ms: 1.51x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 111 ms: 3.47x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (3): json_loads, sympy_integrate, async_tree_eager_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261022-3.16.0a1+dev-ab5187c-NOGIL/bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 95.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.30x