# Results vs. 3.12.6

- fork: python
- ref: 9609574e7fd36edfaa8b
- machine: darwin-arm64
- commit hash: 9609574
- commit date: 2026-01-03
- overall geometric mean: 1.175x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.2 ms: 1.08x faster                                                    |
| sphinx         | 434 ms                                                   | 389 ms: 1.12x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.22x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 232 ms: 1.98x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.7 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.62x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 249 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.7 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.3 ms: 2.50x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.16x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.5 ms: 1.25x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.0 ms: 1.36x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 32.6 ms: 1.19x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.2 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 93.5 us: 1.10x faster                                                    |
| tomli_loads          | 957 ms                                                   | 878 ms: 1.09x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.01x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.75 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.23 ms: 1.14x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 19.8 ms: 1.10x faster                                                    |
| mako            | 4.77 ms                                                  | 4.72 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.05x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.94 ms: 5.28x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.22x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| mdp                              | 1.09 sec                                                 | 528 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 232 ms: 1.98x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 98.7 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.2 us: 1.63x faster                                                    |
| deepcopy                         | 161 us                                                   | 99.6 us: 1.62x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.62x faster                                                     |
| generators                       | 21.9 ms                                                  | 15.0 ms: 1.47x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.97 us: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.38x faster                                                    |
| go                               | 70.0 ms                                                  | 51.5 ms: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.0 ms: 1.36x faster                                                    |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 249 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 39.6 ns: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 43.5 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| k_core                           | 1.12 sec                                                 | 898 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.5 ms: 1.22x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 32.6 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| nbody                            | 54.2 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.60 ms: 1.17x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 44.3 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.7 ms: 1.15x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.15x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.45 us: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.23 ms: 1.14x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.13x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.8 ms: 1.13x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.4 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.7 us: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.2 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                    |
| sphinx                           | 434 ms                                                   | 389 ms: 1.12x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.86 ms: 1.12x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.22 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.4 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 93.5 us: 1.10x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 19.8 ms: 1.10x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 878 ms: 1.09x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.2 ms: 1.08x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.4 ms: 1.08x faster                                                    |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                     |
| pycparser                        | 497 ms                                                   | 465 ms: 1.07x faster                                                     |
| sympy_str                        | 104 ms                                                   | 97.9 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 632 ms: 1.05x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.9 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 164 ms: 1.02x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.01x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.72 ms: 1.01x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 416 us: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                   |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                    |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                     |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.4 ms: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                    |
| connected_components             | 201 ms                                                   | 210 ms: 1.05x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.75 ms: 1.09x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 932 us: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.3 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| coverage                         | 26.9 ms                                                  | 31.6 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 251 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.3 ms: 2.50x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260103-3.15.0a3+-9609574-CLANG/bm-20260103-macm4pro-arm64-python-9609574e7fd36edfaa8b-3.15.0a3+-9609574.json: pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.175x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.21x